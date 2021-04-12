---
description: 檢查函式失敗時，會提供資訊清單常數通訊端 \_ 錯誤。 雖然使用此常數並非強制的，但建議使用。 下列範例說明如何使用通訊端 \_ 錯誤常數。
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: 函數失敗時傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94280d47d705833528c03c0d98a4a31232a0c6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192091"
---
# <a name="return-values-on-function-failure"></a><span data-ttu-id="9588e-105">函數失敗時傳回值</span><span class="sxs-lookup"><span data-stu-id="9588e-105">Return Values on Function Failure</span></span>

<span data-ttu-id="9588e-106">檢查函式失敗時，會提供資訊清單常數 **通訊端 \_ 錯誤** 。</span><span class="sxs-lookup"><span data-stu-id="9588e-106">The manifest constant **SOCKET\_ERROR** is provided for checking function failure.</span></span> <span data-ttu-id="9588e-107">雖然使用此常數並非強制的，但建議使用。</span><span class="sxs-lookup"><span data-stu-id="9588e-107">Although use of this constant is not mandatory, it is recommended.</span></span> <span data-ttu-id="9588e-108">下列範例說明如何使用 **通訊端 \_ 錯誤** 常數。</span><span class="sxs-lookup"><span data-stu-id="9588e-108">The following example illustrates the use of the **SOCKET\_ERROR** constant.</span></span>

<span data-ttu-id="9588e-109">一般的 BSD 樣式 (將無法在 Windows 上運作) </span><span class="sxs-lookup"><span data-stu-id="9588e-109">Typical BSD Style (will not work on Windows)</span></span>


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



<span data-ttu-id="9588e-110">Windows 樣式</span><span class="sxs-lookup"><span data-stu-id="9588e-110">Windows Style</span></span>


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a><span data-ttu-id="9588e-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="9588e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9588e-112">錯誤碼-errno、h \_ errno 和 WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="9588e-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[<span data-ttu-id="9588e-113">處理 Winsock 錯誤</span><span class="sxs-lookup"><span data-stu-id="9588e-113">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="9588e-114">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="9588e-114">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="9588e-115">Winsock 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="9588e-115">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="9588e-116">Windows 通訊端錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9588e-116">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



