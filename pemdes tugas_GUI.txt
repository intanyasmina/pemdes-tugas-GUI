import sys 
from PyQt5.QtWidgets import *

def window ():
    #_inisialisasi pyqt5
    app = QApplication(sys.argv)
    window = QWidget()

    #_menyiapkan label,menempelkan ke window
    #_settext dan posisi
    var = QLabel(window)
    var.setText('Input Biodata')
    var.setStyleSheet ("Font : Bold; color: #dcdcdc; Background-color: #e9967a; Font-size: 26pt")

    line = QLineEdit()
    line1= QLineEdit()
    line2= QLineEdit()

    lay = QFormLayout()
    lay.addRow (var)
    lay.addRow ('Name', line)
    lay.addRow ('Address', line1)
    lay.addWidget (line2)

    #_menampilkan CheckBox
    cek = QCheckBox ('Makan')
    cek1= QCheckBox ('Tidur')
    cek2= QCheckBox ('Main')
    lay.addRow('Hobby',cek)
    lay.addWidget(cek1)
    lay.addWidget(cek2)

    #_menampilkan Button
    but = QRadioButton ('Pelajar')
    but1= QRadioButton ('Pegawai')
    but2= QRadioButton ('Wiraswasta')
    lay.addRow('Status',but)
    lay.addWidget(but1)
    lay.addWidget(but2)

    #_menentukan ukuran window, + title dan menampilkan
    window.setLayout(lay)
    window.setGeometry(200,100,700,500)
    window.setWindowTitle('Biodata PyQt5')
    window.show()
    sys.exit(app.exec_())


	
if __name__ == '__main__':
   window()