# My random notes - garbage dump

#### Wayback Machine (archive.org) mirroring
    wget \
    --mirror \
    --convert-links \
    --adjust-extension \
    --page-requisites \
    --execute robots=off \
    --user-agent=mozilla \
    --random-wait \
    --no-cookies \
    --no-host-directories \
    --continue \
    --tries=1 \
    --cut-dirs=4 \
    --domains=archive.org \
    --accept-regex '.*http://www.idris.fr/.*' \
    https://web.archive.org/web/20061124071657/http://www.idris.fr/data/publications/JMFFT/
    
convert all html to utf-8

    iconv  -f iso-8859-1  -t utf-8  in.txt  -o out.txt
    
regex to search for wayback machine links in the html

    ((?:https?:\/\/web(?:-beta)?\.archive\.org(?::80)?\/(?:web(?:(?:\*|[\d]{1,14}(?:\*|(?:(?:i[dfm]|[cj]s|fw|oe)_))?\/)?)|save(?:\/_embed)?\/))?https?:\/\/.*(?::80)?\/*(JMFFT\/))
