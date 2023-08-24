# 安装node

# 在项目根目录 初始化 
npm init -y

# 安装 typesrcipt （装过可以忽略）
npm install -D typescript 

# 创建 tsconfig.json 文件

# 在根目录新建 src/index.ts 文件

# 再新建 doc 文件，在此文件中初始化，生成package.json文件
cd doc
npm init -y 

# 新建 typedoc.json 文件

# 在 doc 文件夹下安装 typedoc
npm install -D typedoc

# 用命令查看是否安装成功
npx typedoc --version

# 通过命令生成 文档
npx typedoc --options ./typedoc.json

# TypeDoc 文档组织
// 将会生成文档
export class A {}

// 将深入遍历 utils 文件，utils 中的所有 export 将会生成文档
export * from './utils'

// B 只引入但是没导出，不会生成文档
import { B } from './others'

// C 接口没有导出，不会生成文档
interface C {}