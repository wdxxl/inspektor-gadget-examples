

2. 参考案例 https://github.com/inspektor-gadget/inspektor-gadget/blob/main/examples/gadgets/withfilter/trace/exec/exec.go

```
go mod tidy -compat=1.17
go mod vendor
```

```
go build .
```

Terminal 1:
```bash
sudo ./exec --container name foo
```

Terminal 2:
```bash
sudo docker run --rm --name foo ubuntu bash -c "cat /dev/null && sleep 2"
```

