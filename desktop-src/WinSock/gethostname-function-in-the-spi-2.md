---
description: WSALookupServiceBegin 查詢會使用 SVCID \_ 主機名稱作為服務類別 GUID。
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: SPI 中的 gethostname 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aef10be48b264eb607184caf38bd687a5fe307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970169"
---
# <a name="gethostname-function-in-the-spi"></a><span data-ttu-id="87c10-103">SPI 中的 gethostname 函式</span><span class="sxs-lookup"><span data-stu-id="87c10-103">gethostname Function in the SPI</span></span>

<span data-ttu-id="87c10-104">[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)查詢會使用 SVCID \_ 主機名稱作為服務類別 GUID。</span><span class="sxs-lookup"><span data-stu-id="87c10-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="87c10-105">如果 *lpszServiceInstanceName* 為 null 或參考 null 字串 (即為。</span><span class="sxs-lookup"><span data-stu-id="87c10-105">If *lpszServiceInstanceName* is null or references a null string (that is .</span></span> <span data-ttu-id="87c10-106">"" ) ，將會解析本機主機。</span><span class="sxs-lookup"><span data-stu-id="87c10-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="87c10-107">否則，應該會在指定的主機名稱上進行查閱。</span><span class="sxs-lookup"><span data-stu-id="87c10-107">Otherwise, a lookup on a specified host name shall occur.</span></span> <span data-ttu-id="87c10-108">基於模擬 [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) 的目的，Ws2 \_32.dll 將會指定 *lpszServiceInstanceName* 的 Null 指標，並指定 LUP \_ \_ 傳回名稱，以便在 *lpszServiceInstanceName* 參數中傳回主機名稱。</span><span class="sxs-lookup"><span data-stu-id="87c10-108">For the purposes of emulating [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) the Ws2\_32.dll will specify a null pointer for *lpszServiceInstanceName*, and specify LUP\_RETURN\_NAME so that the host name is returned in the *lpszServiceInstanceName* parameter.</span></span> <span data-ttu-id="87c10-109">如果應用程式使用此查詢並指定 LUP \_ RETURN \_ ADDR，則會在 **CSADDR \_ 資訊** 結構中提供主機位址。</span><span class="sxs-lookup"><span data-stu-id="87c10-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address will be provided in a **CSADDR\_INFO** structure.</span></span> <span data-ttu-id="87c10-110">此查詢的 LUP 傳回 \_ \_ BLOB 動作未定義。</span><span class="sxs-lookup"><span data-stu-id="87c10-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="87c10-111">除非 *lpszQueryString* 參考的服務（例如 ftp），否則埠資訊會預設為零，在此情況下，將會提供指定服務的完整傳輸位址。</span><span class="sxs-lookup"><span data-stu-id="87c10-111">Port information will be defaulted to zero unless the *lpszQueryString* references a service such as ftp, in which case the complete transport address of the indicated service will be supplied.</span></span>

 

 



