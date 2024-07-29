## Project Setup / 项目搭建

### 1. Overview / 总览

|                                  | 厨房管理                                                   | Python项目管理                                         |
| -------------------------------- | ---------------------------------------------------------- | ------------------------------------------------------ |
| 开发工具                         | 优质合适的厨具                                             | 提升开发效率的IDE                                      |
| 项目结构                         | 分区存放食材和厨具                                         | 代码结构良好                                           |
| 依赖管理和虚拟环境               | 管控食材采购和库存：确保食材新鲜，质量可靠，避免浪费       | 虚拟环境隔离项目依赖，确保项目环境稳定                 |
| 代码风格和质量控制               | 制定统一的菜品标准：无论哪个厨师上任，菜的口味都要一致     | 统一的风格让代码易于阅读和协作                         |
| 测试和持续集成/持续部署（CI/CD） | 优化厨房工作流程：引入新设备，改进操作流程，提高工作效率   | 自动化测试和持续集成：通过自动化手段提升开发效率和质量 |
| 代码文档                         | 编写菜谱和料理说明：详细记录菜品的制作流程和要点，方便传承 | 文档和注释：帮助他人快速上手和理解代码                 |

|                                                              | Kitchen Management                                           | Python Project Management                                    |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Development Tools                                            | High-quality and suitable kitchenware                        | IDE that enhances development efficiency                     |
| Project Structure                                            | Separate storage for ingredients and kitchenware             | Well-structured code                                         |
| Dependency Management and Virtual Environment                | Control over ingredient procurement and inventory: Ensure freshness, reliable quality, and avoid waste | Virtual environments to isolate project dependencies, ensuring a stable project environment |
| Code Style and Quality Control                               | Establish unified dish standards: Consistent taste regardless of the chef | Unified style makes code easy to read and collaborate on     |
| Testing and Continuous Integration/Continuous Deployment (CI/CD) | Optimize kitchen workflow: Introduce new equipment, improve processes, and increase efficiency | Automated testing and continuous integration: Use automation to enhance development efficiency and quality |
| Code Documentation                                           | Write recipes and cooking instructions: Detailed records of the preparation process and key points, facilitating inheritance | Documentation and comments: Help others quickly understand and get up to speed with the code |



### 2. Development Tool / 开发工具

- Version Control / 版本控制
  - Git
    - Meaningful commit messages / 有意义的提交信息
    - Frequent, small commits / 频繁小粒度提交
    - Use branch development / 使用分支开发
    - Regular sync and merge / 定期同步和合并
    - Use tags to mark versions / 使用标签标记版本

- IDE / 集成开发环境
  - VS Code



### 3. Project Structure / 项目结构

- The organization of files and directories within a project, how different components are organized, and how they relate to each other.
- 项目中文件和目录的组织方式，不同组件如何组织以及它们之间的关系

```
my_project/
├── docs/
│   ├── getting_started.md
│   ├── installation.md
│   ├── usage.md
│   ├── api_reference.md
│   └── faq.md
│   └── ...
├── my_package/
│   ├── __init__.py
│   ├── module1.py
│   └── module2.py
│   └── ...
├── tests/
│   ├── __init__.py
│   ├── test_module1.py
│   └── test_module2.py
│   └── ...
├── .gitignore
├── LICENSE
├── README.md
├── requirements.txt				# list all the dependencies e.g: "Flask==2.0.1"
└── setup.py								# install dependencies e.g: "pip install -r requirements.txt"
```

**Principles of a Project Structure**

- **Clear Separation**: Different components (e.g., source code, tests, documentation) should be placed in separate directories.
- **Modularity**: Code should be divided into different modules based on functionality and logic, with each module having a clear purpose.
- **Reusability**: General-purpose functions should be encapsulated into independent modules for easy reuse across the project.
- **Guidance**: Use meaningful directory and file names, add necessary comments and documentation to make it easier for other developers to understand the code.
- **Consistency**: Apply consistent naming conventions and coding styles throughout the project.

**一个好的Python项目结构的原则：**

- **清晰分离**：不同的组件（例如源代码、测试、文档）应放在不同的目录中。
- **模块化**：代码应根据功能和逻辑分成不同的模块，每个模块应有明确的目的。
- **可重用性**：通用功能应封装成独立的模块，以便在整个项目中轻松重用。
- **指导性**：使用有意义的目录和文件名，添加必要的注释和文档，方便其他开发者理解代码。
- **一致性**：在整个项目中应用一致的命名规范和编码风格。



### 4. Dependency Management

- The process of handling and organizing the libraries and packages that the project depends on.
- Dependencies are external pieces of code written by other developers that you use to add functionality to your project without writing it from scratch.

- 处理项目所依赖的库和包。
- 依赖是由其他开发人员编写的外部代码片段，你可以使用它们来为项目添加功能，而无需从头开始编写。

#### 4.1 Project Management Tools / 项目管理工具

**What is it?**

Dependency management ensures that your project has all the necessary libraries and tools it needs to run. This is done by listing the required packages in a file (like `package.json` for JavaScript or `requirements.txt` for Python), so when someone else runs your project, they can easily install the same packages you used.

**Why is it?**

Risk running into compatibility issues and other problems down the line.

Ensure that everything is up-to-date and working together seamlessly.

**Python**

- pip			 `requirements.txt`
- poetry                   `pyproject.toml`

**Javascript**

- npm			`package.json`
- yarn 



#### 4.2 Virtual Environment / 虚拟环境

Virtual environment is a tool that keeps your project's dependencies isolated from others on your computer. This means each project can have its own versions of libraries without conflicts. 

Without a virtual environment, all projects on your laptop run in a shared global environment. This means:

1. **Global Environment**:
   - All projects use the same set of globally installed libraries.
   - Installing or updating a library for one project can affect all other projects.
   - If a group project relies on specific versions, any mismatch or overwrite can cause severe errors.
2. **Virtual Environment**:
   - Each project has its own isolated environment with its own set of libraries.
   - Dependencies specified in the project's dependency management files are installed in this isolated environment.
   - This ensures consistency and prevents conflicts, as each project can have different versions of the same libraries.
   - In a group project, using a virtual environment ensures that everyone's environment is identical, avoiding version mismatch issues.

### 虚拟环境
虚拟环境是一种工具，用于将您的项目依赖项与计算机上的其他项目隔离开来。这意味着每个项目可以有自己的库版本，而不会发生冲突。

没有虚拟环境时，笔记本电脑上的所有项目都在共享的全局环境中运行。这意味着：

1. **全局环境**：
   - 所有项目使用相同的一组全局安装的库。
   - 为一个项目安装或更新库可能会影响所有其他项目。
   - 如果一个团队项目依赖于特定版本，任何版本不匹配或覆盖都可能导致严重错误。

2. **虚拟环境**：
   - 每个项目都有自己的隔离环境，并拥有自己的一组库。
   - 项目依赖管理文件中指定的依赖项会安装在这个隔离环境中。
   - 这确保了一致性并防止冲突，因为每个项目可以有不同版本的相同库。
   - 在团队项目中，使用虚拟环境可以确保每个人的环境是相同的，避免版本不匹配问题。

#### 4.3 Extra Docker

> Docker takes <u>an extra step in ensuring consistent behavior by encapsulating everything your application needs into a single container</u>.

Docker is a tool that packages your application and its dependencies into a container. This container can run on any computer that has Docker installed, ensuring that your application behaves the same way everywhere. It helps with consistency and simplifies deployment by bundling everything your app needs to run.



### 5. Code Style and Quality Control / 代码风格与质量控制



### 5.1 Benefits/一致代码风格和高质量代码的好处

- **Improves Code Readability**: Consistent code style makes the code easier to read and understand.
- **Enhances Team Collaboration**: Team members can collaborate more easily when everyone follows the same coding standards.
- **Reduces Errors**: Adhering to a standardized code style and quality control helps identify and reduce errors in the code.
- **Increases Code Maintainability**: Structured and consistent code is easier to maintain and update.

- **提高代码可读性**: 一致的代码风格使代码更容易阅读和理解。
- **促进团队协作**: 团队成员使用统一的编码规范，可以更轻松地合作。
- **减少错误**: 规范的代码风格和质量控制有助于发现和减少代码中的错误。
- **提升代码可维护性**: 结构化和一致的代码更易于维护和更新。



### 5.2 Guidlines / 参考

1. **Adhere to Style Guidelines**: Establishes a consistent coding style, improving readability and maintainability.(e.g., PEP 8 for Python, Google's JavaScript Style Guide).
2. **Use Linter Tools**: Helps catch style and logical errors early, ensuring code quality.(e.g., ESLint for JavaScript, Pylint for Python).
3. **Use Automatic Code Formatting Tools**: Ensures code consistency and saves time on manual formatting.(e.g., Prettier for JavaScript, Black for Python).
4. **Write Function and Class Documentation**: Provides clear understanding of code functionality, aiding maintenance and collaboration.(e.g., JSDoc for JavaScript, PEP 257 for Python).
5. **Focus on Code Complexity**: Simplifies code, making it easier to understand, maintain, and reduce potential bugs.
6. **Conduct Performance Analysis and Optimization**: Improves application efficiency and responsiveness, which is critical for user experience.
7. **Use Security Scanning Tools**: Protects the code from vulnerabilities and security risks, ensuring safe operation.
8. **Use Type Annotations**: Enhances code clarity and can prevent type-related bugs, though not always supported in all languages.

Prioritize foundational practices that improve code readability, quality, and consistency first, followed by performance, security, and type clarity enhancements.

1. **遵循风格指南**：建立一致的编码风格，提升代码的可读性和可维护性。（例如：Python 的 PEP 8，Google 的 JavaScript 风格指南）。
2. **使用 Linter 工具**：帮助及早发现风格和逻辑错误，确保代码质量。（例如：JavaScript 的 ESLint，Python 的 Pylint）。
3. **使用自动代码格式化工具**：确保代码一致性并节省手动格式化的时间。（例如：JavaScript 的 Prettier，Python 的 Black）。
4. **编写函数和类的文档**：提供对代码功能的清晰理解，有助于维护和协作。（例如：JavaScript 的 JSDoc，Python 的 PEP 257）。
5. **关注代码复杂度**：简化代码，使其更易于理解、维护，并减少潜在错误。
6. **进行性能分析和优化**：提升应用程序的效率和响应速度，这对用户体验至关重要。
7. **使用安全扫描工具**：保护代码免受漏洞和安全风险的侵害，确保安全运行。
8. **使用类型注解**：增强代码的清晰度，防止类型相关的错误，尽管并非所有语言都支持。

通过遵循这一顺序，您可以优先考虑提升代码可读性、质量和一致性的基础实践，然后再关注性能、安全和类型清晰度的增强。



## 6. CI/CD / 持续集成/持续部署

### 6.1 Continuous Integration/持续集成:

- **Purpose**: To automatically integrate code changes from multiple contributors into a shared repository multiple times a day.
- **Process**: When code is committed to the repository, CI systems automatically build and test the changes to ensure they do not break the existing codebase.
- **Tools**: Popular CI tools include Jenkins, Travis CI, CircleCI, and GitHub Actions.
- **目的**：自动将多个贡献者的代码更改多次集成到共享的代码库中。
- **过程**：当代码提交到代码库时，CI 系统会自动构建并测试更改，以确保它们不会破坏现有代码库。
- **工具**：流行的 CI 工具包括 Jenkins、Travis CI、CircleCI 和 GitHub Actions。

### 6.2 Continuous Deployment (CD):

> 部署是指将应用程序或<u>系统从开发环境发布到生产环境的过程</u>，使其可供最终用户使用。部署包括将代码、配置文件、数据库和其他依赖项<u>部署到服务器或云平台</u>上，并确保应用程序在目标环境中正确运行。

- **Purpose**: To automate the deployment of code to production or staging environments after passing all required tests.
- **Continuous Delivery**: Ensures that code is always in a deployable state, but deployments are triggered manually.
- **Continuous Deployment**: Extends continuous delivery by automatically deploying every code change that passes the CI pipeline to production.
- **目的**：在通过所有必要测试后，自动将代码部署到生产或预发布环境。
- **持续交付**：确保代码始终处于可部署状态，但部署是手动触发的。
- **持续部署**：扩展了持续交付的概念，自动将通过 CI 流水线的每个代码更改部署到生产环境。
- Docker Hub, AWS, Heroku

### 6.3 Example: Setting up a CI/CD Pipeline with GitHub Actions

Let's assume a Python project and I want to automate the following steps:

1. Run tests every time code is pushed to the repository. (CI)
2. Deploy the code to a staging server if tests pass on the main branch. (CD)

I need to create the Workflow File and define the Workflow in that file, for example:
```yml
name: CI/CD Pipeline

# Define when the workflow should run
on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

# Define the jobs
jobs:
  test:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Set up Python
      uses: actions/setup-python@v2
      with:
        python-version: '3.8'

    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt

    - name: Run tests
      run: |
        pytest

  deploy:
    runs-on: ubuntu-latest
    needs: test
    if: github.ref == 'refs/heads/main'

    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Set up Python
      uses: actions/setup-python@v2
      with:
        python-version: '3.8'

    - name: Install dependencies
      run: |
        python -m pip install --upgrade pip
        pip install -r requirements.txt

    - name: Deploy to staging
      run: |
        echo "Deploying to staging server..."
        # Add your deployment commands here
        ssh user@staging-server 'bash -s' < deploy_script.sh
      env:
        DEPLOY_KEY: ${{ secrets.DEPLOY_KEY }}

```

This example demonstrates how to set up a CI/CD pipeline for a Python project. The pipeline runs tests on every push to the `main` branch and deploys to a staging server if the tests pass.



## 7. Documents / 文档

### 项目文档的关键部分 / Key Components of Project Documentation

- **README文件**：每个项目都应有一个README文件（通常是README.md），包含项目概述、安装指南、使用示例和贡献指南等内容。
- **代码注释**：良好的代码注释可以帮助其他开发者（包括未来的自己）理解代码的功能、参数和返回值等。
- **文档字符串（Docstring）**：一种特殊的多行注释，用于描述函数、类和模块的功能、参数和返回值等，放在它们的开头。可以使用适合语言的风格编写，如reStructuredText或Google风格。
- **项目文档**：对于大型项目，可能需要创建专门的文档，详细描述项目的架构、设计决策、API接口和使用示例等。
- **变更日志（Changelog）**：记录项目每个版本的变更内容，如新增功能、Bug修复和不兼容变更，帮助用户和开发者了解项目进展过程。
- **贡献指南（Contributing Guide）**：说明如何为项目贡献，包括如何提交Issue、设置开发环境和提交Pull Request等，吸引贡献者。
- **许可证（License）**：声明项目的版权和许可条款，选择合适的许可证很重要。
- **README File**: Every project should have a README file (typically README.md) that includes an overview of the project, installation instructions, usage examples, and contribution guidelines.
- **Code Comments**: Good code comments can help other developers (including your future self) understand the functionality, parameters, and return values of the code.
- **Docstrings**: Special multi-line comments that describe the functionality, parameters, and return values of functions, classes, and modules. They are placed at the beginning of these elements and can be written in styles suitable for the language, such as reStructuredText or Google style.
- **Project Documentation**: For larger projects, it might be necessary to create dedicated documentation detailing the project's architecture, design decisions, API interfaces, and usage examples.
- **Changelog**: Records the changes in each version of the project, such as new features, bug fixes, and breaking changes, helping users and developers understand the project's progress.
- **Contributing Guide**: Explains how to contribute to the project, including how to submit issues, set up the development environment, and submit pull requests, attracting contributors.
- **License**: States the project's copyright and licensing terms. Choosing the right license is crucial.

### 文档类型 / Document Type 

- **技术文档**：开发者文档、API文档
- **用户文档**：用户手册、操作指南
- **Technical Documentation**: Developer documentation, API documentation.
- **User Documentation**: User manuals, operation guides.



## Project Management