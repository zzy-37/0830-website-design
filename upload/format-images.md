run following command from current dirctrory:

```bash
find \( -iname "*.jpg" -o -iname "*.jpeg" -o -iname "*.png" \) -exec identify -format "%d/%f,%w,%h\n" '{}' >pic.csv \;
```

outputs path to every pictures in the upload folder and their geometry
