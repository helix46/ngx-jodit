# ngx-jodit <a href="https://www.npmjs.com/package/ngx-jodit"><img alt="npm" src="https://img.shields.io/npm/v/ngx-jodit"></a></h1>

Angular wrapper for <a href="https://github.com/xdan/jodit">Jodit</a> WYSIWYG editor. It supports Angular >= 12.

<a href="">Demo</a>

## Options

All <a href="https://xdsoft.net/jodit/docs/classes/config.Config.html">options</a> from Jodit are supported.

## Installation

<ol>
  <li><code>npm install ngx-jodit --save</code></li>
  <li>Add <code>node_modules/jodit/build/jodit.min.css</code> to your app's assets in angular.json (or project.json for
    Nx)
  </li>
  <li>Add <code>NgxJoditModule</code> to the <code>imports</code> array in your app.module.ts</li>
  <li>Add <code>"skipLibCheck": true</code> to compilerOptions in your tsconfig.app.json. This is needed because the
    check fails to typing errors of the jodit package. If you know any other solution, let me know :).
  </li>
  <li>Now you can use the component<br/><code>&lt;ngx-jodit [(value)]="value"
    [(options)]="options">&lt;/ngx-jodit></code></li>
</ol>


## Options for ngx-jodit

<table class="table table-sm table-striped table-bordered">
  <thead>
  <tr>
    <td class="fw-bold">Name</td>
    <td class="fw-bold">Type</td>
    <td class="fw-bold">Description</td>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>value</td>
    <td>two-way data-binding</td>
    <td>Updates as soon as HTML value of the editor changed. You can set your value, too.</td>
  </tr>
  <tr>
    <td>options</td>
    <td>one-way data-binding</td>
    <td>Sets options for Jodit</td>
  </tr>
  </tbody>
</table>

## Events for ngx-jodit
<p>
  You can bind events using the Angular way, e.g.:<br/><code>&lt;ngx-jodit (joditChange)="onChange($event)">&lt;/ngx-jodit></code>
</p>
<table class="table table-sm table-striped table-bordered">
  <thead>
  <tr>
    <td class="fw-bold">Name</td>
    <td class="fw-bold">Description</td>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>joditChange</td>
    <td>Triggers as soon as something of the HTML value changes.</td>
  </tr>
  <tr>
    <td>joditKeyDown</td>
    <td>Triggers as soon as a key is pressed down.</td>
  </tr>
  <tr>
    <td>joditMousedown</td>
    <td>Triggers as soon as the left mouse button is pressed.</td>
  </tr>
  <tr>
    <td>joditClick</td>
    <td>Triggers as soon as the user clicks on the editor.</td>
  </tr>
  <tr>
    <td>joditFocus</td>
    <td>Triggers as soon as Jodit gets focus.</td>
  </tr>
  <tr>
    <td>joditPaste</td>
    <td>Triggers as soon as something is pasted.</td>
  </tr>
  <tr>
    <td>joditResize</td>
    <td>Triggers as soon as the editor resizes.</td>
  </tr>
  <tr>
    <td>joditBeforeEnter</td>
    <td>Triggers as soon as enter key is pressed.</td>
  </tr>
  <tr>
    <td>joditBeforeCommand</td>
    <td>Triggers before a command is executed.</td>
  </tr>
  <tr>
    <td>joditAfterExec</td>
    <td>Triggers after a command is executed.</td>
  </tr>
  <tr>
    <td>joditAfterPaste</td>
    <td>Triggers after something pasted.</td>
  </tr>
  <tr>
    <td>joditChangeSelection</td>
    <td>Triggers as soon as selection is changed.</td>
  </tr>
  </tbody>
</table>
