# simpleappmodify.java
JavaFX is a framework for building GUI (Graphical User Interface) applications in Java. It helps create windows, buttons, text, and more. In this project, we create a window with a button and a label. When the button is clicked, the label shows a message.
see the code::

import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Button;
import javafx.scene.control.Label;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class SimpleApp extends Application {
    public void start(Stage stage) {
        Label label = new Label("Click a button");

        Button greetButton = new Button("Say Hello");
        Button clearButton = new Button("Clear Text");

        greetButton.setOnAction(e -> label.setText("Hello, JavaFX!"));
        clearButton.setOnAction(e -> label.setText(""));

        VBox layout = new VBox(10);
        layout.getChildren().addAll(label, greetButton, clearButton);

        Scene scene = new Scene(layout, 250, 150);
        stage.setTitle("Simple JavaFX App");
        stage.setScene(scene);
        stage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
