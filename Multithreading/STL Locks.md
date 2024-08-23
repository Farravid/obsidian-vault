
# std::unique_lock

This can be useful when you want to be able to unlock / lock a mutex. 
Ideally you only need to hold a mutex as few as you can for performance shake

If not use std::lock_guard or std::scoped_lock


# std::lock_guard vs std::scoped_lock
Esentially they are the same but scoped lock supports variadic templates so you can mute from 0 to N mutexes at the same time.




