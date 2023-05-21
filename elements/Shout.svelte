<script>
	export let text = `here's some <strong>HTML!!!</strong>`;
    let localText =  text  
</script>

<div>
    <h1> InnerText 4 Markdown</h1>
        <div 
        contenteditable="true"
        bind:innerText={localText}>
    </div>
</div>
