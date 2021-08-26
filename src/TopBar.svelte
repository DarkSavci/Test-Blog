<script>
    import TopAppBar, { Row, Section, Title,  } from "@smui/top-app-bar";
    import IconButton from "@smui/icon-button";

    import Textfield from '@smui/textfield';
    import Icon from '@smui/textfield/icon';

    let searchValue = '';

    let prominent = false;
    let dense = false;
    let secondaryColor = false;
</script>

<div class="flexy">
    <div class="top-app-bar-container flexor">
        <TopAppBar
            variant="static"
            {prominent}
            {dense}
            color={secondaryColor ? "secondary" : "primary"}
        >
            <Row>
                <Section>
                   <img class="logo" alt="Logo" src="https://www.iienstitu.com/img/logo.png">
                    <Title>Blog</Title>
                </Section>
                <Section>
                    <h5>Eğitimler &nbsp&nbsp</h5>
                    <h5>Eğitmenler &nbsp&nbsp</h5>
                    <h5>Sertifika &nbsp&nbsp</h5>
                </Section>
                    
                <Section align="end" toolbar>
                    <Textfield style="border-radius: 14px; background-color: #aeaeb4; width:250px; height:45px;" 
                    class="shaped-outlined"
                    variant="outlined"
                    bind:value={searchValue} 
                    label="Ne öğrenmek istersiniz?">
                        <Icon class="material-icons" slot="trailingIcon">search</Icon>
                    </Textfield>
                    &nbsp
                    <IconButton class="material-icons" aria-label="Notifications"
                        >notifications</IconButton
                    >
                    <IconButton
                        class="material-icons"
                        aria-label="Shopping Cart">shopping_cart</IconButton
                    >
                    <IconButton
                        class="material-icons"
                        aria-label="Manage Account">manage_accounts</IconButton
                    >
                </Section>
            </Row>
        </TopAppBar>
    </div>
</div>

<style>
    h5 {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        font-size: 16px;
    }

    h5:hover {
        color: #7b777e;
        transition: all 0.3s ease;
        cursor: pointer;
    }

    :root {
        --mdc-theme-primary: #1c1c24;
        --mdc-theme-secondary: #aeaeb4;
        --mdc-theme-surface: #fff;
    }

    .top-app-bar-container {
        width: 100%;
        height: 64px;
        background-color: var(--mdc-theme-background, #fff);

        overflow: auto;
        display: inline-block;
    }

    @media (max-width: 480px) {
        .top-app-bar-container {
            margin-right: 0;
        }
    }

    .logo {
        margin: 0;
        height: 50px;
        width: 50px;
        color: white;
    }

    .flexy {
        display: flex;
        flex-wrap: wrap;
    }

    .flexor {
        display: inline-flex;
        flex-direction: column;
    }
</style>
