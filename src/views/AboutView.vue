<template>
  <div class="about">
    <div class="main">
      <header>
         <div class="nav-bar">
        <ul>
            <li id="blockx-version">
                <p class="blockX">blockX 1.0</p>
            </li>
            <li id="python-version">
                <label class="python">python:</label>
                <select>
                  <option>3.7</option>
                  <option>3.8</option>
                  <option>3.9</option>
                  <option>3.10</option>
                </select>
            </li>
        </ul>
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
    <category name="Variables" colour="225" custom="VARIABLE">
    </category>
    <category name="Literal Values" colour="30">

      <block type="return"></block>
      <block type="return_full"></block>
    </category>
    <category name="Calculations" colour="190">
    </category>
    <category name="Logic" colour="345"></category>
    <sep></sep>
    <category name="Classes" colour="240">
      <block type="class_def" line_number="1" inline="false">
        <mutation decorators="0" bases="0" keywords="0"></mutation>
        <field name="NAME">___</field>
      </block>
      <block type="class_def" line_number="1" inline="false">
        <mutation decorators="0" bases="1" keywords="0"></mutation>
        <field name="NAME">___</field>
      </block>
      <block type="attribute" line_number="1">
        <field name="VALUE">___</field>
        <field name="ATTR">___</field>
      </block>
      <block type="assign" line_number="1" inline="true">
        <mutation initialized="false"></mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="0" returns="true" parameters="true" method="false" name="super" message="super" premessage="" colour="240" module=""></mutation>
      </block>
      <block type="ellipsis"></block>
    </category>
    <category name="Functions" colour="210">
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
    <category name="Imports" colour="60">
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
    <sep></sep>
    <category name="Control Flow" colour="270">
      <block type="controls_if">
        <mutation orelse="false" elifs="0" />
      </block>
      <block type="for_else"></block>
      <block type="while"></block>
      <block type="break"></block>
      <block type="continue"></block>
      <block type="assert"></block>
      <block type="assert_full"></block>
      <block type="with"></block>
      <block type="try">
        <mutation orelse="false" finalbody="false" handlers="1">
          <arg name="3"></arg>
        </mutation>
        <field name="NAME0">___</field>
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
    </category>
    <sep></sep>
    <category name="Output" colour="140"></category>
    <category name="Input" colour="120"></category>
    <category name="Files" colour="170"></category>
    <sep></sep>
    <category name="Conversion" colour="120"></category>
    <category name="Builtin Functions" colour="15">
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="abs" message="abs" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
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
        <mutation arguments="1" returns="true" parameters="true" method="false" name="bool" message="bool" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="breakpoint" message="breakpoint" premessage="" colour="190" module="">
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
        <mutation arguments="1" returns="true" parameters="true" method="false" name="dict" message="dict" premessage="" colour="190" module="">
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
        <mutation arguments="1" returns="true" parameters="true" method="false" name="float" message="float" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="format" message="format" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="frozenset" message="frozenset" premessage="" colour="190" module="">
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
        <mutation arguments="1" returns="true" parameters="true" method="false" name="input" message="input" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="int" message="int" premessage="" colour="190" module="">
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
        <mutation arguments="1" returns="true" parameters="true" method="false" name="list" message="list" premessage="" colour="190" module="">
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
        <mutation arguments="1" returns="true" parameters="true" method="false" name="max" message="max" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="memoryview" message="memoryview" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="min" message="min" premessage="" colour="190" module="">
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
        <mutation arguments="1" returns="true" parameters="true" method="false" name="pow" message="pow" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="print" message="print" premessage="" colour="190" module="">
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
        <mutation arguments="1" returns="true" parameters="true" method="false" name="round" message="round" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="set" message="set" premessage="" colour="190" module="">
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
        <mutation arguments="1" returns="true" parameters="true" method="false" name="str" message="str" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="sum" message="sum" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="super" message="super" premessage="" colour="190" module="">
        <arg name="UNKNOWN_ARG:0"/>
        </mutation>
      </block>
      <block type="Call" line_number="1" inline="true">
        <mutation arguments="1" returns="true" parameters="true" method="false" name="tuple" message="tuple" premessage="" colour="190" module="">
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
    <category name="List Methods" colour="30"></category>
    <category name="String Methods" colour="120"></category>
    <category name="Subscripting" colour="15"></category>
    <category name="Generators" colour="15">
      <block type="list_comp" line_number="1" inline="false">
        <mutation items="1" />
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
      </block>
      <block type="generator_expr" line_number="1" inline="false">
        <mutation items="1" />
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
      </block>
      <block type="set_comp" line_number="1" inline="false">
        <mutation items="1" />
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
      </block>
      <block type="dict_comp" line_number="1" inline="false">
        <mutation items="2" />
        <value name="ELT">
          <block type="dict_item" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR1">
          <block type="comprehension_if" line_number="1" inline="true" deletable="false" movable="false" />
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
      <block type="generator_expr" line_number="1" inline="false">
        <mutation items="2" />
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR1">
          <block type="comprehension_if" line_number="1" inline="true" deletable="false" movable="false" />
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
      <block type="dict_comp" line_number="1" inline="false">
        <mutation items="2" />
        <value name="ELT">
          <block type="dict_item" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR0">
          <block type="comprehension_for" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
        <value name="GENERATOR1">
          <block type="comprehension_if" line_number="1" inline="true" deletable="false" movable="false" />
        </value>
      </block>
    </category>
    <category name="Comments" colour="60">
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
import Blockx from 'blockx'

// 引入媒体文件：我是在github上下载的blockly源码，将源码中的media文件放入我项目中的public文件夹下
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

console.log(Blockly)
const blockly = Blockx.initBlockly(Blockly)
console.log('blockly', blockly)
console.log('blockly', blockly.Blocks.BinOp)
export default {
  data () {
    return {
      workSpace: null,
      code: null
    }
  },
  mounted: function () {
    this.workSpace = blockly.inject('blockly-div', {
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
    console.log('workspace', this.workSpace)
    Blockly.HSV_SATURATION = 0.65
    Blockly.HSV_VALUE = 0.85
    blockly.Xml.domToWorkspace(document.getElementById('toolbox'), this.workSpace)
    this.workSpace.addChangeListener(this.updateFunction)
  },
  methods: {
    updateFunction: function () {
      this.code = blockly.Python.workspaceToCode(this.workSpace)
      document.getElementById('python-code').value = this.code
    }
  }
}

</script>
<style>
* {
  padding: 0;
  margin: 0;
}
.blockX, .python {
  color: rgb(196,194,18);
}
.main {
  background: url('../../img/body.jpg');
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
  background: url('../../img/boder.jpg');
  background-size: 100% 100%;
  border-radius:calc(4vh);
  width: 50%;
  height: 93%;
  display: flex;
  flex-direction: column;
  margin-left: 3%;
  margin-top: 3%;
  margin-bottom: 3%;
}
.workspaceLable {
  text-align: center;
  background: url('../../img/label.jpg');
  border-top-left-radius:calc(4vh);
  border-top-right-radius:calc(4vh);
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
  background: url('../../img/boder.jpg');
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
  background: url('../../img/label.jpg');
  font-weight: bold;
  font-family: sans-serif;
  font-size: calc(4vh);
  border-top-left-radius:calc(4vh);
  border-top-right-radius:calc(4vh);
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

#blockx-version {
  margin: calc(4vh);
}

#python-version {
  margin: auto;
}

#python-code {
  width: 100%;
  height: 100%;
}

.CodeMirror {
  height: calc(90vh) !important;
}

</style>
