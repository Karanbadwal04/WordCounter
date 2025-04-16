
package com.wordcounter;

import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class WordCounter extends JFrame {
    private JPanel panel;
    private JTextArea textArea;
    private JButton buttonCount;
    private JLabel labelWordCount;

    public WordCounter() {
        setTitle("Word Counter");
        setSize(400, 300);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setLocationRelativeTo(null);

        panel = new JPanel();
        panel.setLayout(null);

        JLabel labelText = new JLabel("Enter text:");
        labelText.setBounds(30, 20, 100, 25);
        panel.add(labelText);

        textArea = new JTextArea();
        textArea.setBounds(30, 50, 300, 100);
        panel.add(textArea);

        buttonCount = new JButton("Count Words");
        buttonCount.setBounds(30, 160, 150, 25);
        panel.add(buttonCount);

        labelWordCount = new JLabel("Word Count: 0");
        labelWordCount.setBounds(30, 200, 150, 25);
        panel.add(labelWordCount);

        add(panel);

        buttonCount.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                countWords();
            }
        });
    }

    private void countWords() {
        String text = textArea.getText();
        if (text.isEmpty()) {
            labelWordCount.setText("Word Count: 0");
        } else {
            String[] words = text.trim().split("\s+");
            labelWordCount.setText("Word Count: " + words.length);
        }
    }

    public static void main(String[] args) {
        SwingUtilities.invokeLater(new Runnable() {
            @Override
            public void run() {
                new WordCounter().setVisible(true);
            }
        });
    }
}
