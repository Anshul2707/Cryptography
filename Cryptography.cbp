#include <iostream>
using namespace std;
void encrypt(int n, string str)
{   char dictionary[]={'\0','a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z'};
    char dictionary1[]={'\0','A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z'};
    char dictionarynum[]={'\0','1','2','3','4','5','6','7','8','9'};
    int k=0;
    std::string finalstr;
    for (auto x : str)
    {   k=0;
        for(int i=1;i<27;i++)
        {
            if(dictionary[i]==x)
            {   if((i+n)>26)
                {
                    finalstr=finalstr+dictionary[(i+n)%26];
                    k=k+1;
                }
                else
                {
                    finalstr=finalstr+dictionary[(i+n)];
                    k=k+1;
                }
            }
            else if(dictionary1[i]==x)
            {
                if((i+n)>26)
                {
                    finalstr=finalstr+dictionary1[(i+n)%26];
                    k=k+1;
                }
                else
                {
                    finalstr=finalstr+dictionary1[(i+n)];
                    k=k+1;
                }
            }
        }

        for(int i=0;i<10;i++)
        {   if(dictionarynum[i]==x)
            {
                if((i+n)>9)
                {
                    finalstr=finalstr+dictionarynum[(i+n)%9];
                    k=k+1;
                }
                else
                {
                    finalstr=finalstr+dictionarynum[(i+n)];
                    k=k+1;
                }
            }
        }

        if(k==0)
        {
           finalstr=finalstr+x;
        }
    }
    cout << finalstr <<"\n";
}

void decrypt(int n, string str)
{   char dictionary[]={'\0','a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z'};
    char dictionary1[]={'\0','A','B','C','D','E','F','G','H','I','J','K','L','M','N','O','P','Q','R','S','T','U','V','W','X','Y','Z'};
    char dictionarynum[]={'\0','1','2','3','4','5','6','7','8','9'};
    int k=0;
    std::string finalstr;
    for (auto x : str)
    {   k=0;
        for(int i=1;i<27;i++)
        {
            if(dictionary[i]==x)
            {   if((i-n)>0)
                {
                    finalstr=finalstr+dictionary[(i-n)];
                    k=k+1;
                }
                else
                {
                    finalstr=finalstr+dictionary[26+i-n];
                    k=k+1;
                }
            }
            else if(dictionary1[i]==x)
            {
                if((i-n)>0)
                {
                    finalstr=finalstr+dictionary1[i-n];
                    k=k+1;
                }
                else
                {
                    finalstr=finalstr+dictionary1[26+i-n];
                    k=k+1;
                }
            }
        }
        for(int i=1;i<10;i++)
        {
            if(dictionarynum[i]==x)
            {   if((i-n)>0)
                {
                    finalstr=finalstr+dictionarynum[(i-n)];
                    k=k+1;
                }
                else
                {
                    finalstr=finalstr+dictionarynum[9+i-n];
                    k=k+1;
                }
            }
        }
        if(k==0)
        {
           finalstr=finalstr+x;
        }
    }
    cout << finalstr <<"\n";
}


int main()
{   int n;
    int i;
    string str;
    cout<<"Welcome to cryptography program \n "<<endl;
    cout << "Enter your string ";
    getline(cin, str);
    cout<<"Give key ";
    cin>>n;
    cout<<"Menu"<<endl;
    cout<<"1. Encryption     2. Decryption "<<endl;
    cout<<"Your choice ";
    cin>>i;
    if(i==1)
    {
        encrypt(n,str);
    }
    if(i==2)
    {
        decrypt(n,str);
    }
    return 0;
}

