<script>
    import { modal } from '../utils/modal';
    const close = () => ($modal.open = false);

    const handle_keydown = (e) => {
        if (e.key === 'Escape') return close();
    };
</script>

<svelte:window on:keydown|once={handle_keydown} />

<dialog open on:click|self|preventDefault={close}>
    <article>
        <h3>{$modal.title}</h3>
        <p>
            {$modal.message}
        </p>
        <footer>
            <button on:click|once={close}>OK</button>
        </footer>
    </article>
</dialog>