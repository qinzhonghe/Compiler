# Compiler
编译原理课程实验——基于算符优先分析法的语法分析器

    						开发环境
1.Windos7 x64以上的操作系统;
2.vs2015/vs2017 x64平台;
3.安装并配置与平台兼容的 BOOST 1.64版本和QT版本;

                    动态链接库：opa-md-x64 项目概述

功能:基于算符优先分析算法，生成相应的DLL,和LIB文件。

项目属性配置:
1.BOOST 1.64在属性配置->C++目录上的配置;
2.在C/C++->代码生成->运行库中选择"MD"(Release版本)及"MDd"(Debug版本);
3.在链接器->输入->附加依赖项添加libboost_regex-vc141-mt-gd-x64-1_67.lib(Debug版本),
libboost_regex-vc141-mt-x64-1_67.lib(Release版本)。


                    GUI：SyntacticAnalyzer 项目概述

1.基于算符优先分析算法的算术表达式合法性检查器;
2.仅支持单个字符标识符的算术表达式检查;
3.根据给定的文法及终结符集合生成FIRST,LAST集和优先关系表；
4.支持查看分析过程;
5.支持高亮显示错误所在位置及其原因。

项目属性配置:
1.QT5.9
2.OPA-MD-X64
3.x64平台
4.在VS中配置项目属性的链接器的常规添加operator_precedence_analysisd.lib;
libboost_regex-vc141-mt-gd-x64-1_67.lib(Debug版本),
libboost_regex-vc141-mt-x64-1_67.lib;operator_precedence_analysis.lib(Release版本);
5.在配置属性->C++目录->库目录,添加"$(ProjectDir)\lib";
6.在配置属性->C++目录->包含目录,添加"$(ProjectDir)\include";
7.在链接器->输入项->附加库目录添加"$(ProjectDir)\lib";
8.在C/C++->预处理器->预处理器定义添加"BOOST_ALL_NO_LIB";
9.在链接器->命令行添加"/ENTRY:"mainCRTStartup""。

                GUI：SyntacticAnalyzer Release版本使用说明

1.仅支持Windows7以上的X64系统;
2.第一次运行可以按照当前的配置运行;
3.导入或输入表达式后点击检查按钮即可在输出项文本框看到结果;
4.检查结果带有超链接,点击即可查看分析过程;
5.任何输入项都是一行一个，包括终结符集合请按行输入;
6.文法和终结符均可配置。
