# CureencyApps
aplikasi ini dapat menghitung nilai tukar dolar ke rupiah
satu dolarnya dianggap 15000 rupiah

#Fungsionalitas
-user dapat menambahkan angka
-apabila user memasukan huruf maka yang ditampilkan "INVALID"
user dapat mengetahui nilai tukar mata uang

#How does it works
- dimulai dari method mainwindows, pada clas mainwindows.xaml.cs
'''csharp
public MainWindow()
        {
            InitializeComponent();
            currencyController = new CurrencyController();
        }
'''
untuk logika nya itu berada pada class currencycontrol.cs atau sebagai berikut
'''csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
        '''
        cara kerjanya itu mengalikan nominal yang dimasukan dengan satuan dolarnya yang telah ditetapkan
