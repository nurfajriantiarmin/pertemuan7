# pertemuan7
    #include <iostream>
     #include <string>
     using namespace std;

     int main ()
     {
    int belanja,diskon,bayar;
    int batas_belanja = 1102019;
    int harga;

    cout << "\nMasukkan status anda (Menikah 'M' atau Belum Menikah 'BM' : ";
    string status;
    cin >> status;
    cout << "\nApakah anda sudah mempunyai anak (Ya atau Tidak) = ";
    string anak;
    cin >> anak ;
    cout << "\nApakah anda mempunyai kartu anggota (Ya atau Tidak)= ";
    string kartu_anggota;
    cin >> kartu_anggota;
    cout << "\nTotal belanja anda = ";
    cin >> belanja;

    if (status=="M" && belanja>=batas_belanja)
    {
        if (anak=="Ya")
        {
            cout << "\nDiskon 75%"<< endl;
            bayar=belanja - (harga * 0.75);
        }
        else
        {
            cout << "\nDiskon 50%"<< endl;
            bayar = belanja - ( harga* 0.50);
        }
    }
    else
    {
        if (kartu_anggota=="Ya" && belanja>=batas_belanja)
            {
            cout << "\nDiskon 25%"<< endl;
            bayar = belanja - ( harga * 0.25);
            }
        else{
            harga = belanja;
        }
    }
    cout << "\nTotal yang harus di bayar adalah Rp." << harga << endl;
    cout << "\nApakah anda berasal dari Makassar (Ya atau Tidak) : ";
    string asal;
    cin >> asal;

    if (asal=="Tidak")
    {
    cout << "\nAnda mendapatkan tambahan diskon 10%";
    bayar = harga - (harga * 0.10);
     }
     else
     { 
    bayar =harga;
     }
     cout << "Harga keseluruhan dari total belanja anda adalah Rp."<< harga << endl;
    return 0;
    }
