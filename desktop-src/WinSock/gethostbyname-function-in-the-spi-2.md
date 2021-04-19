---
description: Winsock SPI 中的 Gethostbyname 函式。
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: SPI 中的 gethostbyname 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972034"
---
# <a name="gethostbyname-function-in-the-spi"></a><span data-ttu-id="ad05e-103">SPI 中的 gethostbyname 函式</span><span class="sxs-lookup"><span data-stu-id="ad05e-103">gethostbyname Function in the SPI</span></span>

<span data-ttu-id="ad05e-104">[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)查詢會使用 SVCID \_ INET \_ HOSTADDRBYNAME 做為服務類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="ad05e-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="ad05e-105">主機名稱是在 *lpszServiceInstanceName* 中提供。</span><span class="sxs-lookup"><span data-stu-id="ad05e-105">The host name is supplied in *lpszServiceInstanceName*.</span></span> <span data-ttu-id="ad05e-106">*Ws2 \_32.dll* 會指定 LUP 傳回 \_ \_ blob，且 NSP 會使用位移而非指標將 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構放在 BLOB (，而不是上述) 所述的指標。</span><span class="sxs-lookup"><span data-stu-id="ad05e-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="ad05e-107">Nsp 也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。</span><span class="sxs-lookup"><span data-stu-id="ad05e-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="ad05e-108">旗標</span><span class="sxs-lookup"><span data-stu-id="ad05e-108">Flag</span></span>              | <span data-ttu-id="ad05e-109">描述</span><span class="sxs-lookup"><span data-stu-id="ad05e-109">Description</span></span>                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad05e-110">LUP \_ 傳回 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="ad05e-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="ad05e-111">從 *lpszServiceInstanceName* 中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)結構傳回 **h \_ 名稱** 成員。</span><span class="sxs-lookup"><span data-stu-id="ad05e-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                            |
| <span data-ttu-id="ad05e-112">LUP \_ 傳回 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="ad05e-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="ad05e-113">從 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)結構中的 [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent)傳回定址資訊，埠資訊預設為零。</span><span class="sxs-lookup"><span data-stu-id="ad05e-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="ad05e-114">請注意，此常式不會解析由以小數點分隔的 IPv4 位址字串組成的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ad05e-114">Note that this routine does not resolve host names consisting of a dotted-decimal IPv4 address string.</span></span> |



 

 

 
