<script>
let files;

$: if (files) {
  // Note that `files` is of type `FileList`, not an Array:
  // https://developer.mozilla.org/en-US/docs/Web/API/FileList
  console.log('files', files);

  for (const file of files) {
    console.log(`${file.name}: ${file.size} bytes`);
  }
}
</script>

<h1>Load Data</h1>

<form>
<label for="avatar">Upload some data:</label>
<input
	accept="application/json"
	bind:files
	id="avatar"
	name="avatar"
	type="file"
/>
<input type="submit" />
  
</form>

