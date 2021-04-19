---
description: Getservbyname 和 getservbyport 函式會使用 WSALookupServiceBegin 函數來查詢 SVCID \_ INET \_ SERVICEBYNAME 做為服務類別 GUID。
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: API 中的 getservbyname 和 getservbyport 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966709"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a><span data-ttu-id="3d1c6-103">API 中的 getservbyname 和 getservbyport 函式</span><span class="sxs-lookup"><span data-stu-id="3d1c6-103">getservbyname and getservbyport Functions in the API</span></span>

<span data-ttu-id="3d1c6-104">[**Getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)和 [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)函式會使用 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)函數來查詢 SVCID \_ INET \_ SERVICEBYNAME 做為服務類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-104">The [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions use the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_SERVICEBYNAME as the service class GUID.</span></span> <span data-ttu-id="3d1c6-105">傳遞至 **WSALookupServiceBegin** 函式的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構中的 *lpszServiceInstanceName* 成員會參考字串來指出服務名稱或服務埠，並 (選擇性地) 服務通訊協定。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-105">The *lpszServiceInstanceName* member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function references a string to indicate the service name or service port, and (optionally) the service protocol.</span></span> <span data-ttu-id="3d1c6-106">字串的格式會以 FTP 或 TCP 或 21/TCP 或單純的 FTP 來說明。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-106">The formatting of the string is illustrated as FTP or TCP or 21/TCP or just FTP.</span></span> <span data-ttu-id="3d1c6-107">字串不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-107">The string is not case sensitive.</span></span> <span data-ttu-id="3d1c6-108">斜線（如果有的話）會將通訊協定識別碼與之前的字串部分隔開。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-108">The slash mark, if present, separates the protocol identifier from the preceding part of the string.</span></span> <span data-ttu-id="3d1c6-109">Ws2 \_32.dll 將會指定 LUP \_ 傳回 \_ BLOB，而且命名空間提供者會使用位移而非指標將 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) 結構放在 BLOB (，而不是上述) 所述。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-109">The Ws2\_32.dll will specify LUP\_RETURN\_BLOB and the namespace provider will place a [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="3d1c6-110">命名空間提供者也應接受這些其他 LUP 傳回 \_ \_ \* 旗標。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-110">Namespace providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="3d1c6-111">旗標</span><span class="sxs-lookup"><span data-stu-id="3d1c6-111">Flag</span></span>              | <span data-ttu-id="3d1c6-112">描述</span><span class="sxs-lookup"><span data-stu-id="3d1c6-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1c6-113">LUP \_ 傳回 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="3d1c6-113">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="3d1c6-114">從 *lpszServiceInstanceName* 中的 [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent)結構傳回 **s \_ 名稱** 成員。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-114">Returns the **s\_name** member from [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3d1c6-115">LUP \_ 傳回 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="3d1c6-115">LUP\_RETURN\_TYPE</span></span> | <span data-ttu-id="3d1c6-116">傳回 *lpServiceClassId* 中的標準 GUID。瞭解識別為 FTP 或21的服務可能會在另一個埠上，根據本機建立的慣例。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-116">Returns canonical GUID in *lpServiceClassId* It is understood that a service identified as FTP or 21 may be on another port according to locally established conventions.</span></span> <span data-ttu-id="3d1c6-117">[**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent)結構的 **s \_ port** 參數應該指出在本機環境中可以聯繫服務的位置。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-117">The **s\_port** parameter of the [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure should indicate where the service can be contacted in the local environment.</span></span> <span data-ttu-id="3d1c6-118">當 LUP 傳回類型設定時，所傳回的標準 GUID \_ \_ 應該是 Svcs 中的其中一個預先定義 guid，對應于 **SERVENT** 結構中指出的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="3d1c6-118">The canonical GUID returned when LUP\_RETURN\_TYPE is set should be one of the predefined GUIDs from Svcs.h that corresponds to the port number indicated in the **SERVENT** structure.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3d1c6-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="3d1c6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d1c6-120">Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析</span><span class="sxs-lookup"><span data-stu-id="3d1c6-120">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="3d1c6-121">通訊協定獨立名稱解析</span><span class="sxs-lookup"><span data-stu-id="3d1c6-121">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="3d1c6-122">註冊和名稱解析</span><span class="sxs-lookup"><span data-stu-id="3d1c6-122">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



