## ๐ [Flyway ์ ์ฉํด๋ณด๊ธฐ](README2.md)

# Flyway๋?

- ์คํ ์์ค ๋ฐ์ดํฐ๋ฒ ์ด์ค ๋ง์ด๊ทธ๋ ์ด์ ๋๊ตฌ
- ๋ฐ์ดํฐ๋ฒ ์ด์ค์ ํ์๊ด๋ฆฌ๋ฅผ ๋ชฉ์ ์ผ๋ก ํ๋ ํด์ด๋ค.
    - ๋ฐ์ดํฐ๋ฒ ์ด์ค์ ํ์๊ด๋ฆฌ๋?
        - git์ ํตํด ์ฐ๋ฆฌ๊ฐ ์ฝ๋๋ฅผ ๊ด๋ฆฌํ๋ ๊ฒ์ ๋ฐ์ดํฐ๋ฒ ์ด์ค ๋ฒ์ ์ผ๋ก ๋ณผ ์ ์๋ค.
        - git์์๋ ์ฝ๋๋ฅผ ํ์ผ๋ณ๋ก ๋ก๊น์ ํตํด์ ๋ณํ์ ์ด๋ ฅ์ ์ถ์ ํ๋ค.
        - flayway๋ ๋ฐ์ดํฐ๋ฒ ์ด์ค์ DDL ์ด๋ ฅ์ ์์์ DDL์ด ์ด๋ป๊ฒ ๋ณํ๋์๋์ง ๊ด๋ฆฌํ๋ ํด๋ก ์ฌ์ฉํ  ์ ์์ต๋๋ค.

![img.png](images/img.png)

- ๋ฒ์ ๋ณ DB ์คํฌ๋ฆฝํธ ํ์ผ์ ์ด๊ฑฐ ํด ๋๋ฉด ์์์ SQL ํ์ผ์ ์์ ํด ์ฃผ๊ณ  DB ๋ณ๊ฒฝ ์ด๋ ฅ์ ๋ํ ๊ด๋ฆฌ๋ฅผ ํด์ฃผ๋ ๋๊ตฌ
- ๊ณต์ ์ฌ์ดํธ์ ๋ฐ๋ฅด๋ฉด gradle, maven, CLI, Java API ์๋๋ค.

## ์ ์ฌ์ฉํด์ผ ํ ๊น?

### ํด๋จผ์๋ฌ
* ๋ฐฐํฌํ๊ฒฝ์ด ๋ค์ํ ์ํฉ์์ ์ง์  ๋ณ๊ฒฝ์ ๋ค๋ฃฌ๋ค๋ฉด ๋ฒ๊ฑฐ๋ก์๊ณผ ์ค์๊ฐ ๋ฐ์ํ๊ธฐ ์ฝ๋ค. 
    * DB์ ์ข๋ฅ๊ฐ ๋ฌ๋ผ์ง๋ฉด์ ๋ฌธ๋ฒ์ด ๋ฐ๋ ์๋ ์๊ณ  ๋ค์ํ ์ํฉ์์ ์ค์๊ฐ ๋์ฌ ์ ์๋ค.

### ํ์คํ ๋ฆฌ ๊ด๋ฆฌ
* ๋ฌธ์ ๊ฐ ์๊ฒผ์ ๋ ๋ณ๊ฒฝ๋ ์ด๋ ฅ์ ์ ์ ์์์ด ๋ชํํด์ง๊ธฐ ๋๋ฌธ์ ๋ฌธ์ ๋ฅผ ๋น ๋ฅด๊ฒ ํด๊ฒฐํ  ์ ์๋ค.

### ํ๊ฒฝ๋ถ๋ฆฌ
* ํ๊ฒฝ์ ๋ณด๋ค ์ฝ๊ฒ ๋ถ๋ฆฌํ๊ณ  ๊ด๋ฆฌ๊ฐ ๊ฐ๋ฅํ๋ค.

## Flyway ํน์ง
### ์ฅ์ 
1. ์ฌ๋ฌ ๋ฐ์ดํฐ๋ฒ ์ด์ค ๋ฐ ์๋ฒ์ ๋ฐ๋ฅธ ํจ์น ์ ์ฉ ์ฌ๋ถ๋ฅผ ๊ด๋ฆฌํ  ์ ์๋ค.
2. ํจ์น ์คํฌ๋ฆฝํธ์ ํ์คํ ๋ฆฌ ๊ด๋ฆฌ๊ฐ ๊ฐ๋ฅํ๋ค.
3. ํจ์น ์์ ์ ์ฌ๋์ ์ค์๋ฅผ ๋ฐฉ์งํ  ์ ์๋ค.

### ๋จ์ 
1. ์ต์ด baseline ์คํ ์ ๋ชจ๋ ๊ฐ์ ํ์์ ๊ฐ์ง๊ณ  ์์ด์ผ ํ๋ค.
2. ๋ฐ์ดํฐ๊ฐ ๋ค๋ฅด๋ฉด DML์ ํตํ ๋ก์ง ์ ๋ณด๊ฐ ์๋ค๋ฉด ๋ค๋ฅธ ๊ฒฐ๊ณผ๋ฅผ ๊ฐ์ ธ์ฌ ์ ์๋ค.
3. ์คํค๋ง ๋น๊ต๋ฅผ ํ  ์ ์๋ค.

## ๋์๋ฐฉ์
1. ์ค์น ํ ๊ธฐ๋ณธ ์ค์ ์ ์งํํ๋ฉด ๋ฒ์  ๊ด๋ฆฌ ํ์ด๋ธ์ด ์์ฑ๋ฉ๋๋ค.
2. Flyway๋ ๋ง์ด๊ทธ๋ ์ด์์ ์ํด ํ์ผ ์์คํ์ด๋ ํด๋์ค ํจ์ค๋ฅผ ๊ฒ์ฌํฉ๋๋ค.
3. ๋ง์ด๊ทธ๋ ์ด์์ ๋ฒ์  ๋ฒํธ๋ฅผ ๊ธฐ์ค์ผ๋ก ์ ๋ ฌ ๋๊ณ  ์์๋๋ก ์ ์ฉํฉ๋๋ค.
    1. ๊ฐ ๋ง์ด๊ทธ๋ ์ด์์ด ์ ์ฉ๋  ๋๋ง๋ค ์คํค๋ง ๊ธฐ๋ก ํ์ด๋ธ์ด ๊ทธ์ ๋ฐ๋ผ ์๋ฐ์ดํธ ๋ฉ๋๋ค.

### Flyway ๋ช๋ น์ด ์์๋ณด๊ธฐ
* init -SCHEMA_VERSION ์ baseline ๊ณผ ํจ๊ป ์์ฑํ๋ค. ํ์ด๋ธ์ด ์ด๋ฏธ ์์ฑ๋์ด ์์ผ๋ฉด ์ํ๋์ง ์๋๋ค.
* migrate - ์คํค๋ง์ ๋ณด๋ฅผ ๋ฆฌ์ผDB์ ๋ง์ด๊ทธ๋ ์ด์ํ๋ค.
* clean - flyway๋ก ์์ฑํ ์คํค๋ง๋ฅผ ๋ชจ๋ ์ญ์ ํ๋ค๊ณ  ํ์ง๋ง, ํด๋น ๋ฐ์ดํฐ ๋ฒ ์ด์ค์ ๋ชจ๋  ํ์ด๋ธ์ ์ญ์ ํ๋ค.
* info - DB์ ์ ์ฉ๋ ์คํค๋ง ์ ๋ณด์, ๋ก์ปฌ์ pending ๋์ด์๋ ๋ณ๊ฒฝ ์ ๋ณด๋ฅผ ๋ณด์ฌ์ค๋ค.
* validate - DB์ ์ ์ฉ๋ ์คํค๋ง ์ ๋ณด์, ๋ก์ปฌ์ ๋ณ๊ฒฝ์ ์ ๋น๊ตํ์ฌ ๋ณด์ฌ์ค๋ค.
* repair - ๋ง์ด๊ทธ๋ ์ด์ ์คํจํ ๋ด์ญ์ ์์ ํ๋ค (์ญ์ , ๊ต์ฒด)
* baseline - flyway๋ก ํ์ ๋ฒ์ ๊ด๋ฆฌ๋ฅผ ์์ ํ  baseline ์ ์ค์ ํ๋ค.
