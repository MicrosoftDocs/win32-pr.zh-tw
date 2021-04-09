---
description: ICE29 會驗證截斷的資料流程名稱是否維持唯一。 任何具有二進位或物件資料行的資料表都會經過驗證。 請參閱 Binary 資料行資料類型。
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f606bd09314d045b643816c08349eba38bde72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943888"
---
# <a name="ice29"></a><span data-ttu-id="1e78b-105">ICE29</span><span class="sxs-lookup"><span data-stu-id="1e78b-105">ICE29</span></span>

<span data-ttu-id="1e78b-106">ICE29 會驗證截斷的資料流程名稱是否維持唯一。</span><span class="sxs-lookup"><span data-stu-id="1e78b-106">ICE29 validates that truncated stream names remain unique.</span></span> <span data-ttu-id="1e78b-107">任何具有二進位或物件資料行的資料表都會經過驗證。</span><span class="sxs-lookup"><span data-stu-id="1e78b-107">Any table having a Binary or Object column is validated.</span></span> <span data-ttu-id="1e78b-108">請參閱 [Binary](binary.md) 資料行資料類型。</span><span class="sxs-lookup"><span data-stu-id="1e78b-108">See the [Binary](binary.md) column data type.</span></span>

<span data-ttu-id="1e78b-109">由 Win32 OLE 結構化儲存體執行的資料流程處理會限制資料流程名稱。</span><span class="sxs-lookup"><span data-stu-id="1e78b-109">Handling of streams by the Win32 OLE structured storage implementation limits stream names.</span></span> <span data-ttu-id="1e78b-110">請參閱 [OLE 對資料流程的限制](ole-limitations-on-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="1e78b-110">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="1e78b-111">安裝程式最多可壓縮長度為62個字元的資料流程名稱。</span><span class="sxs-lookup"><span data-stu-id="1e78b-111">The installer can compress stream names up to 62 characters in length.</span></span> <span data-ttu-id="1e78b-112">長度超過此名稱的名稱會被截斷。</span><span class="sxs-lookup"><span data-stu-id="1e78b-112">Names longer than this are truncated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e78b-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e78b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e78b-114">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="1e78b-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



