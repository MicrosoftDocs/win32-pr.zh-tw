---
description: 您可以使用下列函數來處理 Visual Basic 中的效能資料。
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Visual Basic 的效能計數器函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849283"
---
# <a name="performance-counters-functions-for-visual-basic"></a><span data-ttu-id="e8eb3-103">Visual Basic 的效能計數器函數</span><span class="sxs-lookup"><span data-stu-id="e8eb3-103">Performance Counters Functions for Visual Basic</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8eb3-104">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="e8eb3-104">The functions that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="e8eb3-105">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="e8eb3-105">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="e8eb3-106">您可以使用下列函數來處理 Visual Basic 中的效能資料。</span><span class="sxs-lookup"><span data-stu-id="e8eb3-106">You can use the following functions to work with performance data in Visual Basic.</span></span>

- [<span data-ttu-id="e8eb3-107">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-107">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="e8eb3-108">**PdhCollectQueryData**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-108">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="e8eb3-109">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-109">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="e8eb3-110">**PdhVbAddCounter**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-110">**PdhVbAddCounter**</span></span>](pdhvbaddcounter.md)
- [<span data-ttu-id="e8eb3-111">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-111">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
- [<span data-ttu-id="e8eb3-112">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-112">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
- [<span data-ttu-id="e8eb3-113">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-113">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
- [<span data-ttu-id="e8eb3-114">**PdhVbGetDoubleCounterValue**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-114">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
- [<span data-ttu-id="e8eb3-115">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-115">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
- [<span data-ttu-id="e8eb3-116">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-116">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
- [<span data-ttu-id="e8eb3-117">**PdhVbIsGoodStatus**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-117">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
- [<span data-ttu-id="e8eb3-118">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-118">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
- [<span data-ttu-id="e8eb3-119">**PdhVbOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-119">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
- [<span data-ttu-id="e8eb3-120">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="e8eb3-120">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)

> [!NOTE]
> <span data-ttu-id="e8eb3-121">這些函 `PdhVb***` 式適用于每個進程的會話，而且不是安全線程。</span><span class="sxs-lookup"><span data-stu-id="e8eb3-121">The `PdhVb***` functions work on a per-process session and are not thread-safe.</span></span> <span data-ttu-id="e8eb3-122">這些函式只能從簡單的單一執行緒應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="e8eb3-122">These functions should only be used from simple single-threaded applications.</span></span>
