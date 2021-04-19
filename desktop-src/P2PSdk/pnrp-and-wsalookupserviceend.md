---
description: PNRP 會使用 WSALookupServiceEnd 函數來執行下列作業。
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP 和 WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985470"
---
# <a name="pnrp-and-wsalookupserviceend"></a><span data-ttu-id="5d421-103">PNRP 和 WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="5d421-103">PNRP and WSALookupServiceEnd</span></span>

<span data-ttu-id="5d421-104">PNRP 會使用 [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) 函數來執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="5d421-104">PNRP uses the [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) function to do the following:</span></span>

-   <span data-ttu-id="5d421-105">終止先前呼叫 WSALookupServiceBegin 所起始的查詢[ ](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="5d421-105">Terminate a query initiated in a previous call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span></span>
-   <span data-ttu-id="5d421-106">解除封鎖對 [**WSALookupServiceNext**](winsock-nsp-reference-links.md) 的呼叫以停止搜尋</span><span class="sxs-lookup"><span data-stu-id="5d421-106">Unblock a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to stop the search</span></span>

<span data-ttu-id="5d421-107">呼叫 [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) 會終止查詢並清除內容。</span><span class="sxs-lookup"><span data-stu-id="5d421-107">A call to [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) terminates a query and cleans up the context.</span></span> <span data-ttu-id="5d421-108">從呼叫 **WSALookupServiceBegin** 取得的控制碼必須傳遞至 **WSALookupServiceEnd** 的參數。</span><span class="sxs-lookup"><span data-stu-id="5d421-108">The handle obtained from a call to **WSALookupServiceBegin** must be passed as a parameter to **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="5d421-109">如需 PNRP 和 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) 函數的詳細資訊，請參閱 [pnrp 和 WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)。</span><span class="sxs-lookup"><span data-stu-id="5d421-109">For more information about PNRP and the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function, see [PNRP and WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d421-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d421-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d421-111">PNRP 和 WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="5d421-111">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="5d421-112">PNRP NSP 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5d421-112">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="5d421-113">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="5d421-113">**WSALookupServiceNext**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



