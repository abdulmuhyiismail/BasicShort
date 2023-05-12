Aplikasi kelas  publik {

    public  static  void  main ( String [] args ) melempar  Pengecualian {

        Sistem . keluar . println ( "\nUrutkan Gelembung" );

        int [] arr1 = { 64 , 34 , 25 , 12 , 22 , 11 , 90 };

        Sistem . keluar . println ( "Array sebelum diurutkan : " );

        printArray ( arr1 );

        bubbleSort ( arr1 , "asc" );

        Sistem . keluar . println ( "Array setelah diurutkan (naik): " );

        printArray ( arr1 );

        bubbleSort ( arr1 , "desc" );

        Sistem . keluar . println ( "Array setelah diurutkan (descending): " );

        printArray ( arr1 );

        Sistem . keluar . println ( "\nUrutan Penyisipan" );

        int [] arr2 = { 64 , 34 , 25 , 12 , 22 , 11 , 90 };

        Sistem . keluar . println ( "Array sebelum diurutkan : " );

        printArray ( arr2 );

        insertionSort ( arr2 , "asc" );

        Sistem . keluar . println ( "Array setelah diurutkan (naik): " );

        printArray ( arr2 );

        insertionSort ( arr2 , "desc" );

        Sistem . keluar . println ( "Array setelah diurutkan (descending): " );

        printArray ( arr2 );

        Sistem . keluar . println ( "\nUrutkan Pilihan" );

        int [] arr3 = { 64 , 34 , 25 , 12 , 22 , 100 , 90 };

        Sistem . keluar . println ( "Array sebelum diurutkan : " );

        printArray ( arr3 );

        sortirpilihan ( arr3 , "asc" );

        Sistem . keluar . println ( "Array setelah diurutkan (naik): " );

        printArray ( arr3 );

        seleksiSort ( arr3 , "desc" );

        Sistem . keluar . println ( "Array setelah diurutkan (descending): " );

        printArray ( arr3 );

    }

    public  static  void  insertionSort ( int [] arr , Urutan string  ) {

        int  n = arr . panjang ;

        untuk ( int  i = 1 ; i < n ; i ++){

            int  kunci = arr [ i ];

            int  j = i - 1 ;

            

            if ( order . equals ( "asc" )){

                sementara ( j >= 0 && arr [ j ] > kunci ){

                    arr [ j + 1 ] = arr [ j ];

                    j = j - 1 ;

                }

                arr [ j + 1 ] = kunci ;

            } else  if ( order . equals ( "desc" )){

                while ( j >= 0 && arr [ j ] < kunci ){

                    arr [ j + 1 ] = arr [ j ];

                    j = j - 1 ;

                }

                arr [ j + 1 ] = kunci ;

            } lain {

                throw  new  Error ( "Urutan tidak diketahui" );

            }

        }

    }

    public  static  void  selectionSort ( int [] arr , Urutan string  ) {

        int  pos ;

        int  suhu ;

        for ( int  i = 0 ; i < arr . length ; i ++){

            pos = saya ;

            untuk ( int  j = i + 1 ; j < arr.panjang ; j ++ ) {

                if ( order . equals ( "asc" )){

                    if ( arr [ j ] < arr [ pos ]){ // temukan indeks minimum

                        pos = j ;

                    }

                } else  if ( order . equals ( "desc" )){

                    if ( arr [ j ] > arr [ pos ]){ // temukan indeks maksimum

                        pos = j ;

                    }

                } lain {

                    throw  new  Error ( "Urutan tidak diketahui" );

                }

            }

            temp = arr [ pos ]; // tukar elemen saat ini dengan minimum

            arr [ pos ] = arr [ i ];

            arr [ i ] = suhu ;

        }

    }

    public  static  void  bubbleSort ( int [] arr , Urutan string  ) {

        int  n = arr . panjang ;

        untuk ( int  i = 0 ; i < n - 1 ; i ++){

            untuk ( int  j = 0 ; j < n - i - 1 ; j ++){

                if ( order . equals ( "asc" )){

                    jika ( arr [ j ] > arr [ j + 1 ]) {

                        // tukar element arr[j] dengan arr[j + 1]

                        int  temp = arr [ j ];

                        arr [ j ] = arr [ j + 1 ];

                        arr [ j + 1 ] = suhu ;

                    }

                } else  if ( order . equals ( "desc" )){

                    jika ( arr [ j ] < arr [ j + 1 ]) {

                        // tukar element arr[j] dengan arr[j + 1]

                        int  temp = arr [ j ];

                        arr [ j ] = arr [ j + 1 ];

                        arr [ j + 1 ] = suhu ;

                    }

                } lain {

                    throw  new  Error ( "Urutan tidak diketahui" );

                }

            }

        }

    }

    public  static  void  printArray ( int [] arr ){

        int  n = arr . panjang ;

        untuk ( int  i = 0 ; i < n ; i ++){

            Sistem . keluar . cetak ( arr [ i ] + " " );

        }

        Sistem . keluar . println ();

    }

}
