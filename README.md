# Mailer text editor with `angular`

## Instructions for quill text editer for mailing:

### Start by installing quill:
```bash
npm install ngx-quill@~27 quill
```
### Imports :
```ts
import 'quill/dist/quill.core.css';
import 'quill/dist/quill.snow.css';

imports:[CommonModule, FormsModule, QuillModule]
```

## Usage example :

In your `component` add this :

```ts
  emailContent='';
  quillModules = {
    toolbar: [
      ['bold', 'italic', 'strike'],
      ['blockquote', 'code-block'],

      [{ 'header': 1 }, { 'header': 2 }, { 'header': 3 }, { 'header': 4 }],
      [{ 'list': 'ordered'}, { 'list': 'bullet' }],
      [{ 'script': 'sub'}, { 'script': 'super' }],
      [{ 'indent': '-1'}, { 'indent': '+1' }],
      [{ 'direction': 'rtl' }],

      [{ 'size': ['small', false, 'large', 'huge'] }],
      [{ 'header': [1, 2, 3, 4, 5, 6, false] }],

      [{ 'color': [] }, { 'background': [] }],
      [{ 'font': [] }],
      [{ 'align': [] }],

      ['clean'],

      ['link', 'image', 'video'],
    ],
  };
```
And add this to the `HTML template` :

```html
<quill-editor class="w-8/12" [(ngModel)]="emailContent" [modules]="quillModules" placeholder="Compose your email..." />

<h3>Preview:</h3>

<div class="email-preview w-8/12" [innerHTML]="emailContent"></div>
```

# 🎉 And you're all set 🎊

# $${\color{green}happy\ coding}$$
