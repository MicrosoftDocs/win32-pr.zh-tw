---
description: WSALookupServiceBegin 查詢會使用 SVCID \_ INET \_ HOSTNAMEBYADDR 做為服務類別 GUID。
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: SPI 中的 gethostbyaddr 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511441"
---
# <a name="gethostbyaddr-function-in-the-spi"></a><span data-ttu-id="e265a-103">SPI 中的 gethostbyaddr 函式</span><span class="sxs-lookup"><span data-stu-id="e265a-103">gethostbyaddr Function in the SPI</span></span>

<span data-ttu-id="e265a-104">[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)查詢會使用 SVCID \_ INET \_ HOSTNAMEBYADDR 做為服務類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="e265a-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="e265a-105">主機位址在 *lpszServiceInstanceName* 中是以小數點分隔的 IPv4 位址字串的形式提供 (例如 192.9.200.120) 。</span><span class="sxs-lookup"><span data-stu-id="e265a-105">The host address is supplied in *lpszServiceInstanceName* as a dotted-decimal IPv4 address string (for example, 192.9.200.120).</span></span> <span data-ttu-id="e265a-106">*Ws2 \_32.dll* 會指定 LUP 傳回 \_ \_ blob，且 NSP 會使用位移而非指標將 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構放在 BLOB (，而不是上述) 所述的指標。</span><span class="sxs-lookup"><span data-stu-id="e265a-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="e265a-107">Nsp 也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。</span><span class="sxs-lookup"><span data-stu-id="e265a-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="e265a-108">旗標</span><span class="sxs-lookup"><span data-stu-id="e265a-108">Flag</span></span>              | <span data-ttu-id="e265a-109">描述</span><span class="sxs-lookup"><span data-stu-id="e265a-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e265a-110">LUP \_ 傳回 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="e265a-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="e265a-111">從 *lpszServiceInstanceName* 中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構傳回 **h \_ 名稱** 成員。</span><span class="sxs-lookup"><span data-stu-id="e265a-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="e265a-112">LUP \_ 傳回 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="e265a-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="e265a-113">從 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)傳回定址資訊，埠資訊預設為零。</span><span class="sxs-lookup"><span data-stu-id="e265a-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

 

 
