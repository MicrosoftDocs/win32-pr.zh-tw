---
description: Windows 通訊端中的名稱服務查詢 (Winsock) 。
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: 服務查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad1950c0f1d97ab0ca6d06f79ed6ff0180d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026550"
---
# <a name="service-query"></a><span data-ttu-id="3b527-103">服務查詢</span><span class="sxs-lookup"><span data-stu-id="3b527-103">Service Query</span></span>

-   [<span data-ttu-id="3b527-104">**NSPLookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="3b527-104">**NSPLookupServiceBegin**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [<span data-ttu-id="3b527-105">**NSPLookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="3b527-105">**NSPLookupServiceNext**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [<span data-ttu-id="3b527-106">**NSPLookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="3b527-106">**NSPLookupServiceEnd**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

<span data-ttu-id="3b527-107">名稱服務查詢牽涉到一連串的呼叫： [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)，後面接著一或多個 [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) 的呼叫，然後以 [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)的呼叫結尾。</span><span class="sxs-lookup"><span data-stu-id="3b527-107">A name service query involves a series of calls: [**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), followed by one or more calls to [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) and ending with a call to [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend).</span></span> <span data-ttu-id="3b527-108">[**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) 會採用 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 結構作為輸入，以便定義查詢參數以及一組旗標，以提供對搜尋作業的額外控制。</span><span class="sxs-lookup"><span data-stu-id="3b527-108">[**NSPLookupServiceBegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as input in order to define the query parameters along with a set of flags to provide additional control over the search operation.</span></span> <span data-ttu-id="3b527-109">它會傳回查詢控制碼，此控制碼用於後續呼叫 **NSPLookupServiceNext** 和 **NSPLookupServiceEnd**。</span><span class="sxs-lookup"><span data-stu-id="3b527-109">It returns a query handle which is used in the subsequent calls to **NSPLookupServiceNext** and **NSPLookupServiceEnd**.</span></span>

<span data-ttu-id="3b527-110">命名空間 SPI 用戶端會叫用 [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) 來取得查詢結果，並在用戶端提供的 [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) 緩衝區中提供結果。</span><span class="sxs-lookup"><span data-stu-id="3b527-110">The namespace SPI client invokes [**NSPLookupServiceNext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) to obtain query results, with results supplied in an client-supplied [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) buffer.</span></span> <span data-ttu-id="3b527-111">用戶端會繼續呼叫 **NSPLookupServiceNext** ，直到錯誤碼 \_ \_ 不會再傳回錯誤訊息 \_ ，指出已取出所有結果。</span><span class="sxs-lookup"><span data-stu-id="3b527-111">The client continues to call **NSPLookupServiceNext** until the error code WSA\_E\_NO\_MORE is returned indicating that all results have been retrieved.</span></span> <span data-ttu-id="3b527-112">然後搜尋會透過呼叫 [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)來終止。</span><span class="sxs-lookup"><span data-stu-id="3b527-112">The search is then terminated by a call to [**NSPLookupServiceEnd**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend).</span></span> <span data-ttu-id="3b527-113">從另一個執行緒呼叫時， **NSPLookupServiceEnd** 函式也可以用來取消目前暫止的 **NSPLookupServiceNext** 。</span><span class="sxs-lookup"><span data-stu-id="3b527-113">The **NSPLookupServiceEnd** function can also be used to cancel a currently pending **NSPLookupServiceNext** when called from another thread.</span></span>

<span data-ttu-id="3b527-114">在 Windows 通訊端2中，WSAENOMORE (10102) 和 WSA \_ E \_ 不再 \_ (10110) 定義了衝突的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b527-114">In Windows Sockets 2, conflicting error codes are defined for WSAENOMORE (10102) and WSA\_E\_NO\_MORE (10110).</span></span> <span data-ttu-id="3b527-115">錯誤碼 WSAENOMORE 將會在未來的版本中移除，而且只有 WSA \_ E \_ 不再有 \_ 其他會保留。</span><span class="sxs-lookup"><span data-stu-id="3b527-115">The error code WSAENOMORE will be removed in a future version and only WSA\_E\_NO\_MORE will remain.</span></span> <span data-ttu-id="3b527-116">命名空間提供者應該儘快切換為使用不會再使用的 \_ \_ \_ 錯誤代碼，以維持與最廣泛的應用程式之間的相容性。</span><span class="sxs-lookup"><span data-stu-id="3b527-116">Namespace providers should switch to using the WSA\_E\_NO\_MORE error code as soon as possible to maintain compatibility with the widest possible range of applications.</span></span>

 

 



