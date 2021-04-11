---
description: WSALookupServiceBegin 查詢會使用 SVCID \_ INET \_ SERVICEBYNAME 做為服務類別 GUID。
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: SPI 中的 getservbyname 和 getservbyport 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd910dc7ab478c262bd5ca6c480dc3ec58e1b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113072"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a><span data-ttu-id="03b65-103">SPI 中的 getservbyname 和 getservbyport 函數</span><span class="sxs-lookup"><span data-stu-id="03b65-103">getservbyname and getservbyport Functions in the SPI</span></span>

<span data-ttu-id="03b65-104">[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)查詢會使用 SVCID \_ INET \_ SERVICEBYNAME 做為服務類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="03b65-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_SERVICEBYNAME as the service class GUID.</span></span> <span data-ttu-id="03b65-105">*LpszServiceInstanceName* 參數會參考指出服務名稱或服務埠的字串，並 (選擇性地) 服務通訊協定。</span><span class="sxs-lookup"><span data-stu-id="03b65-105">The *lpszServiceInstanceName* parameter references a string that indicates the service name or service port, and (optionally) the service protocol.</span></span> <span data-ttu-id="03b65-106">字串的格式會以 ftp/tcp 或 21/tcp 或單純的 ftp 來說明。</span><span class="sxs-lookup"><span data-stu-id="03b65-106">The formatting of the string is illustrated as ftp/tcp or 21/tcp or just ftp.</span></span> <span data-ttu-id="03b65-107">字串不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="03b65-107">The string is not case sensitive.</span></span> <span data-ttu-id="03b65-108">斜線（如果有的話）會將通訊協定識別碼與之前的字串部分隔開。</span><span class="sxs-lookup"><span data-stu-id="03b65-108">The slash mark, if present, separates the protocol identifier from the preceding part of the string.</span></span> <span data-ttu-id="03b65-109">Ws2 \_32.dll 將會指定 LUP \_ 傳回 \_ BLOB，而且 NSP 會使用位移而非指標將 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) 結構放在 BLOB (，而不是上述) 所述。</span><span class="sxs-lookup"><span data-stu-id="03b65-109">The Ws2\_32.dll will specify LUP\_RETURN\_BLOB and the NSP will place a [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="03b65-110">Nsp 也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。</span><span class="sxs-lookup"><span data-stu-id="03b65-110">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="03b65-111">旗標</span><span class="sxs-lookup"><span data-stu-id="03b65-111">Flag</span></span>              | <span data-ttu-id="03b65-112">描述</span><span class="sxs-lookup"><span data-stu-id="03b65-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03b65-113">LUP \_ 傳回 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="03b65-113">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="03b65-114">從 *lpszServiceInstanceName* 中的 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent)結構傳回 **s \_ 名稱** 成員。</span><span class="sxs-lookup"><span data-stu-id="03b65-114">Returns the **s\_name** member from [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="03b65-115">LUP \_ 傳回 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="03b65-115">LUP\_RETURN\_TYPE</span></span> | <span data-ttu-id="03b65-116">傳回 *lpServiceClassId* 中的標準 GUID。瞭解識別為 ftp 或21的服務可能會在另一個埠上，根據本機建立的慣例。</span><span class="sxs-lookup"><span data-stu-id="03b65-116">Returns canonical GUID in *lpServiceClassId* It is understood that a service identified as ftp or 21 may be on another port according to locally established conventions.</span></span> <span data-ttu-id="03b65-117">[**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent)結構的 **s \_ 埠** 成員應該指出在本機環境中可以聯繫服務的位置。</span><span class="sxs-lookup"><span data-stu-id="03b65-117">The **s\_port** member of the [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure should indicate where the service can be contacted in the local environment.</span></span> <span data-ttu-id="03b65-118">當 LUP 傳回類型設定時，所傳回的標準 GUID \_ \_ 應該是 svcs 中的其中一個預先定義 guid，對應于 **SERVENT** 結構中指出的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="03b65-118">The canonical GUID returned when LUP\_RETURN\_TYPE is set should be one of the predefined GUIDs from svcs.h that corresponds to the port number indicated in the **SERVENT** structure.</span></span> |



 

 

 



