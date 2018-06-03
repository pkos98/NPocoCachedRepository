This repository implementation provides basic CRUD operations on a database using NPoco. 
It caches all changes until you explicitly save them to the db!

>Usage:  
```
var repo = new CachedRepositoryBase<MovieModel>(db);
// CRUD operations
repo.Add(lotrPartOne);
repo.Remove(gotS01E01);
repo.Update(siliconValleyS01E01);
var allMovies = repo.GetAll();
// Apply changes to db!
repo.Save();

// Aboort changes => Rollback!
repo.Remove(siliconValleyS01E02);
repo.Rollback();
```

>Dependencies:
* NPoco