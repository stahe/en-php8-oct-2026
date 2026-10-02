# Introduction to PHP 8 Through Examples

📖 **Read the tutorial: [https://stahe.github.io/en-php8-oct-2026/](https://stahe.github.io/en-php8-oct-2026/)**

This course teaches the [PHP](https://www.php.net) 8.5 language **through examples**: over 300 PHP files, commented line by line, with their execution results reproduced. It starts with the basics of the language and progresses to web services and an MVC web application.

This is a rewrite for PHP 8 of the course [Introduction to PHP 7 Through Examples](https://stahe.github.io/en-php7-juillet-2019/) (2019): same outline, same examples, same overarching theme, but with up-to-date code. Between PHP 7 and PHP 8.5, many features have become **deprecated**: the code in this course uses **none** of them. All scripts were run with PHP 8.5 configured to report everything (`error_reporting = E_ALL`): no `Deprecated` messages appear in their output.

| PHP 7 Course (2019) | PHP 8 Course (2026) |
|---|---|
| PHP 7.3 | PHP 8.5 |
| NetBeans | VS Code + PHP Intelephense |
| Codeception | PHPUnit 12 |
| Postman | curl |
| SwiftMailer, hMailServer | Symfony Mailer, Mailpit |
| `imap_*` functions (removed from the PHP core in 8.4) | POP3/IMAP clients written using sockets |
| dynamic properties, getters/setters | typed properties, `readonly`, constructor parameter promotion |
| `switch`, class constants | `match`, enumerations (`enum`) |
| `PDO::MYSQL_ATTR_*` (deprecated in 8.5) | `PDO::connect()`, `Pdo\Mysql`, `Pdo\Pgsql` |
| `deny from all` (Apache 2.2) | a `public/` directory and `Require all denied` (Apache 2.4) |

## Course Outline

| Chapter | Content |
|---|---|
| Installation | Laragon 8 (PHP 8.5, Apache, MySQL, PostgreSQL, Redis), VS Code, Composer |
| PHP Basics | variables, strict typing, arrays, strings, functions (named arguments, `match`, arrow functions, PHP 8.5 pipe operator `\|>`), text files, JSON |
| Classes, Interfaces | typed attributes, constructor promotion, `readonly`, property brackets and asymmetric visibility (PHP 8.4), enumerations, `#[\Override]`, `clone` with modifications (PHP 8.5), intersection types |
| Exceptions and errors | the `Throwable` hierarchy in PHP 8, PHP 7 warnings converted to exceptions |
| Traits, layered applications | code reuse; [DAO] / [business logic] / [console] architecture |
| Testing | PHPUnit 12: data providers via attributes, expected exceptions |
| Databases | PDO with MySQL 8 and PostgreSQL: prepared statements, transactions |
| Network functions | TCP, HTTP, SMTP, POP3, IMAP, implemented using sockets and then using libraries |
| Web services | dynamic pages, JSON, GET/POST parameters, sessions, authentication, HTTPS |
| XML | SimpleXML and the new `Dom\XMLDocument` API in PHP 8.4 |

## The Common Thread: An Income Tax Calculator in 13 Versions

Throughout the course, version by version, we build an **income tax calculator**:

- **versions 1 and 2**: a script, functions, text files, and JSON;
- **version 3**: classes; **version 4**: a layered architecture, tested with PHPUnit;
- **versions 5 through 7**: tax data in a MySQL database, then PostgreSQL, then either one;
- **versions 8 through 11**: a web service and its console client: authentication, sessions, logging, email notifications to the administrator in case of errors, Redis cache, responses in JSON and then XML;
- **version 12**: an **MVC** web application that returns responses in JSON, XML, or HTML (Bootstrap 5), with a console client for the JSON service;
- **Version 13**: Application file security (only the `public/` folder is visible from the web).



## Technologies

PHP 8.5 · Apache 2.4 · MySQL 8.4 · PostgreSQL · Redis · Composer · PHPUnit 12 · Symfony HttpFoundation 8 · Symfony HttpClient 8 · Symfony Mailer 8 · Predis 3 · zbateson/mail-mime-parser 3 · Mailpit · Bootstrap 5 · Laragon 8 · VS Code

## Prerequisites

- Previous programming experience in any language.
- Windows and [Laragon](https://laragon.org) 8 (which includes PHP 8.5, Apache, MySQL, PostgreSQL, Redis, and Composer), [VS Code](https://code.visualstudio.com), and its PHP IntelliSense extension. Installation instructions are provided at the beginning of the course.

## Author

This course and its code were written by **Claude**, the AI from [Anthropic](https://www.anthropic.com) (October 2026), at the request of Serge Tahé, based on his 2019 PHP 7 course.
