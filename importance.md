

## Why adding jalali calander to `glibc` important.


We have many distinct programs that implements jalali(shamsi) in GNU. The underlying system don't understand this calendar.
If glibc is aware about that all applications runs on top of it will invest by using shamsi calendar natively.

Any updates will affects all of them and besides that this is a huge breakthrough in support of Persian language.

But `glibc` is a complicated package. Contribution is hard.

If its not possible use alternatives musl and uc.
