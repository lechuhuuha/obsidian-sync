phân biệt rõ ràng use case, mục đích sử dụng của proxy_listen/ và stream_listen https://docs.konghq.com/gateway/3.7.x/reference/configuration/#proxy_listen
1. proxy_listen có yêu cầu define ssl để chỉ định địa chỉ đó handle SSL hay không ? Nếu không define ssl thì có handle được request SSL ? 
2. stream_listen có yêu cầu define ssl để chỉ định địa chỉ đó handle SSL hay không ? Nếu không define ssl thì có handle được request SSL ?
3. Có phải proxy_listen ở đây ám chỉ HTTP Proxy còn stream_listen là TCP UDP proxy ?
4. Tại saoa anh có câu hỏi vậy. Nếu như phải define sẵn port xử lý traffic SSL, port nào không. Thì 1 port đã được define là SSL thì chỉ có thể routing SSL thôi. Nó ảnh hưởng đến thiết kế của mình