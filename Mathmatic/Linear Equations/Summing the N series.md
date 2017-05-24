# Summing the N series

### HackerRank

## Question
![Kiku](Images/Summing the N series Q.png)
![Test](Images/test.png)

## Solutions

* C++1
```bash
int SN(long double N){
    //long double x = N*(N+1)/2;
    //long double y = N*(N-1)/2;
    long double x = fmod(N, 1e9 + 7);
    return (int) fmod(x*x,  1e9 + 7);
}

int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */   
    int T;
    long double N;
    cin>>T;
    for(int i=0; i<T; ++i){
        cin>>N;
        cout<< SN(N)<< endl;
    }
    return 0;
}
```

* Java1
```bash
public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner sc = new Scanner(System.in);
        int T = sc.nextInt();
        BigInteger N;
        for(int i=0; i<T; ++i){
            N = sc.nextBigInteger();
            System.out.println(SN(N));
        }  
    }
    
    private static BigInteger MOD = new BigInteger("1000000007");
    
    private static BigInteger SN(BigInteger N){
        N = N.mod(MOD);
        return (N.multiply(N)).mod(MOD);
    }
```

## Explanation

![Kiku](Images/Summing the N series E.png)