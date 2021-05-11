<script lang="ts">
    let description;
    let notes;
    let qty;
</script>

<form on:submit|preventDefault>
    <label>Name:</label>
    <input type='text' bind:value={description} class='border-gray-100' name="name"/>
    <label>Notes</label>
    <textarea bind:value={notes}></textarea>
    <label>Quantity</label>
    <input type='number' bind:value={qty} />

    <button type="submit">Submit</button>
</form>

<style>
    input {
        @apply border-blue-100;
    }
</style>
