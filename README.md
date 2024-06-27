
import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class PetSelector extends JFrame {
    private JLabel label;
    private JRadioButton birdButton, catButton, dogButton, rabbitButton, pigButton;
    private ButtonGroup group;

    public PetSelector() {
        setTitle("Pet Selector");
        setSize(300, 200);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLayout(null);

        label = new JLabel("Choose a pet:");
        label.setBounds(10, 10, 200, 30);
        add(label);

        birdButton = new JRadioButton("Bird");
        birdButton.setBounds(10, 40, 200, 30);
        birdButton.addActionListener(new RadioButtonListener());

        catButton = new JRadioButton("Cat");
        catButton.setBounds(10, 70, 200, 30);
        catButton.addActionListener(new RadioButtonListener());

        dogButton = new JRadioButton("Dog");
        dogButton.setBounds(10, 100, 200, 30);
        dogButton.addActionListener(new RadioButtonListener());

        rabbitButton = new JRadioButton("Rabbit");
        rabbitButton.setBounds(10, 130, 200, 30);
        rabbitButton.addActionListener(new RadioButtonListener());

        pigButton = new JRadioButton("Pig");
        pigButton.setBounds(10, 160, 200, 30);
        pigButton.addActionListener(new RadioButtonListener());

        group = new ButtonGroup();
        group.add(birdButton);
        group.add(catButton);
        group.add(dogButton);
        group.add(rabbitButton);
        group.add(pigButton);

        add(birdButton);
        add(catButton);
        add(dogButton);
        add(rabbitButton);
        add(pigButton);
    }

    private class RadioButtonListener implements ActionListener {
        public void actionPerformed(ActionEvent e) {
            JRadioButton source = (JRadioButton) e.getSource();
            String pet = source.getText();
            JOptionPane.showMessageDialog(PetSelector.this, "You chose: " + pet);
        }
    }

    public static void main(String[] args) {
        SwingUtilities.invokeLater(() -> {
            PetSelector frame = new PetSelector();
            frame.setVisible(true);
        });
    }
}
```

<!---
Thelma005/Thelma005 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
