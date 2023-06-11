# 1. <a id="project-overview">Project Overview</a>
Flowbiz is a startup that builds a platform for developing and managing all kinds of projects using outsourced professionals from all over the world.<br>
Entrepreneurs will develop their ideas into products on the platform, overcoming low funding and lack of technological knowledge.<br>
Small companies would pay precisely the value for product development via the platform, excluding unproductive time
## 1.1. <a id="technologies-overview"></a>Technologies
- Nodejs
- Express
- React
- Gatsby
- Mongodb
# 2. <a id="repos">Repos</a>
The following repos participate in constructing the Flowbiz platform
## 2.1 Pablo - Flowbiz Frontend Application
The [pablo](https://github.com/wonderfloyd/Pablo) application is a Gatsby React server that serves as the Landing page for Flowbiz.<br>
The public production site is [here](https://flowbiz.info/sEMuDsrhV2DMk0BH)
## 2.2 Flogo Server Simulator
This [Flogo Server Simulator](https://github.com/flowbiz/FlogoServerSimulator) serves pablo client both statically when pablo gatsby build process retrieves pages data in order to pre-render the pages ([Server Side Rendering](https://www.gatsbyjs.com/docs/how-to/rendering-options/using-server-side-rendering/))
and dynamically when the user operates using the react app in the browser.

# 3. <a id="protractor_tests">Protractor Tests</a>
End-To-End testing is done using protractor test suite.<br>
The tests simulate a user creating project and pages in the platform.<br>
Currently, there are 73 passing steps. Tests must always pass during development.

### 3.1. Install protractor globally
```bash
npm install protractor -g
```
### 3.2. Set Pablo environment variables
- **REACT_APP_PORT** should point the pablo gatsby server port (8000)
- **SimulatorDirectory** should point to the flogo server simulator directory
- when running the tests on local enviroment, in order to see the automathic tests browser running, the **NOT_HEADLESS** variable should be set to true
### 3.3. Run the tests suite
```bash
protractor [Path_to_Pablo]\tests\consenz\conf_buildConsenzProjectFromScratch.js
```
![Image### 3.3.image.1](https://user-images.githubusercontent.com/55399150/143771292-d39bf52c-46fd-4a88-a667-0ce810e60e62.png)

