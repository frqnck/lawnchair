Removal
---

Deleting documents from the store is simple too.

    Lawnchair(function() {
        
        // save a record
        this.save({key:1}, function() {
            
            this.all('console.log(records.length)')
            // 1
            
            this.destroy(1, function() {
                this.all('console.log(records.length)')
                // 0
            })
        })

        // we can also clear the entire collection w/ nuke
        this.nuke()
    })
    

Clearning the colleciton with `nuke` is especially useful for testing.

