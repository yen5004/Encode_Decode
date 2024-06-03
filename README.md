# Encode_Decode
developer tips for cli commands


# Base64

You can easily encode and decode Base64 on the Linux command line using the `base64` utility. Here are the steps to do both:

### Base64 Encoding

To encode a file or a string in Base64, you can use the following commands:

### Encoding a File

To encode a file named `file.txt`:

```
base64 file.txt > file.txt.b64
```

This command will read `file.txt`, encode its contents in Base64, and save the output to `file.txt.b64`.

### Encoding a String

To encode a string directly:

```
echo -n "Your string here" | base64
```

The `-n` option for `echo` ensures that no newline character is added at the end of the string.

### Base64 Decoding

To decode a Base64-encoded file or string, you can use the following commands:

### Decoding a File

To decode a file named `file.txt.b64`:

```
base64 -d file.txt.b64 > file.txt
```

This command will read `file.txt.b64`, decode its contents from Base64, and save the output to `file.txt`.

### Decoding a String

To decode a Base64 string directly:

```
echo "WW91ciBzdHJpbmcgaGVyZQ==" | base64 -d
```

This will decode the Base64-encoded string and print the result.

### Examples

### Encoding a File

```
base64 myfile.txt > myfile.txt.b64
```

### Encoding a String

```
echo -n "Hello, World!" | base64
```

Output:

```
SGVsbG8sIFdvcmxkIQ==
```

### Decoding a File

```
base64 -d myfile.txt.b64 > myfile_decoded.txt
```

### Decoding a String

```
echo "SGVsbG8sIFdvcmxkIQ==" | base64 -d
```

Output:

```
Hello, World!
```

You can effectively encode and decode data in Base64 on the Linux command line using these commands.
