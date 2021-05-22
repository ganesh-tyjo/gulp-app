<!-- PROJECT SHIELDS -->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<br />
<p align="center">
  <a href="https://gulpjs.com">
    <img src="./content/images/gulp-logo.png" alt="Gulp" height="150" width="auto" >
  </a>
  <p align="center">The streaming build system</p>
</p>

---

This is a gulpfile with useful tasks. Using this you can automate all boring and repetitive tasks especially in regards to deploying a html, css and javascript website.

<br />
<details open='open'>
<summary><strong>Table of Contents<strong></summary>

- [Summary](#summary)
- [Common Tasks](#common-tasks)
- [Getting Started](#getting-started)
- [Roadmap](#roadmap)
- [Contribution](#contribution)
- [License](#license)
- [Author](#author)

</details>

## Summary

- Gulp is an open source javascript toolkit and task runner
- It was built on Node.js and NPM
- Used for time consuming and repetitive tasks
- Hundreds of plugins available for different tasks

## Common Tasks

- Minification of styles and scripts
- Concatenation
- Cache busting
- Testing, linting and optimization

## Getting Started

### Step - 1

Install [Node.js](https://nodejs.org/en/download/)

### Step - 2

Install Gulp globally using following command in command line.

```bash
npm install -g gulp
```

### Step - 3

Go to your project directory and run below command from inside that directory. It will create `package.json` file.

```bash
npm init -y
```

### Step - 4

Install required plugins and save them as development dependencies using below command.

```bash
npm install --save-dev gulp gulp-concat gulp-rename gulp-replace gulp-imagemin gulp-sourcemaps gulp-sass postcss gulp-postcss autoprefixer cssnano gulp-terser
```

This plugins serves below purposes.

`gulp gulp-concat gulp-rename gulp-replace` - Basic file operations such as concatenation, file renaming and file content replacement.

`gulp-imagemin` - Image optimization.

`gulp-sourcemaps` - Sourcemaps creation for styles and scripts.

`gulp-sass postcss gulp-postcss autoprefixer cssnano` - Sass/scss compilation and minify styles.

`gulp-terser` - Minify scripts.

After this your `package.json` file will look something like below.

```javascript
{
  "name": "gulp-app",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "autoprefixer": "^10.2.5",
    "cssnano": "^5.0.2",
    "gulp": "^4.0.2",
    "gulp-concat": "^2.6.1",
    "gulp-imagemin": "^7.1.0",
    "gulp-postcss": "^9.0.0",
    "gulp-rename": "^2.0.0",
    "gulp-replace": "^1.1.3",
    "gulp-sass": "^4.1.0",
    "gulp-sourcemaps": "^3.0.0",
    "gulp-terser": "^2.0.1",
    "postcss": "^8.2.15"
  }
}
```

### Step - 5

Create `gulpfile.js` file and copy content of my [gulpfile.js](https://github.com/ganesh-tyjo/gulp-app/blob/master/gulpfile.js 'ganesh-tyjo/gulpfile.js') in your file.

### Step - 6

Update paths in `gulpfile.js` file according to your project folder structure.

```javascript
// All paths
const paths = {
  html: {
    src: ['./src/**/*.html'],
    dest: './dist/',
  },
  images: {
    src: ['./src/content/images/**/*'],
    dest: './dist/content/images/',
  },
  styles: {
    src: ['./src/scss/**/*.scss'],
    dest: './dist/css/',
  },
  scripts: {
    src: ['./src/js/**/*.js'],
    dest: './dist/js/',
  },
  cachebust: {
    src: ['./dist/**/*.html'],
    dest: './dist/',
  },
};
```

### Step - 7

Run gulp tasks.

To run any specific task use below command.

```bash
gulp your-task-name
```

To run default task use below command.

```bash
gulp
```

This default task will run `watcher` task after finishing defined tasks. `watcher` will continuously watch for any file modifications and will run necessary tasks according to that.

To stop this `watcher` task and go out of watch state press `ctrl + c` in command prompt and answer the prompted question as `Y`.

```bash
^CTerminate batch job (Y/N)? Y
```

## Roadmap

See the [open issues](https://github.com/ganesh-tyjo/gulp-app/issues) for a list of proposed features (and known issues).

## Contribution

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See [LICENSE](https://github.com/ganesh-tyjo/gulp-app/blob/master/LICENSE 'ganesh-tyjo/LICENSE') for more information.

## Author

Ganesh Shinde - ganeshshinde.tyjo@gmail.com

Project Link - [https://github.com/ganesh-tyjo/gulp-app](https://github.com/ganesh-tyjo/gulp-app)

<!-- MARKDOWN LINKS & IMAGES -->

[contributors-shield]: https://img.shields.io/github/contributors/ganesh-tyjo/gulp-app.svg?style=for-the-badge
[contributors-url]: https://github.com/ganesh-tyjo/gulp-app/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ganesh-tyjo/gulp-app.svg?style=for-the-badge
[forks-url]: https://github.com/ganesh-tyjo/gulp-app/network/members
[stars-shield]: https://img.shields.io/github/stars/ganesh-tyjo/gulp-app.svg?style=for-the-badge
[stars-url]: https://github.com/ganesh-tyjo/gulp-app/stargazers
[issues-shield]: https://img.shields.io/github/issues/ganesh-tyjo/gulp-app.svg?style=for-the-badge
[issues-url]: https://github.com/ganesh-tyjo/gulp-app/issues
[license-shield]: https://img.shields.io/github/license/ganesh-tyjo/gulp-app.svg?style=for-the-badge
[license-url]: https://github.com/ganesh-tyjo/gulp-app/blob/master/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/ganesh-tyjo
