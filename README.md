# {App} API Spec

## Endpoints:

### Song

Operation | Endpoint
---|---
Get all songs | `GET /song`
Get one song | `GET /song/:songId`
Create a new song | `POST /song`
Update a song | `PUT /song/:songId`
Remove a song | `DELETE /song/:songId`
Favorite a song | `POST /song/:songId/favorite`
Un-Favorite a song | `DELETE /song/:songId/favorite`

### Artist

Operation | Endpoint
---|---
Get all artists | `GET /artist`
Get one artist | `GET /artist/:artistId`
Create a new artist | `POST /artist`
Update an artist | `PUT /artist/:artistId`
Remove an artist | `DELETE /artist/:artistId`
Get all songs created by artist | `GET /artist/:artistId/songs`
Follow an artist | `POST /artist/:artistId/follow`
Un-Follow an artist | `DELETE /artist/:artistId/follow`

### Genre

Operation | Endpoint
---|---
Get all genres | `GET /genre`
Get one genre | `GET /genre/:genreId`
Create a new genre | `POST /genre`
Update a genre | `PUT /genre/:genreId`
Remove a genre | `DELETE /genre/:genreId`

### Album

Operation | Endpoint
---|---
Get all albums | `GET /album`
Get one album | `GET /album/:albumId`
Create a new album | `POST /album`
Update an album | `PUT /album/:albumId`
Remove an album | `DELETE /album/:albumId`
Get all songs in an album | `GET /album/:albumId/songs`

### Playlist

Operation | Endpoint
---|---
Get all playlists | `GET /playlist`
Get one playlist | `GET /playlist/:playlistId`
Create a new playlist | `POST /playlist`
Update a playlist | `PUT /playlist/:playlistId`
Delete a playlist | `DELETE /playlist/:playlistId`
Get all songs in a playlist | `GET /playlist/:playlistId/songs`
Add a song to a playlist | `POST /playlist/:playlistId/:songId`
Remove a song from a playlist | `DELETE /playlist/:playlistId/:songId`