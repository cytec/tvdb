# tvdb [![CircleCI](https://circleci.com/gh/danesparza/tvdb.svg?style=svg)](https://circleci.com/gh/danesparza/tvdb)
TVDB v2.0 API wrapper for Go

## Example
Be sure to `go get github.com/danesparza/tvdb` and then import the package in your code first

``` Go
// Create a client and search request
client := tvdb.Client{}
request := tvdb.SeriesEpisodesRequest{Name: "Looney Tunes"}

// Search for the series
responses, err := client.SeriesSearch(request)

// Loop through the TV series information in the resopnse:
for _, response := range responses {
  fmt.Printf("Series name: %v", response.SeriesName)
}
  
```

This should print:
```
Series name: Looney Tunes
Series name: The Looney Tunes Show (2011)
Series name: ** 403: Series Not Permitted **
Series name: Baby Looney Tunes
```
