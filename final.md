
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int a = 0;
    int b =0;
    int d = 0;
    int n_de_zeros_a_esquerda = 0;					//alterar aqui o numero de zeros à esquerda <--------------
    int c =0;
    int f = 0;
    int v =0;
    int fac = 0;
    int e =0;
    int control = 0;
    int num=0;
    vector<int> k;
    for(int l=0;l<6;l++){
    	k.push_back(0);
	}
    while(control==0){
        a++;
		k[5]=a;
        if(a==10){
            a=0;
            k[5]=a;
            b++; 
			k[4]=b;
            if(b==10){
                b=0;
                k[4]=b;
                c++;
                k[3]=c;
                if(c==10){
                    c=0;
                    k[3]=c;
                    d++;
                    k[2]=d;
                    if (d==10){
                    	d=0;
                    	k[2]=d;
                        e++;
                        k[1]=e;
                        if(e==10){
                            e=0;
                            k[1]=e;
                            f++;
                            k[0]=f;
                            if(f==10){
                                control=1;
                            }
                        }
                    }

                }
            }

        }
		num=a+b*10+c*100+d*1000+e*10000+f*100000;
		for(int m=0;m<6;m++){	
			if(k[5-m]==0){
				fac = 1;	
			}
			if(k[5-m]==1){
				fac = 1;
			}
			if(k[5-m]==2){
				fac = 2;
			}
			if(k[5-m]==3){
				fac = 6;
			}
			if(k[5-m]==4){
				fac = 24;
			}
			if(k[5-m]==5){
				fac = 120;
			}
			if(k[5-m]==6){
				fac = 720;
			}
			if(k[5-m]==7){
				fac = 5040;
			}
			if(k[5-m]==8){
				fac = 40320;
			}
			if(k[5-m]==9){
				fac = 362880;
			}
			num=num-fac;
		}
		num = num+n_de_zeros_a_esquerda;
		if (num==0) {
			cout << k[0]<<k[1]<<k[2]<<k[3]<<k[4]<<k[5]<<" ";
		}
    }
    return 0;
}
