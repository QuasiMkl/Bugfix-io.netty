# Bugfix-io.netty (Unknown Source)
### Server端出現以下錯誤:
`NetworkDispatcher exception io.netty.channel.unix.Errors$NativeIoException: syscall:write(..) failed: Broken pipe`
`at io.netty.channel.unix.FileDescriptor.writeAddress(..)(Unknown Source) ~[minecraft_server.1.12.2.jar:?]`
### 以下錯誤修正步驟:
1.下載最新的`netty`完整軟件包API: https://netty.io/

2.打開服務器jar`minecraft_server.1.12.2.jar`進入到`minecraft_server.1.12.2.jar\io\netty\`

3.打開剛才下載的`netty api`，進入到`netty-4.1.37.Final.tar.bz2\netty-4.1.37.Final.tar\netty-4.1.37.Final\jar\all-in-one\netty-all-4.1.37.Final.jar\io\netty\`

4.刪除`minecraft_server.1.12.2.jar`裡的`handler``channel``util``buffer``resolver``bootstrap`資料夾

5.然後再將`netty api`裡的`handler``channel``util``buffer``resolver``bootstrap`資料夾，複製到`minecraft_server.1.12.2.jar`裡面

6.完成了!!

### 更新netty版本可以解決一下的問題:
`NetworkDispatcher exception io.netty.channel.unix.Errors$NativeIoException: syscall:writev(…) failed: Broken pipe`
