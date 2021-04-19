---
description: Gethostname 函式會使用 WSALookupServiceBegin 函數，將 SVCID \_ 主機名稱查詢為服務類別 GUID。
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: API 中的 gethostname 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970424"
---
# <a name="gethostname-function-in-the-api"></a><span data-ttu-id="2be4b-103">API 中的 gethostname 函式</span><span class="sxs-lookup"><span data-stu-id="2be4b-103">gethostname Function in the API</span></span>

<span data-ttu-id="2be4b-104">[**Gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname)函式會使用 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)函數，將 SVCID \_ 主機名稱查詢為服務類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="2be4b-104">The [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="2be4b-105">如果傳遞給 **WSALookupServiceBegin** 函式之 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)結構的 **lpszServiceInstanceName** 成員是 **null** 或參考 **null** 字串 (也就是。</span><span class="sxs-lookup"><span data-stu-id="2be4b-105">If the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function is **NULL** or references a **NULL** string (that is .</span></span> <span data-ttu-id="2be4b-106">"" ) ，將會解析本機主機。</span><span class="sxs-lookup"><span data-stu-id="2be4b-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="2be4b-107">否則，就會在指定的主機名稱上進行查閱。</span><span class="sxs-lookup"><span data-stu-id="2be4b-107">Otherwise, a lookup on a specified host name occurs.</span></span> <span data-ttu-id="2be4b-108">基於模擬 **gethostname** 的目的 \_ ，Ws232.dll 指定 **lpszServiceInstanceName** 成員的 **Null** 指標，並指定 LUP \_ \_ 傳回名稱，以便在 **lpszServiceInstanceName** 成員中傳回主機名稱。</span><span class="sxs-lookup"><span data-stu-id="2be4b-108">For the purposes of emulating **gethostname** the Ws2\_32.dll specifies a **NULL** pointer for the **lpszServiceInstanceName** member, and specifies LUP\_RETURN\_NAME so that the host name is returned in the **lpszServiceInstanceName** member.</span></span> <span data-ttu-id="2be4b-109">如果應用程式使用此查詢並指定 LUP \_ RETURN \_ ADDR，則會在 [**CSADDR \_ 資訊**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) 結構中提供主機位址。</span><span class="sxs-lookup"><span data-stu-id="2be4b-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address is provided in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span> <span data-ttu-id="2be4b-110">此查詢的 LUP 傳回 \_ \_ BLOB 動作未定義。</span><span class="sxs-lookup"><span data-stu-id="2be4b-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="2be4b-111">除非傳遞給 **WSALookupServiceBegin** 函式之 **WSAQUERYSET** 結構的 **lpszQueryString** 成員參考 FTP 之類的服務（在此情況下，會提供指定服務的完整傳輸位址），否則埠資訊會預設為零。</span><span class="sxs-lookup"><span data-stu-id="2be4b-111">Port information is defaulted to zero unless the **lpszQueryString** member of the **WSAQUERYSET** structure passed to the **WSALookupServiceBegin** function references a service such as FTP, in which case the complete transport address of the indicated service is supplied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2be4b-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="2be4b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2be4b-113">Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析</span><span class="sxs-lookup"><span data-stu-id="2be4b-113">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="2be4b-114">通訊協定獨立名稱解析</span><span class="sxs-lookup"><span data-stu-id="2be4b-114">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="2be4b-115">註冊和名稱解析</span><span class="sxs-lookup"><span data-stu-id="2be4b-115">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
