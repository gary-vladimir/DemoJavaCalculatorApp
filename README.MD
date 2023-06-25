# Tip Calculator Java GUI Creation Process

## Download SceneBuilder
this is used as a very simple way for creating the GUI layout and is basically like an editor that gives you the "HTML" at the end.

https://www.oracle.com/java/technologies/javafxscenebuilder-1x-archive-downloads.html


## Create new CalculatorApp.fxml file

this is done inside the SceneBuilder.

Make your GUI design in this step by using the editor.

![SceneBuilder Overview](SceneBuilding1.png)

After you are happy with your design, copy the generated Controller.java starting code> view ==> show sample controller skeleton. It should be similar to this one:
```
import javafx.event.ActionEvent;
import javafx.fxml.FXML;
import javafx.scene.control.Button;
import javafx.scene.control.Label;
import javafx.scene.control.Slider;
import javafx.scene.control.TextField;

public class CalculatorAppController {

    @FXML
    private TextField amountTextField;

    @FXML
    private Button calculateButton;

    @FXML
    private Label tipPercentageLabel;

    @FXML
    private Slider tipPercentageSlider;

    @FXML
    private TextField tipTextField;

    @FXML
    private TextField totalTextField;

    @FXML
    void CalculateButtonPressed(ActionEvent event) {

    }

}
```
The CalculatorApp.jxml is directly edited by the SceneBuilder (you don't need to export or anything like that).

To preview your current progress, simply Ctrl + P

## Download JDK (Java Dev Kit)

https://www.oracle.com/mx/java/technologies/downloads/#jdk20-windows

I downloaded the zip file. make sure to decompress in a known location.

## Adding aditional Imports CalculatorApp.fxml
```
<?import javafx.scene.control.*?>
<?import java.lang.*?>
<?import javafx.scene.layout.*?>
<?controller CalculatorAppController?>
```
The last line is for our CalculatorAppController.java

## Up and running the app

The main file for our app is the CalculatorApp.java. and the CalculatorAppController.java handles all the actions and events. We must compile both like this:

`javac --module-path C:\\Users\\Gary\\Downloads\\openjfx-20.0.1_windows-x64_bin-sdk\\javafx-sdk-20.0.1\\lib --add-modules javafx.controls,javafx.fxml CalculatorApp.java CalculatorAppController.java`

It looks longer than usual, but this is because we must add the modules that come from the downloaded JDK file ==> bin

Lastly to run the app do:

`
java --module-path C:\\Users\\Gary\\Downloads\\openjfx-20.0.1_windows-x64_bin-sdk\\javafx-sdk-20.0.1\\lib --add-modules javafx.controls,javafx.fxml CalculatorApp
`

in the same fashion, we must add the JDK modules. 