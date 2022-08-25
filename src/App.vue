<template>
  <div class="app">
    <div class="main">
      <header>
        <div class="nav-bar">
          <p class="blockX">BlockX 1.0</p>
        </div>
      </header>
      <div class="body">
        <div class="workspaceBorder">
          <div class="workspaceLable">积木区</div>
          <div class="workspace" id="blockly-div"></div>
        </div>
           <div class="textAreaBorder">
          <div class="textAreaLable">文本域</div>
           <div class="textArea" id="code-div">
             <textarea id="python-code"></textarea>
           </div>
        </div>
      </div>
    </div>
  <xml id="toolbox" style="display:none">
    <category name="新变量" colour="#D44E42">
      <block type="variables_set"></block>
      <block type="variables_get"></block>
    </category>
    <category name="字面值" colour="#D47742">
      <block type="math_number"></block>
      <block type="logic_boolean"></block>
      <block type="logic_null"></block>
      <block type="character"></block>
    </category>
    <sep></sep>
    <category name="字符串" colour="#D49A42">
      <block type="text"></block>
      <block type="text_multiline"></block>
      <block type="text_join"></block>
      <block type="text_append"></block>
      <block type="text_length"></block>
      <block type="text_isEmpty"></block>
      <block type="text_indexOf"></block>
      <block type="text_charAt"></block>
      <block type="text_getSubstring"></block>
      <block type="text_changeCase"></block>
      <block type="text_trim"></block>
      <block type="text_count"></block>
      <block type="text_replace"></block>
      <block type="text_reverse"></block>
    </category>
    <category name="列表" colour="#D4C342">
      <block type="lists_create_with">
        <mutation items="1"></mutation>
      </block>
      <block type="list_comp" line_number="1" inline="false">
        <mutation items="1" />
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
      </block>
      <block type="list_comp" line_number="1" inline="false">
        <mutation items="2" />
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR1">
          <block type="comprehension_if" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
      </block>
      <block type="lists_getSublist"></block>
      <block type="Subscript" line_number="1" inline="true">
        <mutation>
        <arg name="I"/>
        </mutation>
      </block>
      <block type="Subscript" line_number="1" inline="true">
        <mutation>
        <arg name="S110"/>
        </mutation>
      </block>
      <block type="Subscript" line_number="1" inline="true">
        <mutation>
        <arg name="S111"/>
        </mutation>
      </block>
    </category>
    <category name="元组" colour="#B7D442">
      <block type="tuples_create_with">
        <mutation items="1"></mutation>
      </block>
      <block type="tuples_getSubtuple"></block>
    </category>
    <category name="集合" colour="#8AD442">
      <block type="sets_create_with">
        <mutation items="1"></mutation>
      </block>
      <block type="set_comp" line_number="1" inline="false">
        <mutation items="1"/>
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false"/>
        </value>
      </block>
      <block type="set_comp" line_number="1" inline="false">
        <mutation items="2" />
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR1">
          <block type="comprehension_if" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
      </block>
    </category>
    <category name="字典" colour="#65D442">
      <block type="dicts_create_with">
        <mutation items="1"></mutation>
      </block>
      <block type="dict_comp" line_number="1" inline="false">
        <mutation items="2" />
        <value name="ELT">
          <block type="dicts_pair" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR1">
          <block type="comprehension_if" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
      </block>
      <block type="dict_comp" line_number="1" inline="false">
        <mutation items="2" />
        <value name="ELT">
          <block type="dicts_pair" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR1">
          <block type="comprehension_if" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
      </block>
    </category>
    <category name="表达式" colour="#42D442">
      <category name="生成器表达式" colour="black">
        <block type="generator_expr" line_number="1" inline="false">
          <mutation items="1"/>
          <value name="GENERATOR0">
            <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false"/>
          </value>
        </block>
        <block type="generator_expr" line_number="1" inline="false">
          <mutation items="2" />
          <value name="GENERATOR0">
            <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
          </value>
          <value name="GENERATOR1">
            <block type="comprehension_if" line_number="1" inline="true" deletable="false" movable="false" />
          </value>
        </block>
      </category>
      <category name="逻辑及操作符" colour="black">
        <block type="if_expr" line_number="1"></block>
        <block type="BinOp"></block>
        <block type="UnaryOpUAdd"></block>
        <block type="UnaryOpUSub"></block>
        <block type="UnaryOpNot"></block>
        <block type="UnaryOpInvert"></block>
      </category>
    </category>
    <sep></sep>
    <category name="控制结构" colour="#42D463">
      <category name="循环结构" colour="black">
        <block type="for"></block>
        <block type="while"></block>
      </category>
      <category name="分支结构" colour="black">
        <block type="controls_if"></block>
      </category>
      <category name="条件" colour="black">
        <block type="Compare"></block>
        <block type="break"></block>
        <block type="continue"></block>
      </category>
    </category>
    <category name="增量赋值" colour="#42D492">
      <block type="aug_assign"></block>
    </category>
    <category name="类型转换" colour="#42D4BA">
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="bool" message="bool" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="int" message="int" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="float" message="float" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="str" message="str" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="list" message="list" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="tuple" message="tuple" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="set" message="set" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="frozenset" message="frozenset" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="dict" message="dict" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
    </category>
    <category name="内置函数" colour="#42D2D4">
      <category name="数学" colour="black">
        <block type="Call" line_number="1" inline="true">
          <mutation arguments="1" returns="true" parameters="true" method="false" name="abs" message="abs" premessage="" colour="190" module="">
          <arg name="UNKNOWN_ARG:0"/>
          </mutation>
        </block>
        <block type="Call" line_number="1" inline="true">
          <mutation arguments="1" returns="true" parameters="true" method="false" name="max" message="max" premessage="" colour="190" module="">
          <arg name="UNKNOWN_ARG:0"/>
          </mutation>
        </block>
        <block type="Call" line_number="1" inline="true">
          <mutation arguments="1" returns="true" parameters="true" method="false" name="min" message="min" premessage="" colour="190" module="">
          <arg name="UNKNOWN_ARG:0"/>
          </mutation>
        </block>
        <block type="Call" line_number="1" inline="true">
          <mutation arguments="1" returns="true" parameters="true" method="false" name="pow" message="pow" premessage="" colour="190" module="">
          <arg name="UNKNOWN_ARG:0"/>
          </mutation>
        </block>
        <block type="Call" line_number="1" inline="true">
          <mutation arguments="1" returns="true" parameters="true" method="false" name="round" message="round" premessage="" colour="190" module="">
          <arg name="UNKNOWN_ARG:0"/>
          </mutation>
        </block>
        <block type="Call" line_number="1" inline="true">
          <mutation arguments="1" returns="true" parameters="true" method="false" name="sum" message="sum" premessage="" colour="190" module="">
          <arg name="UNKNOWN_ARG:0"/>
          </mutation>
        </block>
      </category>
      <category name="其他" colour="black">
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="aiter" message="aiter" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="all" message="all" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="any" message="any" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="anext" message="anext" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="ascii" message="ascii" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="bin" message="bin" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="bytearray" message="bytearray" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="bytes" message="bytes" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="callable" message="callable" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="chr" message="chr" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="classmethod" message="classmethod" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="compile" message="compile" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="complex" message="complex" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="delattr" message="delattr" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="dir" message="dir" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="divmod" message="divmod" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="enumerate" message="enumerate" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="eval" message="eval" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="exec" message="exec" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="filter" message="filter" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="format" message="format" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="getattr" message="getattr" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="globals" message="globals" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="hasattr" message="hasattr" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="hash" message="hash" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="help" message="help" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="hex" message="hex" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="id" message="id" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="isinstance" message="isinstance" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="issubclass" message="issubclass" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="iter" message="iter" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="len" message="len" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="locals" message="locals" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="map" message="map" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="memoryview" message="memoryview" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>

      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="next" message="next" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="object" message="object" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="oct" message="oct" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="open" message="open" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="ord" message="ord" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="property" message="property" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="range" message="range" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="repr" message="repr" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="reversed" message="reversed" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="setattr" message="setattr" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="sorted" message="sorted" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="staticmethod" message="staticmethod" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="type" message="type" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="vars" message="vars" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="zip" message="zip" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="__import__" message="__import__" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      </category>
    </category>
    <sep></sep>
    <category name="自定义函数" colour="#42ACD4">
      <block type="FunctionDef"></block>
      <block type="lambda">
        <mutation decorators="0" parameters="1" returns="false"/>
        <value name="PARAMETER0">
        <block type="FunctionParameter" line_number="1" movable="false" deletable="false">
          <field name="NAME">___</field>
        </block>
        </value>
      </block>
    </category>
    <category name="自定义类" colour="#428DD4">
      <block type="class_def" line_number="1" inline="false">
        <mutation decorators="0" bases="0" keywords="0"/>
        <field name="NAME">___</field>
      </block>
      <block type="class_def" line_number="1" inline="false">
        <mutation decorators="0" bases="1" keywords="0"/>
        <field name="NAME">___</field>
      </block>
      <block type="attribute" line_number="1">
        <field name="VALUE">___</field>
        <field name="ATTR">___</field>
      </block>
      <block type="assign" line_number="1" inline="true">
        <mutation initialized="false"/>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="0" returns="true" parameters="true" method="false" name="super" message="super" premessage="" colour="240" module=""/>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="super" message="super" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
    </category>
    <sep></sep>
    <category name="异常处理" colour="#426CD4">
      <block type="assert"></block>
      <block type="with"></block>
      <block type="try">
        <mutation orelse="false" finalbody="false" handlers="1">
          <arg name="3"></arg>
        </mutation>
      </block>
      <block type="raise"></block>
      <block type="with" line_number="1" inline="false">
        <mutation items="1">
          <as name="[object Object]"></as>
        </mutation>
        <value name="ITEM0">
          <block type="with_item_as" line_number="1" inline="true" deletable="false" movable="false"></block>
        </value>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="breakpoint" message="breakpoint" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
    </category>
    <category name="模块导入" colour="#4250D4">
      <block type="import" line_number="1" inline="true">
        <mutation names="1" from="false">
          <regular name="true" />
        </mutation>
        <field name="NAME0">___</field>
      </block>
      <block type="import" line_number="1" inline="true">
        <mutation names="1" from="true">
          <regular name="true" />
        </mutation>
        <field name="NAME0">___</field>
        <field name="MODULE">___</field>
      </block>
      <block type="import" line_number="1" inline="true">
        <mutation names="1" from="false">
          <regular name="false" />
        </mutation>
        <field name="NAME0">___</field>
        <field name="ASNAME0">___</field>
      </block>
      <block type="import" line_number="1" inline="true">
        <mutation names="1" from="true">
          <regular name="false" />
        </mutation>
        <field name="NAME0">___</field>
        <field name="ASNAME0">___</field>
        <field name="MODULE">___</field>
      </block>
    </category>
    <category name="输入/输出" colour="#5142D4">
      <category name="输出" colour="black">
        <block type="text_print"></block>
      </category>
      <category name="输入" colour="black">
        <block type="text_prompt_ext"></block>
        <block type="text_prompt"></block>
        <block type="Call" line_number="1" inline="true">
          <mutation arguments="1" returns="true" parameters="true" method="false" name="input" message="input" premessage="" colour="190" module="">
          <arg name="UNKNOWN_ARG:0"/>
          </mutation>
        </block>
      </category>
      <category name="文件读写" colour="black"></category>
    </category>
    <category name="注释" colour="#7342D4">
      <block type="Comment"></block>
    </category>
  </xml>
  </div>
</template>

<script>
import Vue from 'vue'
import Blockly from 'blockly'
import 'blockly/blocks'
import 'blockly/javascript'
import 'blockly/python'
import * as en from 'blockly/msg/en'
import Sk from 'skulpt'
import Blockx from 'blockx-drag'

import 'codemirror/lib/codemirror.css'
import 'codemirror/theme/elegant.css'
import 'codemirror/addon/display/fullscreen.css'
import CodeMirror from 'codemirror'
import 'codemirror/mode/javascript/javascript'
import 'codemirror/mode/xml/xml.js'
import 'codemirror/mode/css/css.js'
import 'codemirror/mode/htmlmixed/htmlmixed.js'
import 'codemirror/mode/python/python.js'
import 'codemirror/addon/selection/active-line.js'
import 'codemirror/addon/edit/matchbrackets.js'
Blockly.setLocale(en)

Vue.config.ignoredElements.push('xml')
Vue.config.ignoredElements.push('block')
Vue.config.ignoredElements.push('field')
Vue.config.ignoredElements.push('category')
Vue.config.ignoredElements.push('sep')
Vue.config.ignoredElements.push('value')
Vue.config.ignoredElements.push('statement')
Vue.config.ignoredElements.push('mutation')
Vue.config.ignoredElements.push('regular')
Vue.config.ignoredElements.push('arg')
Vue.config.ignoredElements.push('as')
Vue.config.ignoredElements.push('sets_create_with')
Vue.config.ignoredElements.push('class_def')
Vue.config.ignoredElements.push('FunctionDef')
Vue.config.ignoredElements.push('import')
Vue.config.ignoredElements.push('for_else')

Blockx.initBlockly(Blockly)
Blockx.initSk(Sk)
Blockx.initPythonToBlock()

const textToBlock = Blockx.getPythonToBlock()
// eslint-disable-next-line new-cap
const textToBlocks = new textToBlock()
export default {
  data () {
    return {
      workSpace: null,
      code: null,
      TxtArea: null
    }
  },
  mounted: function () {
    const that = this
    this.workSpace = Blockly.inject('blockly-div', {
      toolbox: document.getElementById('toolbox'),
      media: './media/',
      zoom: {
        controls: true,
        wheel: true,
        startScale: 1.0,
        maxScale: 3,
        minScale: 0.3,
        scaleSpeed: 1.2
      },
      trashcan: true
    })
    // this.TxtArea = document.getElementById('python-code')
    Blockly.HSV_SATURATION = 0.65
    Blockly.HSV_VALUE = 0.85
    Blockly.Xml.domToWorkspace(document.getElementById('toolbox'), this.workSpace)
    this.workSpace.addChangeListener(this.updateFunction)
    // 代码编辑editor
    this.editor = CodeMirror.fromTextArea(document.getElementById('python-code'), {
      lineNumbers: true, // 显示行号
      indentUnit: 4, // 缩进
      styleActiveLine: true,
      matchBrackets: true,
      mode: 'python', // 语言
      lineWrapping: true,
      theme: 'elegant' // 主题
    })
    this.editor.setOption('extraKeys', {
      // <Tab> to 4 <space>
      Tab: function (cm) {
        const spaces = Array(cm.getOption('indentUnit') + 1).join(' ')
        cm.replaceSelection(spaces)
      },
      // F11键切换全屏
      F11: function (cm) {
        cm.setOption('fullScreen', !cm.getOption('fullScreen'))
      },
      // Esc键退出全屏
      Esc: function (cm) {
        if (cm.getOption('fullScreen')) cm.setOption('fullScreen', false)
      }
    })
    this.editor.on('blur', function () {
      that.editor.off('change', that.updateFunctionEdi)
      that.workSpace.addChangeListener(that.updateFunction)
    })
    this.editor.on('focus', function () {
      that.editor.on('change', that.updateFunctionEdi)
      that.workSpace.removeChangeListener(that.updateFunction)
    })
  },
  methods: {
    updateFunction: function () {
      this.code = Blockly.Python.workspaceToCode(this.workSpace)
      document.getElementById('python-code').value = this.code
      this.editor.setValue(this.code)
    },
    updateFunctionEdi: function () {
      const blockXml = textToBlocks.convertSource(this.editor.getValue())
      this.workSpace.clear()
      Blockly.Xml.domToWorkspace(Blockly.Xml.textToDom(blockXml.xml), this.workSpace)
    }
  }
}

</script>
<style>
* {
  padding: 0;
  margin: 0;
}
.blockX {
  color: rgb(196,194,18);
  margin-left: 10%;
}
.main {
  background: url('../img/body.jpg');
  background-size: 100% 100%;
  width: 100%;
  height: calc(97vh);
}
.body {
  width: 100%;
  height: 93%;
  display: flex;
  justify-content: center;
}
.workspaceBorder {
  background: url('../img/boder.jpg');
  background-size: 100% 100%;
  border-radius:calc(4vh);
  width: 50%;
  height: 93%;
  display: flex;
  flex-direction: column;
  margin-top: 3%;
  margin-bottom: 3%;
}
.workspaceLable {
  text-align: center;
  background: url('../img/label.jpg');
  font-weight: bold;
  font-family: sans-serif;
  font-size: calc(4vh);
  width: 94%;
  height: 8%;
  margin-left: 3%;
  margin-top: 3%;
}
.workspace {
  background-color:  rgb(0,0,0,0.5);
  width: 94%;
  height: 85%;
  margin-left: 3%;
}
.textAreaBorder {
  background: url('../img/boder.jpg');
  background-size: 100% 100%;
  border-radius:calc(4vh);
  width: 30%;
  height: 93%;
  display: flex;
  flex-direction: column;
  margin-left: 3%;
  margin-top: 3%;
  margin-bottom: 3%;
}
.textAreaLable {
  text-align: center;
  background: url('../img/label.jpg');
  font-weight: bold;
  font-family: sans-serif;
  font-size: calc(4vh);
  width: 94%;
  height: 8%;
  margin-left: 3%;
  margin-top: 4%;
}
.textArea {
  background-color: orange;
  width: 94%;
  height: 85%;
  margin-left: 3%;
}

header {
  width: 100%;
  height: calc(4vh);
}

.nav-bar {
  height: calc(6vh);
  display: flex;
  font-weight: bold;
  font-family: sans-serif;
  font-size: calc(4vh);
  align-items: center;
  justify-content: space-between;
  background-color:  rgb(0,0,0,0.7);
}

header ul {
  display: flex;
  list-style: none;
  align-items: center;
  justify-content: space-between;
}

header ul li {
  float: left;
}

header ul li select {
  height: calc(4vh);
  margin: calc(4vh);
}

#python-code {
  width: 100%;
  height: 100%;
}

.CodeMirror {
  height: 100%;
}

</style>
