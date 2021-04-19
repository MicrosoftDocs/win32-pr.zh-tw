---
description: Gethostbyaddr 函式會使用 WSALookupServiceBegin 函數，將 SVCID \_ INET \_ HOSTNAMEBYADDR 查詢為服務類別 GUID。
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: API 中的 gethostbyaddr 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999856"
---
# <a name="gethostbyaddr-function-in-the-api"></a><span data-ttu-id="e668b-103">API 中的 gethostbyaddr 函式</span><span class="sxs-lookup"><span data-stu-id="e668b-103">gethostbyaddr Function in the API</span></span>

<span data-ttu-id="e668b-104">[**Gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)函式會使用 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)函數，將 SVCID \_ INET \_ HOSTNAMEBYADDR 查詢為服務類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="e668b-104">The [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="e668b-105">主機位址是以點 decimnal IPv4 字串的形式提供 (例如，"192.9.200.120" ) 在傳遞給 **WSALookupServiceBegin** 函數的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構的 *lpszServiceInstanceName* 成員中。</span><span class="sxs-lookup"><span data-stu-id="e668b-105">The host address is supplied as a dotted decimnal IPv4 string (for example, "192.9.200.120") in the *lpszServiceInstanceName* member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="e668b-106">Ws2 \_32.dll 會指定 LUP \_ 傳回 \_ blob，而且名稱服務提供者會使用位移來將 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) 結構放在 BLOB (，而不是上述) 所述的指標。</span><span class="sxs-lookup"><span data-stu-id="e668b-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="e668b-107">名稱服務提供者也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。</span><span class="sxs-lookup"><span data-stu-id="e668b-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span> 

| <span data-ttu-id="e668b-108">旗標</span><span class="sxs-lookup"><span data-stu-id="e668b-108">Flag</span></span>              | <span data-ttu-id="e668b-109">描述</span><span class="sxs-lookup"><span data-stu-id="e668b-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e668b-110">LUP \_ 傳回 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="e668b-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="e668b-111">從 *lpszServiceInstanceName* 中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構傳回 **h \_ 名稱** 成員。</span><span class="sxs-lookup"><span data-stu-id="e668b-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="e668b-112">LUP \_ 傳回 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="e668b-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="e668b-113">從 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)傳回定址資訊，埠資訊預設為零。</span><span class="sxs-lookup"><span data-stu-id="e668b-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e668b-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="e668b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e668b-115">Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析</span><span class="sxs-lookup"><span data-stu-id="e668b-115">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="e668b-116">通訊協定獨立名稱解析</span><span class="sxs-lookup"><span data-stu-id="e668b-116">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="e668b-117">註冊和名稱解析</span><span class="sxs-lookup"><span data-stu-id="e668b-117">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
