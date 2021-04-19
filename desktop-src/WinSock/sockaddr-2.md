---
description: Sockaddr 結構會根據選取的通訊協定而有所不同。
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
title: sockaddr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sockaddr
api_type:
- NA
api_location: ''
ms.openlocfilehash: ccd4b98efc987630ab625e5c9788f0be16018e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982357"
---
# <a name="sockaddr"></a>sockaddr

Sockaddr 結構會根據選取的通訊協定而有所不同。 除了 *sin \* \_ 系列* 參數之外，sockaddr 內容會以網路位元組順序表示。

使用 sockaddr 的 Winsock 函式不會嚴格地解讀為 sockaddr 結構的指標。 結構在不同的位址系列內容中會以不同的方式轉譯。 唯一的需求是，第一個 **u \_ 短** 是位址系列，而記憶體緩衝區的大小總計（以位元組為單位）為 *>namelen*。

[**SOCKADDR \_ 儲存體**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))結構也會儲存通訊端位址資訊，而且結構夠大，足以儲存 IPv4 或 IPv6 位址資訊。 使用 **SOCKADDR \_ 儲存體** 結構可提升通訊協定系列和通訊協定版本的獨立性，並簡化開發。 建議使用 **SOCKADDR \_ 儲存體** 結構來取代 SOCKADDR 結構。 Windows Server 2003 和更新版本支援 **SOCKADDR \_ 儲存體** 結構。

下列結構中的 sockaddr 結構和 sockaddr \_ 會搭配 IPv4 使用。 其他通訊協定使用類似的結構。

``` syntax
struct sockaddr {
        ushort  sa_family;
        char    sa_data[14];
};

struct sockaddr_in {
        short   sin_family;
        u_short sin_port;
        struct  in_addr sin_addr;
        char    sin_zero[8];
};
```

下列 sockaddr \_ in6 和 sockaddr \_ in6 \_ 舊結構會搭配 IPv6 使用。

``` syntax
struct sockaddr_in6 {
        short   sin6_family;
        u_short sin6_port;
        u_long  sin6_flowinfo;
        struct  in6_addr sin6_addr;
        u_long  sin6_scope_id;
};

typedef struct sockaddr_in6 SOCKADDR_IN6;
typedef struct sockaddr_in6 *PSOCKADDR_IN6;
typedef struct sockaddr_in6 FAR *LPSOCKADDR_IN6;


struct sockaddr_in6_old {
        short   sin6_family;        
        u_short sin6_port;          
        u_long  sin6_flowinfo;      
        struct  in6_addr sin6_addr;  
};
```

在 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 上，typedef 標記 **\_ 中** 的 **SOCKADDR** 和 SOCKADDR 會針對結構中的 SOCKADDR 和 SOCKADDR 定義，如下所示 \_ ：

``` syntax
typedef struct sockaddr {
#if (_WIN32_WINNT < 0x0600)
    u_short sa_family;
#else 
    ADDRESS_FAMILY sa_family;
#endif //(_WIN32_WINNT < 0x0600)
    CHAR sa_data[14];
} SOCKADDR, *PSOCKADDR, FAR *LPSOCKADDR;


typedef struct sockaddr_in {
#if(_WIN32_WINNT < 0x0600)
    short   sin_family;    
#else //(_WIN32_WINNT < 0x0600)
    ADDRESS_FAMILY sin_family;
#endif //(_WIN32_WINNT < 0x0600)
    USHORT sin_port;
    IN_ADDR sin_addr;
    CHAR sin_zero[8];
} SOCKADDR_IN, *PSOCKADDR_IN;
```

在 Windows Vista 和更新版本的 Windows SDK 發行時，標頭檔的組織已經變更，而結構中的 sockaddr 和 sockaddr \_ 是在 *Ws2def .h* 標頭檔中定義，而不是在 *Winsock2* 標頭檔中定義。 *Ws2def. h* 標頭檔會自動包含在 *Winsock2* 標頭檔中。 Sockaddr \_ in6 結構定義于 *Ws2ipdef .h* 標頭檔中，而不是 *Ws2tcpip .h* 標頭檔中。 *Ws2ipdef .h* 標頭檔會自動包含在 *Ws2tcpip .h* 標頭檔中。 不應直接使用 *Ws2def .h* 和 *Ws2ipdef* 標頭檔。

## <a name="example-code"></a>範例程式碼

下列範例示範如何使用 **sockaddr** 結構。


```C++

// Declare variables
SOCKET ListenSocket;
struct sockaddr_in saServer;
hostent* localHost;
char* localIP;

// Create a listening socket
ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);

// Get the local host information
localHost = gethostbyname("");
localIP = inet_ntoa (*(struct in_addr *)*localHost->h_addr_list);

// Set up the sockaddr structure
saServer.sin_family = AF_INET;
saServer.sin_addr.s_addr = inet_addr(localIP);
saServer.sin_port = htons(5150);

// Bind the listening socket using the
// information in the sockaddr structure
bind( ListenSocket,(SOCKADDR*) &saServer, sizeof(saServer) );


```



## <a name="see-also"></a>另請參閱

[**SOCKADDR \_ 儲存體**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))


 

 
