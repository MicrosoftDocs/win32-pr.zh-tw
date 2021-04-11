---
description: PdhVbGetOneCounterPath 函式會顯示一個對話方塊，讓使用者流覽可用的效能計數器，並選取一個計數器。
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: PdhVbGetOneCounterPath 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849288"
---
# <a name="pdhvbgetonecounterpath-function"></a><span data-ttu-id="aab4c-103">PdhVbGetOneCounterPath 函式</span><span class="sxs-lookup"><span data-stu-id="aab4c-103">PdhVbGetOneCounterPath function</span></span>

<span data-ttu-id="aab4c-104">**PdhVbGetOneCounterPath** 函式會顯示一個對話方塊，讓使用者流覽可用的效能計數器，並選取一個計數器。</span><span class="sxs-lookup"><span data-stu-id="aab4c-104">The **PdhVbGetOneCounterPath** function displays a dialog box that lets the user browse the available performance counters and select one counter.</span></span> <span data-ttu-id="aab4c-105">選取的計數器會在 *PathString* 變數中傳回。</span><span class="sxs-lookup"><span data-stu-id="aab4c-105">The counter selected is returned in the *PathString* variable.</span></span> <span data-ttu-id="aab4c-106">在呼叫此函式之前，必須先將 *PathString* 變數進行維度和初始化，而且維度大小必須由 *PathLength* 變數表示。</span><span class="sxs-lookup"><span data-stu-id="aab4c-106">The *PathString* variable must be dimensioned and initialized before this function is called, and the dimensioned size must be indicated by the *PathLength* variable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aab4c-107">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="aab4c-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="aab4c-108">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="aab4c-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="aab4c-109">函數 PdhVbGetOneCounterPath ( \_ Byval PathString As string， \_ Byval PathLength long，byval DetailLevel long，Byval \_ \_ CaptionString as string \_ ) long</span><span class="sxs-lookup"><span data-stu-id="aab4c-109">Function PdhVbGetOneCounterPath( \_ ByVal PathString As String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="aab4c-110">參數</span><span class="sxs-lookup"><span data-stu-id="aab4c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aab4c-111">*PathString*</span><span class="sxs-lookup"><span data-stu-id="aab4c-111">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="aab4c-112">初始化的字串變數，用來接收使用者選取的計數器路徑。</span><span class="sxs-lookup"><span data-stu-id="aab4c-112">Initialized string variable used to receive the counter path selected by the user.</span></span>

</dd> <dt>

<span data-ttu-id="aab4c-113">*PathLength*</span><span class="sxs-lookup"><span data-stu-id="aab4c-113">*PathLength*</span></span> 
</dt> <dd>

<span data-ttu-id="aab4c-114">初始化的 PathString 長度。</span><span class="sxs-lookup"><span data-stu-id="aab4c-114">Length of the initialized PathString.</span></span>

</dd> <dt>

<span data-ttu-id="aab4c-115">*DetailLevel*</span><span class="sxs-lookup"><span data-stu-id="aab4c-115">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="aab4c-116">要在對話方塊中顯示的計數器類型。</span><span class="sxs-lookup"><span data-stu-id="aab4c-116">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="aab4c-117">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="aab4c-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="aab4c-118">值</span><span class="sxs-lookup"><span data-stu-id="aab4c-118">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="aab4c-119">意義</span><span class="sxs-lookup"><span data-stu-id="aab4c-119">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="aab4c-120"><dt>**效能 \_ 詳細資料 \_ ADVANCED**</dt></span><span class="sxs-lookup"><span data-stu-id="aab4c-120"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="aab4c-121">Advanced user 可能瞭解的計數器，以及新手使用者的計數器。</span><span class="sxs-lookup"><span data-stu-id="aab4c-121">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="aab4c-122"><dt>**效能 \_ 詳細資料 \_ 專家**</dt></span><span class="sxs-lookup"><span data-stu-id="aab4c-122"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="aab4c-123">專家使用者和軟體發展人員可能會瞭解的計數器，以及新手和 advanced 使用者的計數器。</span><span class="sxs-lookup"><span data-stu-id="aab4c-123">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="aab4c-124"><dt>**效能 \_ 詳細資料 \_ 新手**</dt></span><span class="sxs-lookup"><span data-stu-id="aab4c-124"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="aab4c-125">只有新手使用者可能會瞭解的計數器。</span><span class="sxs-lookup"><span data-stu-id="aab4c-125">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="aab4c-126"><dt>**效能 \_ 詳細資料 \_ 嚮導**</dt></span><span class="sxs-lookup"><span data-stu-id="aab4c-126"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="aab4c-127">系統中的所有計數器。</span><span class="sxs-lookup"><span data-stu-id="aab4c-127">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="aab4c-128">*CaptionString*</span><span class="sxs-lookup"><span data-stu-id="aab4c-128">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="aab4c-129">包含要在對話方塊標題列中顯示之文字的字串變數。</span><span class="sxs-lookup"><span data-stu-id="aab4c-129">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aab4c-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="aab4c-130">Return value</span></span>

<span data-ttu-id="aab4c-131">函數會傳回寫入 *PathString* 緩衝區的字元數。</span><span class="sxs-lookup"><span data-stu-id="aab4c-131">The function returns the number of characters written to the *PathString* buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="aab4c-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="aab4c-132">Requirements</span></span>



| <span data-ttu-id="aab4c-133">需求</span><span class="sxs-lookup"><span data-stu-id="aab4c-133">Requirement</span></span> | <span data-ttu-id="aab4c-134">值</span><span class="sxs-lookup"><span data-stu-id="aab4c-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aab4c-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aab4c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="aab4c-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aab4c-136">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aab4c-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aab4c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="aab4c-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aab4c-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="aab4c-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="aab4c-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="aab4c-140"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="aab4c-140"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="aab4c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="aab4c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aab4c-142"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aab4c-142"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aab4c-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aab4c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab4c-144">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="aab4c-144">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="aab4c-145">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="aab4c-145">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="aab4c-146">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="aab4c-146">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




