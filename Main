#define t(i) (s[i] - '0')
int decodeWays(string s)
{
    int n = s.size();
    int f[n + 1];
    int m = 1e9 + 7;
    f[0] = 1;
    for (int i = 1; i <= n; i++) {
        f[i] = 0;
        if (s[i - 1] > '0') {
            f[i] = f[i - 1];
        }
        if (i - 2 >= 0) {
            int c = t(i - 2) * 10 + t(i - 1);
            if (10 <= c && c <= 26)
                f[i] = (f[i] + f[i - 2]) % m;
        }
        if (f[i] == 0) return 0;
    }
    return f[n];
}
