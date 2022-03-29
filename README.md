# gitbugr/opencv-4.5.1

Tahoma2D requires opencv version 4.5.1, so I created this keg to build this specific version

## How do I install these formulae?

`brew install gitbugr/opencv-4.5.1/opencv@4.5.1.rb`

Or `brew tap gitbugr/opencv-4.5.1` and then `brew install opencv@4.5.1.rb`.

### Tahoma2D

For the time being, Tahoma2D's plugins are linked to opencv dylibs stored in /usr/local/opt (subject to change). This keg does not create those symlinks for you. You can add them with the following command:
```sh
for f in $(find /usr/local/opt/opencv@4.5.1/lib -type f -name '*.4.5.1.dylib'); do
    ln -s $f "/usr/local/lib/$(echo $f | sed 's/.*lib\///' | sed s/4\.5\.1/4\.5/)"
done
```

## Documentation

`brew help`, `man brew` or check [Homebrew's documentation](https://docs.brew.sh).
