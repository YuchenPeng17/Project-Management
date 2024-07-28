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











## Project Management