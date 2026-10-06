import java.awt.*;
import java.awt.event.*;
import java.util.Arrays;
import javax.swing.*;
import javax.swing.border.LineBorder;

public class Kalkulator {

    int lebarLayar = 360;
    int tinggiLayar = 540;

    Color abuAbuTerang = new Color(212, 212, 210);
    Color abuAbuGelap = new Color(80, 80, 80);
    Color hitam = new Color(28, 28, 28);
    Color oranye = new Color(255, 149, 0);

    String[] nilaiTombol = {
        "AC", "+/-", "%", "÷",
        "7", "8", "9", "×",
        "4", "5", "6", "-",
        "1", "2", "3", "+",
        "0", ".", "√", "="
    };

    String[] simbolKanan = {"÷", "×", "-", "+", "="};
    String[] simbolAtas = {"AC", "+/-", "%"};

    JFrame layar = new JFrame("Kalkulator");
    JLabel tampilan = new JLabel();
    JPanel panelTampilan = new JPanel();
    JPanel panelTombol = new JPanel();

// A+B, A-B, A*B, A/B
    String angkaA = "0";
    String operator = null;
    String angkaB = null;

    // Constructor untuk membuat tampilan kalkulator
    Kalkulator() {

        layar.setSize(lebarLayar, tinggiLayar);
        layar.setLocationRelativeTo(null);
        layar.setResizable(false);
        layar.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        layar.setLayout(new BorderLayout());

        // Mengatur tampilan angka
        tampilan.setBackground(hitam);
        tampilan.setForeground(Color.white);
        tampilan.setFont(new Font("Arial", Font.PLAIN, 80));
        tampilan.setHorizontalAlignment(JLabel.RIGHT);
        tampilan.setText("0");
        tampilan.setOpaque(true);

        panelTampilan.setLayout(new BorderLayout());
        panelTampilan.add(tampilan);
        layar.add(panelTampilan, BorderLayout.NORTH);

        // Mengatur panel tombol
        panelTombol.setLayout(new GridLayout(5, 4));
        panelTombol.setBackground(hitam);
        layar.add(panelTombol);

        // Membuat semua tombol kalkulator
        for (int i = 0; i < nilaiTombol.length; i++) {

            JButton tombol = new JButton();
            String nilaiTombolSaatIni = nilaiTombol[i];

            tombol.setFont(new Font("Arial", Font.PLAIN, 30));
            tombol.setText(nilaiTombolSaatIni);
            tombol.setFocusable(false);
            tombol.setBorder(new LineBorder(hitam));

            // Warna tombol bagian atas
            if (Arrays.asList(simbolAtas).contains(nilaiTombolSaatIni)) {
                tombol.setBackground(abuAbuTerang);
                tombol.setForeground(hitam);
            }

            // Warna tombol operator
            else if (Arrays.asList(simbolKanan).contains(nilaiTombolSaatIni)) {
                tombol.setBackground(oranye);
                tombol.setForeground(Color.white);
            }
                        // Warna tombol angka
            else {
                tombol.setBackground(abuAbuGelap);
                tombol.setForeground(Color.white);
            }

            panelTombol.add(tombol);
            // Aksi ketika tombol ditekan
            tombol.addActionListener(new ActionListener() {

                public void actionPerformed(ActionEvent e) {

                    JButton tombolDitekan = (JButton) e.getSource();
                    String nilaiTombol = tombolDitekan.getText();

                    // Jika tombol merupakan operator
                    if (Arrays.asList(simbolKanan).contains(nilaiTombol)) {

                        // Jika tombol "=" ditekan
                        if (nilaiTombol == "=") {

                            if (angkaA != null) {

                                angkaB = tampilan.getText();

                                double nilaiA = Double.parseDouble(angkaA);
                                double nilaiB = Double.parseDouble(angkaB);

                                if (operator == "+") {
                                    tampilan.setText(
                                        hapusDesimalNol(nilaiA + nilaiB)
                                    );
                                }

                                else if (operator == "-") {
                                    tampilan.setText(
                                        hapusDesimalNol(nilaiA - nilaiB)
                                    );
                                }

                                else if (operator == "×") {
                                    tampilan.setText(
                                        hapusDesimalNol(nilaiA * nilaiB)
                                    );
                                }
                                else if (operator == "÷") {
                                    tampilan.setText(
                                        hapusDesimalNol(nilaiA / nilaiB)
                                    );
                                }

                                bersihkanSemua();
                            }
                        }

                        // Jika tombol +, -, ×, atau ÷ ditekan
                        else if ("+-×÷".contains(nilaiTombol)) {

                            if (operator == null) {

                                angkaA = tampilan.getText();
                                tampilan.setText("0");
                                angkaB = "0";
                            }

                            operator = nilaiTombol;
                        }
                    }

                    // Jika tombol AC, +/-, atau % ditekan
                    else if (Arrays.asList(simbolAtas).contains(nilaiTombol)) {

                        // Tombol AC
                        if (nilaiTombol == "AC") {

                            bersihkanSemua();
                            tampilan.setText("0");
                        }

                        // Tombol +/-
                        else if (nilaiTombol == "+/-") {

                            double nilaiTampilan =
                                Double.parseDouble(tampilan.getText());

                            nilaiTampilan *= -1;

                            tampilan.setText(
                                hapusDesimalNol(nilaiTampilan)
                            );
                        }
                        // Tombol %
                        else if (nilaiTombol == "%") {

                            double nilaiTampilan =
                                Double.parseDouble(tampilan.getText());

                            nilaiTampilan /= 100;

                            tampilan.setText(
                                hapusDesimalNol(nilaiTampilan)
                            );
                        }
                    }

                    // Jika tombol angka atau titik ditekan
                    else {

                        // Tombol titik
                        if (nilaiTombol == ".") {

                            if (!tampilan.getText().contains(nilaiTombol)) {

                                tampilan.setText(
                                    tampilan.getText() + nilaiTombol
                                );
                            }
                        }

                        // Tombol angka 0-9
                        else if ("0123456789".contains(nilaiTombol)) {

                            if (tampilan.getText() == "0") {

                                tampilan.setText(nilaiTombol);
                            }

                            else {

                                tampilan.setText(
                                    tampilan.getText() + nilaiTombol
                                );
                            }
                        }
                    }
                }
            });

            layar.setVisible(true);
        }
    }

    // Menghapus semua data perhitungan
    void bersihkanSemua() {

        angkaA = "0";
        operator = null;
        angkaB = null;
    }

    // Menghilangkan .0 pada hasil bilangan bulat
    String hapusDesimalNol(double nilaiTampilan) {

        if (nilaiTampilan % 1 == 0) {

            return Integer.toString((int) nilaiTampilan);
        }

        return Double.toString(nilaiTampilan);
    }
}
