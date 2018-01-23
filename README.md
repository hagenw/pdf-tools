# PDF tools

Bash scripts to manipulate PDF files.


## Installation

PDF tools depends on [simply-bash] and on [is.sh].

Install all files of [pdf-tools] into a directory in your `$PATH`. The easiest
way to achieve this is to clone the repository and add it to your `$PATH`:

```bash
git clone https://github.com/hagenw/pdf-tools.git ~/git/pdf-tools
echo 'PATH="${PATH}:${HOME}/git/pdf-tools"' >> ~/.bashrc
```

Replace `~/git/pdf-tools` with your desired directory.

Install [simply-bash] by cloning it and sourcing `simply-bash.sh`, e.g.

```bash
git clone https://github.com/hagenw/simply-bash.git ~/git/simply-bash
source ~/git/simply-bash/simply-bash.sh
```

Install [is.sh], into your simply-bash folder or in another folder included in
`$PATH`, e.g.

```bash
wget https://github.com/qzb/is.sh/raw/master/is.sh -O "${HOME}/.local/bin/is"
```

[pdf-tools]: https://github.com/hagenw/pdf-tools.git
[simply-bash]: https://github.com/hagenw/simply-bash
[is.sh]: https://github.com/qzb/is.sh


## Usage

### `pdf2png`

Generate a thumbnail of the given PDF file as a compressed PNG file.
Example:

```sh
$ pdf2png --max-size 400 --page 2 --output page2_400px.png input.pdf
```

### `pdfextract`

Extract pages from a PDF file.
Example:

```sh
$ pdfextract --pages "1 3-5" --output output.pdf input.pdf
```

### `pdfmerge`

Merge PDF files.
Example:

```sh
$ pdfmerge --output output.pdf input1.pdf input2.pdf input3.pdf
```

### `pdfshrink`

Shrink a PDF file.
Example:

```sh
$ pdfshrink --aggressive input.pdf
```
