
## gson benchmark

It's a fork of ajson's benches to focus on perfmance benchmarks only.

## Performance

`$ cargo bench`

* [ajson](https://github.com/importcjj/ajson)
* [gjson](https://github.com/tidwall/gjson.rs)
* [serde_json](https://github.com/serde-rs/json)
* [rust-json](https://github.com/maciejhirsz/json-rust)

```
ajson benchmark         time:   [9.1979 us 9.2489 us 9.3066 us]
                        change: [-10.706% -9.1719% -7.6992%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 2 outliers among 100 measurements (2.00%)
  2 (2.00%) high mild

gjson benchmark         time:   [3.6221 us 3.6413 us 3.6623 us]
                        change: [-15.350% -12.966% -10.873%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 6 outliers among 100 measurements (6.00%)
  3 (3.00%) high mild
  3 (3.00%) high severe

serde_json benchmark    time:   [59.616 us 59.876 us 60.162 us]
                        change: [-14.793% -12.771% -10.900%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 9 outliers among 100 measurements (9.00%)
  1 (1.00%) low mild
  2 (2.00%) high mild
  6 (6.00%) high severe

json-rust benchmark     time:   [29.568 us 29.729 us 29.894 us]
                        change: [-15.512% -14.014% -12.561%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 5 outliers among 100 measurements (5.00%)
  1 (1.00%) low mild
  3 (3.00%) high mild
  1 (1.00%) high severe

ajson selector          time:   [3.0875 us 3.1000 us 3.1139 us]
                        change: [-11.651% -10.079% -8.4826%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 5 outliers among 100 measurements (5.00%)
  5 (5.00%) high mild

gjson selector          time:   [2.0724 us 2.0882 us 2.1050 us]
                        change: [-5.7071% -3.8407% -1.9520%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 4 outliers among 100 measurements (4.00%)
  4 (4.00%) high severe

ajson multi query       time:   [2.6245 us 2.6365 us 2.6492 us]
                        change: [-9.4889% -8.3135% -7.1778%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 9 outliers among 100 measurements (9.00%)
  1 (1.00%) low mild
  5 (5.00%) high mild
  3 (3.00%) high severe

gjson multi query       time:   [858.23 ns 861.61 ns 865.37 ns]
                        change: [-10.479% -8.6397% -6.8407%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 5 outliers among 100 measurements (5.00%)
  3 (3.00%) high mild
  2 (2.00%) high severe

serde derive            time:   [9.1830 us 9.2368 us 9.2964 us]
                        change: [-10.407% -8.5730% -6.7286%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 5 outliers among 100 measurements (5.00%)
  4 (4.00%) high mild
  1 (1.00%) high severe

serde derive multi query
                        time:   [1.9318 us 1.9421 us 1.9542 us]
                        change: [-5.3005% -4.0650% -2.8234%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 3 outliers among 100 measurements (3.00%)
  3 (3.00%) high mild

nom json bench          time:   [1.2689 us 1.2735 us 1.2783 us]
                        change: [-4.7747% -3.7796% -2.8171%] (p = 0.00 < 0.05)
                        Performance has improved.
Found 5 outliers among 100 measurements (5.00%)
  2 (2.00%) high mild
  3 (3.00%) high severe


```

* MacBook Pro (Retina, 15-inch, Mid 2015)
* 2.2 GHz Quad-Core Intel Core i7
* 16 GB 1600 MHz DDR3