# Content Keys

```py
import hashlib

# For example in my tubi script, this is how my string looks like before encoding it,

version_string = f"{item[1]}|{item[8]}|{item[3]}|" \
                 f"{item[2]}|{item[4]}|{item[6]}|" \
                 f"{item[5]}|{category}|{pro_url}" \
                 f"|{provider}|{cease}"

# item is just a list that's been yielded, but basically the elements are the metadata, such as title, release_date, url, other dates, genres, ratings, etc.

version_key = hashlib.md5(version_string.encode())
# and if you're yielding or returning 

def .....():
    return version_key.hexdigest()
    
# aa202acd61cb0cb6ec1d6cf876923399
[Example](https://i.imgur.com/ZoDLpAg.png)
