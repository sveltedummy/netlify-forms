<script>
    import {Input, Textarea} from '../components';

    export let isDark;
</script>

<form name="nice" method="POST">
    <input type="hidden" name="form-name" value="nice" />
    <p style="display: none">
        <label>Don’t fill this out if you're human: <input name="bot-field" /></label>
    </p>
    <Input label="How are you today?" name="howareyou" {isDark} />
    <Textarea label="Thoughts on Svelte?" name="svelte" {isDark} />
    <Textarea label="Thoughts on my videos?" name="videos" {isDark} />
    <button type="submit" class="nes-btn is-primary">Submit</button>
</form>

<style>
    form {
        position: relative;
        max-width: 500px;
        margin: 0 auto;
    }
    button[type="submit"] {
        display: block;
        margin: 0 auto;
        margin-top: 15px;
    }
</style>