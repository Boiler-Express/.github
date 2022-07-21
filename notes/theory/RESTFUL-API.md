# 🐌 RESTful API

RESTful API is some kind of [API](https://github.com/Boiler-Express/.github/blob/main/notes/theory/API.md)

## What is REST?

REST is abbreviation of `Representational State Transfer`.

This is a common known method to Communication Rules between Client and Server.

Client can comminucate `URI` and `METHOD`.

- URI : basically people know `URL`.
- METHOD : basically people don't know, default value is `GET`

### Base

> Basically, you can run Application in your PC.<br>
> And then, default URL looks like `http://localhost:PORT/`.<br>
> In the foward, all URl start with default URL.<br>
> So, if you slice default string, you could receive '/'<br>

### Collection

If some URL return movies data, server URL looks like `/movies`.<br>
If some URL return cats data, server URL looks like `/cats`.

Collection means keyword of Return Object.<br>

#### General Rules of Collection Name

- Use Singular Word ( movie o / movies x )
- Use Lowercase Word ( movie o / MOVIE x / Movie x )
- Use '-' for blank space ( movie-theater o / movie theater x / movie)

If you want to more detail, please googling.

### Method

If some URL return movies data, you should set METHOD = `GET`. <br>
If some URL create movie data, you should set METHOD = `POST` <br>

Method menas What will you do with Colleciton?

#### General Methods

- `GET` : should return Collection
- `POST` : should create Colleciton
- `PUT` : should update Collection, and then Not-Include Key-Value will be removed.
- `PATCH` : should update Collection, and then Not-Include key-Value will be not-removed.
- `DELETE` : should delete Collection

