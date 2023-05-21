<script >
    import { marked } from 'marked';
	export let text = `here's some <strong>HTML!!!</strong>`;
    let localText =  text  
    $: originText = text
</script>

    <div >
        <h1>Render</h1>
        <p>{@html marked(localText) }</p>
    </div>
