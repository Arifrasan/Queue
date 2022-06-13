#include <iostream>
#define n 10
using namespace std;

struct mahasiswa{
    string nama;
    int nim;
}Mhs[n];

struct queue{
    int awal, akhir;
}Queue;

void deQueue();
void menu();
void inQueue();
void tampil();

void init(){
    Queue.awal = -1;
    Queue.akhir = -1;
    cout << "Data berhasil direset" << endl << endl;
    menu();
}

bool isFull(){
    if(Queue.akhir == n - 1){
        return true;
    } else {
        return false;
    }
}

bool isEmpty(){
    if(Queue.akhir == -1){
        return true;
    }else {
        return false;
    }
}

void inQueue(){
    if(!isFull()){
        string nama;
        int nim;
        cout << "Masukkan nama mahasiswa:";
        cin >> nama;
        cout << "Masukkan NIM mahasiswa:";
        cin >> nim;
        Mhs[Queue.akhir].nama = nama;
        Mhs[Queue.akhir].nim = nim;
        ++Queue.akhir;
        cout << endl;
        menu();
    }else {
        cout << "Data penuh";
        menu();
    }
}

void menu(){
    int pilih;
    cout << "1. masukkan data\n";
    cout << "2. Hapus satu data\n";
    cout << "3. Reset data\n";
    cout << "4. tampilkan data\n";
    cout << "Masukkan pilihan anda:";
    cin >> pilih;
    cout << endl;
    if(pilih == 1){
        inQueue();
    }else if(pilih == 2){
        deQueue();
    } else if(pilih == 3){
        init();
    }else if(pilih == 4){
        tampil();
    }else {
        menu();
    }
}

void deQueue(){
    if(!isEmpty()){
        for(int i = Queue.awal; i < Queue.akhir; i++){
            Mhs[i].nama = Mhs[i+1].nama;
            Mhs[i].nim = Mhs[i+1].nim;
        }Queue.akhir--;
        cout << "Data berhasil dihapus" << endl;
        cout << endl;
        menu();
    }else{
        cout << "antrian kosong" << endl;
    }
}

void tampil(){
    if(!isEmpty()){
        for(int i = 0; i < Queue.akhir; i++){
        cout << "Nama Mahasiswa: " << Mhs[i].nama << endl;
        cout << "NIM : " << Mhs[i].nim << endl; 
        cout << endl;
        }
    }else {
        cout << "data kosong";
        cout << endl << endl;
    }
    menu();
}

int main(){
    menu();

    return 0;
}
