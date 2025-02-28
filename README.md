
# 使用cli初始化项目 指定项目模版
npx create-next-app@latest nextjs-dashboard --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example" --use-pnpm
# css 组织方式
tailwind styled-comp css sass etc.
# 使用图片和字体并优化
nestjs 会下载字体文件到本地，打包到静态资源中；还可以指定下载字体的子集；把字体当做模块来处理，既可以使用字体库中的字体，也可使用本都字体
import Image from 'next/image'; 
使用 Image 内置组件去显示图片，会自动懒加载和进行图片其他的一些优化比如过度效果，占位效果等
# 路由组织
依靠文件结构来组织路由，page.tsx 文件和  layout.tsx 文件会被特殊对待，layout.tsx 会当做子级路由的容器
# 路由间跳转
import Link from 'next/link';  ui跳转，href属性指定路由
优点：按需加载，link组件出现的页面会自动预加载目标页面的代码，得益于文件夹结构组织路由的方式，代码已经被自动分割。
import { usePathname } from 'next/navigation'; 这个 hook 可以获取当前路由，需要在客户端渲染模式下使用 "use client"
# Vercel 发布，使用PostgreSQL 数据库