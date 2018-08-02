# Geek Night API Spec

## Json Objects returned by API:

### Song (Simple)

```json
{
    "id": 1,
    "title": "My Favorite Song",
    "duration": "00:03:30",
    "isExplicit": false,
    "isFavorite": true
}
```

### Song (Detailed)

```json
{
    "id": 1,
    "title": "My Favorite Song",
    "duration": "00:03:30",
    "isExplicit": false,
    "isFavorite": true,
    "album": {
        "id": 3,
        "title": "Album Title",
        "artistId": {
            "id": 2,
            "name": "Artist Name",
            "genre": {
                "id": 5,
                "name": "Nu-Ironic Transcendental Banjo Electronica"
            },
            "monthlyListeners": 2,
            "following": true,
        },
        "genre": {
            "id": 4,
            "name": "Meh Pop",
        },
        "duration": "00:04:32",
        "isExplicit": false,
        "isFavorite": true
    }
}
```

### Artist

```json
{
    "id": 2,
    "name": "Artist",
    "genre": {
        "id": 5,
        "name": "Nu-Ironic Transcendental Banjo Electronica"
    },
    "monthlyListeners": 2,
    "following": true,
}
```

### Album

```json
{
    "id": 3,
    "title": "Title",
    "artistId": 3,
    "genre": {
        "id": 4,
        "name": "Meh Pop",
    },
    "duration": "00:04:32",
    "isExplicit": false,
    "isFavorite": true,
}
```

### Genre

```json
{
    "id": 4,
    "name": "Meh Pop",
}
```

### Playlist

```json
{
    "id": 4,
    "title": "Cool Tunes for Cool Dudes",
    "createdBy": "CoolDude99x",
    "createdOn": "2018-08-02 12:20:34",
    "numSongs": 50,
    "totalDuration": "04:55:00"
}
```

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
Get all albums created by artist | `GET /artist/:artistId/albums`
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
Get all albums by genre | `GET /genre/:genreId/albums`
Get all artists by genre | `GET /genre/:genreId/artists`

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