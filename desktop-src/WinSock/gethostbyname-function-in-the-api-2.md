---
description: Winsock API 中的 Gethostbyname 函式。
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: API 中的 gethostbyname 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113076"
---
# <a name="gethostbyname-function-in-the-api"></a><span data-ttu-id="ea69a-103">API 中的 gethostbyname 函式</span><span class="sxs-lookup"><span data-stu-id="ea69a-103">gethostbyname Function in the API</span></span>

<span data-ttu-id="ea69a-104">[**Gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)函式會使用 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)函數，將 SVCID \_ INET \_ HOSTADDRBYNAME 查詢為服務類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="ea69a-104">The [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="ea69a-105">在傳遞給 **WSALookupServiceBegin** 函式的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構中， **lpszServiceInstanceName** 成員會提供主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ea69a-105">The host name is supplied in the **lpszServiceInstanceName** member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="ea69a-106">Ws2 \_32.dll 會指定 LUP \_ 傳回 \_ blob，而且名稱服務提供者會使用位移來將 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) 結構放在 BLOB (，而不是上述) 所述的指標。</span><span class="sxs-lookup"><span data-stu-id="ea69a-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="ea69a-107">名稱服務提供者也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。</span><span class="sxs-lookup"><span data-stu-id="ea69a-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="ea69a-108">旗標</span><span class="sxs-lookup"><span data-stu-id="ea69a-108">Flag</span></span>              | <span data-ttu-id="ea69a-109">描述</span><span class="sxs-lookup"><span data-stu-id="ea69a-109">Description</span></span>                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea69a-110">LUP \_ 傳回 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="ea69a-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="ea69a-111">從 *lpszServiceInstanceName* 中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構傳回 **h \_ 名稱** 成員。</span><span class="sxs-lookup"><span data-stu-id="ea69a-111">Returns the **h\_name** member from the [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                           |
| <span data-ttu-id="ea69a-112">LUP \_ 傳回 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="ea69a-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="ea69a-113">從 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)傳回定址資訊，埠資訊預設為零。</span><span class="sxs-lookup"><span data-stu-id="ea69a-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="ea69a-114">請注意，此常式不會解析由點式 IPv4 位址組成的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ea69a-114">Note that this routine does not resolve host names that consist of a dotted IPv4 address.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ea69a-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea69a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea69a-116">Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析</span><span class="sxs-lookup"><span data-stu-id="ea69a-116">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="ea69a-117">通訊協定獨立名稱解析</span><span class="sxs-lookup"><span data-stu-id="ea69a-117">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="ea69a-118">註冊和名稱解析</span><span class="sxs-lookup"><span data-stu-id="ea69a-118">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
