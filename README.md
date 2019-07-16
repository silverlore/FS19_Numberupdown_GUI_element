# FS19_Numberupdown_GUI_element
A Gui element forhandling number in the Gui for FS 19. The element can count a number up and down with arrow keys.

# Usage
Simple place the NumberUpDownElement.lua anywhere in the your project. And make sure the file is loaded 
either in the modDesc.xml:
```
<extraSourceFiles>
        <sourceFile filename="NumberUpDownElement.lua"/>
</extraSourceFiles>
```
or in loader file:
```
source(Utils.getFilename("NumberUpDownElement.lua", directory))
```
# Implement in Menu XML file.
The element is used the same way as multiTextOption with min 3 child elements.
1. Button for counting down
2. Button for counting up
3. Text element for displaying value.
4. \[option] Text element for title
5. \[option] bitmap for background
example:
```
<GuiElement type="numberUpDown" profile="multiTextOptionSettings" id="elementId">
    <GuiElement type="button" profile="multiTextOptionLeft"/>
    <GuiElement type="button" profile="multiTextOptionRight"/>
    <GuiElement type="text" profile="multiTextOptionText"/>
    <GuiElement type="text" profile="multiTextOptionSettingsTitle" text="Title"/>
    <GuiElement type="bitmap" profile="multiTextOptionBg"/> 
</GuiElement>
```
following xml attributes is possible to use:

| Attribute | Describtion |
| --------- | ----------- |
| increment | The value which the number is changed with for every click. |
| min | The minimum value the number can be counted down to. |
| max | The maximum value the number can be counted up to. |

Following function is available

| Function | Describtion |
| ---- | ---- |
| NumberUpDownElement:getValue() | Get the current value |
| NumberUpDownElement:setValue(value) | Set a new current value |
| NumberUpDownElement:getIncrement() | Get current increment value |
| NumberUpDownElement:setIncrement(increment) | Set a new increment value |
| NumberUpDownElement:getMin() | Get current minimum value |
| NumberUpDownElement:setMin(minValue) | Set a new minimum value |
| NumberUpDownElement:getMax() | Get current maximum value |
| NumberUpDownElement:setMax(maxValue) | Set a new maximum value |


