---
description: PdhVbCreateCounterPathList 函式會顯示 [效能計數器流覽] 對話方塊，讓使用者選取數個效能計數器。 接著，每個選取的計數器路徑都必須使用 PdhVbGetCounterPathFromList 函式來讀取。
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: PdhVbCreateCounterPathList 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849290"
---
# <a name="pdhvbcreatecounterpathlist-function"></a><span data-ttu-id="e9ef2-104">PdhVbCreateCounterPathList 函式</span><span class="sxs-lookup"><span data-stu-id="e9ef2-104">PdhVbCreateCounterPathList function</span></span>

<span data-ttu-id="e9ef2-105">**PdhVbCreateCounterPathList** 函式會顯示 [效能計數器流覽] 對話方塊，讓使用者選取數個效能計數器。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-105">The **PdhVbCreateCounterPathList** function displays the performance counter browsing dialog box, which lets the user select several performance counters.</span></span> <span data-ttu-id="e9ef2-106">接著，每個選取的計數器路徑都必須使用 [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) 函式來讀取。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-106">Each selected counter path must then be read using the [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9ef2-107">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="e9ef2-108">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="e9ef2-109">函式 PdhVbCreateCounterPathList ( \_ Byval DetailLevel，只要是 \_ 字串 \_ ) </span><span class="sxs-lookup"><span data-stu-id="e9ef2-109">Function PdhVbCreateCounterPathList( \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="e9ef2-110">參數</span><span class="sxs-lookup"><span data-stu-id="e9ef2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ef2-111">*DetailLevel*</span><span class="sxs-lookup"><span data-stu-id="e9ef2-111">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ef2-112">要在對話方塊中顯示的計數器類型。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-112">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="e9ef2-113">使用下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-113">Use one of the following values.</span></span>



| <span data-ttu-id="e9ef2-114">值</span><span class="sxs-lookup"><span data-stu-id="e9ef2-114">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="e9ef2-115">意義</span><span class="sxs-lookup"><span data-stu-id="e9ef2-115">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="e9ef2-116"><dt>**效能 \_ 詳細資料 \_ ADVANCED**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ef2-116"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="e9ef2-117">Advanced user 可能瞭解的計數器，以及新手使用者的計數器。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-117">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="e9ef2-118"><dt>**效能 \_ 詳細資料 \_ 專家**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ef2-118"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="e9ef2-119">專家使用者和軟體發展人員可能會瞭解的計數器，以及新手和 advanced 使用者的計數器。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-119">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="e9ef2-120"><dt>**效能 \_ 詳細資料 \_ 新手**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ef2-120"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="e9ef2-121">只有新手使用者可能會瞭解的計數器。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-121">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="e9ef2-122"><dt>**效能 \_ 詳細資料 \_ 嚮導**</dt></span><span class="sxs-lookup"><span data-stu-id="e9ef2-122"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="e9ef2-123">系統中的所有計數器。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-123">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="e9ef2-124">*CaptionString*</span><span class="sxs-lookup"><span data-stu-id="e9ef2-124">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ef2-125">包含要在對話方塊標題列中顯示之文字的字串變數。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-125">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ef2-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9ef2-126">Return value</span></span>

<span data-ttu-id="e9ef2-127">函數會傳回使用者選取的計數器路徑數目。</span><span class="sxs-lookup"><span data-stu-id="e9ef2-127">The function returns the number of counter paths that the user selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ef2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9ef2-128">Requirements</span></span>



| <span data-ttu-id="e9ef2-129">需求</span><span class="sxs-lookup"><span data-stu-id="e9ef2-129">Requirement</span></span> | <span data-ttu-id="e9ef2-130">值</span><span class="sxs-lookup"><span data-stu-id="e9ef2-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ef2-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9ef2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ef2-132">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9ef2-132">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9ef2-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9ef2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ef2-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9ef2-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e9ef2-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9ef2-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9ef2-136"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9ef2-136"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="e9ef2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e9ef2-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9ef2-138"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9ef2-138"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ef2-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9ef2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ef2-140">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="e9ef2-140">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="e9ef2-141">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="e9ef2-141">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="e9ef2-142">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="e9ef2-142">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




