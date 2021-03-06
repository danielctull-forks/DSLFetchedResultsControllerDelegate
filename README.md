DSLFetchedResultsControllerDelegate
===================================

A simple class to take the chore out of implementing NSFetchedResultsControllerDelegates.

To use it, create an instance with either a `UITableView` or `UICollectionView` and set it as the delegate of your `NSFetchedResultsController`.

```Objective-C
self.myFetchedResultsControllerDelegate = [[DSLFetchedResultsControllerDelegate alloc] initWithCollectionView:self.collectionView];
self.myFetchedResultsController = [[NSFetchedResultsController alloc] initWithFetchRequest:fetchRequest managedObjectContext:context sectionNameKeyPath:nil cacheName:nil];
self.myFetchedResultsController.delegate = self.myFetchedResultsControllerDelegate;
```

This is based on the workarounds documented by [Michael Fey](https://github.com/MrRooni)'s article "[UITableview and NSFetchedResultsController updates done right](http://www.fruitstandsoftware.com/blog/2013/02/uitableview-and-nsfetchedresultscontroller-updates-done-right/)".
