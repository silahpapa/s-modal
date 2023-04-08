# Modal Component
This component is a Vue 3 modal component written in TypeScript. It supports the following props:

## Installation
To use this component, simply import it into your Vue 3 project like so:

vue

```
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
        Launch demo modal
 </button>
<shb-modal id="exampleModal" >
   <p>This is the content of my modal.</p>
</shb-modal>
``` 

### Props
- id
The ID of the modal element. This prop is required and must be a string.

- title
The title of the modal. This prop is optional and must be a string.

- static
Whether or not the modal should be static. This prop is optional and must be a string. If set to 'static', the modal will not close when the user clicks outside of it.

- position
The position of the modal. This prop is optional and must be a string. If set to 'top', 'center', or 'bottom', the modal will be positioned at the top, center, or bottom of the screen, respectively.

- size
The size of the modal. This prop is optional and must be a string. If set to 'sm', 'md', 'lg', or 'xl', the modal will be small, medium, large, or extra-large, respectively.

