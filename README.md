# A2-by-group-2

#include<bits/stdc++.h>>
#include<iomanip>
using namespace std;
class phong{
	private:
		char ma, loai;
		int tang, succhua;
		float gia;
		int trangthai;
	public:
		void nhap();
		void xuat();		
};

phong a[200];

void phong::nhap(){
	cout<<"nhap ma phong: ";
	cin>> ma;
	cin.ignore();
	cout<<"nhap loai phong: ";
	cin>> loai;
	cout<<"nhap tang: ";
	cin>> tang;
	cout<<"nhap suc chua: ";
	cin>> succhua;
	cout<<"nhap gia thue: ";
	cin>> gia;
	cout<<"nhap trang thai (1: con trong, 0: da thue): ";
	cin>> trangthai;
}

void phong::xuat(){
	cout<<left<<setw(10)<<ma
		<<setw(10)<<loai
		<<setw(10)<<tang
		<<setw(12)<<succhua
		<<setw(12)<<gia<<endl; 
		 
	if(trangthai==1){
		cout<<"con trong"<< endl;
	}else{
		cout<<"dathue"<< endl;
	}
}

	
int main(){
	int n;
	
	do{
		cout<<"nhap so luong phong: ";
		cin>>n;
	}while(n<=0||n>=200);
	cout<< "\nnhap sanh sach phong:\n ";
		for(int i=0; i<n; i++){
	cout<<"\nnhap phong thu "<<i+1<<":\n";
	a[i].nhap();
	}
	cout<<"\ndanh sach phong khach san: \n";
	cout<<left<<setw(10)<<"ma"
		<<setw(10)<<"loai"
		<<setw(10)<<"tang"
		<<setw(12)<<"suc chua"
		<<setw(12)<<"gia"<<endl; 
		
		for(int i=0; i<n; i++){
	a[i].xuat();
	}
	return 0;
}
