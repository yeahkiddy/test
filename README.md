int floyd_all_pairs_sp(int n, int A[][46]) { int i, j, k; for(k = 0; k < n; k++) {  for(i = 0; i < n; i++) {   for(j = 0; j< n; j++) {    if(i != j)  {     if(A[i][j] == 0) A[i][j] = STATION_INF;     A[i][j] = min(A[i][j], A[i][k] + A[k][j]);    }   }  } } return 0;}
