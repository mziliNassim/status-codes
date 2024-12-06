# Comprehensive table for all the HTTP status codes:

## 1xx Informational

| Code | Message             | Signification                                                                            |
| ---- | ------------------- | ---------------------------------------------------------------------------------------- |
| 100  | Continue            | The client should continue with its request.                                             |
| 101  | Switching Protocols | The server is switching protocols as requested by the client.                            |
| 102  | Processing          | The server has received and is processing the request, but no response is available yet. |
| 103  | Early Hints         | Indique que le serveur est prêt à envoyer les en-têtes de réponse préliminaires.         |

## 2xx Success

| Code | Message                       | Signification                                                                                                                                                                      |
| ---- | ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 200  | OK                            | Request has succeeded. The meaning of a success varies depending on the HTTP method: GET, POST, etc.                                                                               |
| 201  | Created                       | The request has been fulfilled and resulted in a new resource being created.                                                                                                       |
| 202  | Accepted                      | The request has been accepted for processing, but the processing has not been completed.                                                                                           |
| 203  | Non-Authoritative Information | The request has been successfully processed, but is returning information that may be from another source.                                                                         |
| 204  | No Content                    | The server successfully processed the request and is not returning any content.                                                                                                    |
| 205  | Reset Content                 | The server successfully processed the request and is not returning any content, but requires the requester to reset the document view.                                             |
| 206  | Partial Content               | The server is delivering only part of the resource due to a range header sent by the client.                                                                                       |
| 207  | Multi-Status                  | The message body that follows is an XML message and can contain a number of separate response codes.                                                                               |
| 208  | Already Reported              | The members of a DAV binding have already been enumerated in a previous reply to this request, and are not being included again.                                                   |
| 226  | IM Used                       | The server has fulfilled a GET request for the resource, and the response is a representation of the result of one or more instance-manipulations applied to the current instance. |

## 3xx Redirection

| Code | Message            | Signification                                                                                                              |
| ---- | ------------------ | -------------------------------------------------------------------------------------------------------------------------- |
| 300  | Multiple Choices   | There are multiple options for the resource that the client may follow.                                                    |
| 301  | Moved Permanently  | The requested resource has been assigned a new permanent URI.                                                              |
| 302  | Found              | The requested resource resides temporarily under a different URI.                                                          |
| 303  | See Other          | The response to the request can be found under another URI.                                                                |
| 304  | Not Modified       | Indicates that the resource has not been modified since the version specified by the request headers.                      |
| 305  | Use Proxy          | The requested resource is available only through a proxy, whose address is provided in the response.                       |
| 306  | (Unused)           | This code was used in a previous version of the HTTP/1.1 specification but is no longer used.                              |
| 307  | Temporary Redirect | In this case, the request should be repeated with another URI; however, future requests should still use the original URI. |
| 308  | Permanent Redirect | The request and all future requests should be repeated using another URI.                                                  |

## 4xx Client Errors

| Code | Message                         | Signification                                                                                                                               |
| ---- | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| 400  | Bad Request                     | The server could not understand the request due to invalid syntax.                                                                          |
| 401  | Unauthorized                    | The client must authenticate itself to get the requested response.                                                                          |
| 402  | Payment Required                | This code is reserved for future use.                                                                                                       |
| 403  | Forbidden                       | The client does not have access rights to the content.                                                                                      |
| 404  | Not Found                       | The server can not find the requested resource.                                                                                             |
| 405  | Method Not Allowed              | The request method is known by the server but has been disabled and cannot be used.                                                         |
| 406  | Not Acceptable                  | The server cannot produce a response matching the list of acceptable values defined in the request's proactive content negotiation headers. |
| 407  | Proxy Authentication Required   | The client must first authenticate itself with the proxy.                                                                                   |
| 408  | Request Timeout                 | The server would like to shut down this unused connection.                                                                                  |
| 409  | Conflict                        | The request conflicts with the current state of the server.                                                                                 |
| 410  | Gone                            | The requested content has been permanently deleted from the server, with no forwarding address.                                             |
| 411  | Length Required                 | The server rejects the request because the Content-Length header field is not defined and the server requires it.                           |
| 412  | Precondition Failed             | The client has indicated preconditions in its headers which the server does not meet.                                                       |
| 413  | Payload Too Large               | The request entity is larger than limits defined by server.                                                                                 |
| 414  | URI Too Long                    | The URI requested by the client is longer than the server is willing to interpret.                                                          |
| 415  | Unsupported Media Type          | The media format of the requested data is not supported by the server.                                                                      |
| 416  | Range Not Satisfiable           | The range specified by the Range header field in the request cannot be fulfilled.                                                           |
| 417  | Expectation Failed              | The expectation given in the request's Expect header could not be met by at least one of the inbound servers.                               |
| 418  | I'm a teapot                    | The server refuses the attempt to brew coffee with a teapot.                                                                                |
| 421  | Misdirected Request             | The request was directed at a server that is not able to produce a response.                                                                |
| 422  | Unprocessable Entity            | The request was well-formed but was unable to be followed due to semantic errors.                                                           |
| 423  | Locked                          | The resource that is being accessed is locked.                                                                                              |
| 424  | Failed Dependency               | The request failed due to failure of a previous request.                                                                                    |
| 425  | Too Early                       | Indicates that the server is unwilling to risk processing a request that might be replayed.                                                 |
| 426  | Upgrade Required                | The client should switch to a different protocol.                                                                                           |
| 428  | Precondition Required           | The origin server requires the request to be conditional.                                                                                   |
| 429  | Too Many Requests               | The user has sent too many requests in a given amount of time.                                                                              |
| 431  | Request Header Fields Too Large | The server is unwilling to process the request because its header fields are too large.                                                     |
| 451  | Unavailable For Legal Reasons   | The user requested a resource that cannot legally be provided.                                                                              |

## 5xx Server Errors

| Code | Message                         | Signification                                                                                                                 |
| ---- | ------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| 500  | Internal Server Error           | The server has encountered a situation it doesn't know how to handle.                                                         |
| 501  | Not Implemented                 | The request method is not supported by the server and cannot be handled.                                                      |
| 502  | Bad Gateway                     | The server, while working as a gateway to get a response needed to handle the request, got an invalid response.               |
| 503  | Service Unavailable             | The server is not ready to handle the request. Common causes are a server that is down for maintenance or that is overloaded. |
| 504  | Gateway Timeout                 | The server is acting as a gateway and cannot get a response in time.                                                          |
| 505  | HTTP Version Not Supported      | The HTTP version used in the request is not supported by the server.                                                          |
| 506  | Variant Also Negotiates         | The server has an internal configuration error.                                                                               |
| 507  | Insufficient Storage            | The server is unable to store the representation needed to complete the request.                                              |
| 508  | Loop Detected                   | The server detected an infinite loop while processing a request.                                                              |
| 510  | Not Extended                    | Further extensions to the request are required for the server to fulfill it.                                                  |
| 511  | Network Authentication Required | The client needs to authenticate to gain network access.                                                                      |

This should cover all the standard HTTP status codes along with their messages and meanings. If you need more details or specific codes, feel free to ask!
