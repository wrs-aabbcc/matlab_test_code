# app_design_code
#These are some cases for matlab classdef     matlab中的 classdef定义类的使用

#Just for study not for any commercial interest. 

PLZ read these codes below at first.#先阅读以下matlab中app类， classdef的标准定义，再运行例子进行学习
#this is app classdef
classdef　类名 <matlab.apps.AppBase
　　properties(Access=public)
　　　　……
　　end
　　methods(Access=private)
　　　　　function 函数1（app,event）
　　　　　　……
　　　　　end
　　　　　function 函数2（app）
　　　　　　……
　　　　　end
　　　end
end

#this is classdef classExample, usually file name same as classExample
classdef classExample
    %UNTITLED Summary of this class goes here
    %   Detailed explanation goes here  详细解释如下
    
    properties               %定义属性－－－类变量
        x
        y
    end
    properties (Constant)    % 定义类常量
        z =100
    end
    
    methods                  % 定义类的方法
        function obj = classExample (a,b)   %构造函数，函数类名一致，完成类中变量的初始化
            obj.x = a;
            obj.y = b;
        end
        
        function display(obj)   % 自定义函数
            fprintf ('自定义类显示信息:\t ');
            fprintf('x+y = %d',obj.x + obj.y);
        end
    end
    
end
