## Idea: AVL tree database using file system structure and symlinks to index data
* language: C#?
* every folder has a "left" and "right" folder, which are just the alphabetical* order of the folder names.
  * not entirely alphabetical, as 2 has to come before 10, example python: `from natsort import natsorted`
  * tables/movie/director/row/2/1/name.string:Jack Nicholson
* Should there also be a symlink to the next folder? because resultSet.next() is needed?
```
     db
    table
    movie
actor   director
            2
           1 3
       name.string255, .next.folderlink
```

* create index: creates symlinks that are based on columns, which creates a folder structure of that column
  * index/actor.name/jack nicholson/symlink.symlink
  * index/director.name/quentin tarantino/steven spielberg/symlink.symlink

* full text search?
  * index/all.strings/jack nicholson/notting hill/symlink.symlink

## SQL minimum feature set
* simple select query
* update data
* delete data
* create table
* create index

## Then, create a jdbc driver and test it

## Step 2
* joins
* subselects
* 
