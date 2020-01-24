# Thoth websocket example.

This example sends a file (log file or json file) to the browser client for display whenever the file is modified.

    $ go get github.com/gorilla/websocket
    $ cd `code dir`
    $ go run main.go <name of file to watch>
    # Open http://localhost:8080/ .
    # Modify the file to see it update in the browser.

***The basic idea is to make this example a method under the thoth package, so users can basically add something like thoth.watch('logfilename') in their main function, then that call adds a http.HandleFunc('/thothlog',func(){do logic here}, then they can access their logs via that endpoint.)***