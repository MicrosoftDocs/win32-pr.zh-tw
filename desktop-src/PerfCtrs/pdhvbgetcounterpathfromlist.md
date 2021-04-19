---
description: PdhVbGetCounterPathFromList 函式會將索引參數所參考的計數器路徑從使用者建立的計數器路徑清單複製到 PdhVbCreateCounterPathList 函數的最新呼叫。
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: PdhVbGetCounterPathFromList 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974278"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a><span data-ttu-id="8c0c8-103">PdhVbGetCounterPathFromList 函式</span><span class="sxs-lookup"><span data-stu-id="8c0c8-103">PdhVbGetCounterPathFromList function</span></span>

<span data-ttu-id="8c0c8-104">**PdhVbGetCounterPathFromList** 函式會將 *索引* 參數所參考的計數器路徑從使用者建立的計數器路徑清單複製到 [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)函數的最新呼叫。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-104">The **PdhVbGetCounterPathFromList** function copies the counter path referenced by the *Index* parameter from a counter path list created by the user from the most recent call to the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c0c8-105">本主題所描述的功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="8c0c8-106">相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="8c0c8-107">函式 PdhVbGetCounterPathFromList ( 的 \_ Byval 索引為 long，以字串形式的 \_ byval 緩衝區， \_ \_ ) 長時間的 byval BufferLength</span><span class="sxs-lookup"><span data-stu-id="8c0c8-107">Function PdhVbGetCounterPathFromList( \_ ByVal Index As Long, \_ ByVal Buffer As String, \_ ByVal BufferLength As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="8c0c8-108">參數</span><span class="sxs-lookup"><span data-stu-id="8c0c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c0c8-109">*Index*</span><span class="sxs-lookup"><span data-stu-id="8c0c8-109">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0c8-110">要取出的計數器路徑索引。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-110">Index of the counter path to retrieve.</span></span> <span data-ttu-id="8c0c8-111">這必須是大於或等於1，且小於或等於 [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) 函數所傳回值的值。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-111">This must be a value that is greater than or equal to 1, and less than or equal to the value returned by the [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8c0c8-112">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="8c0c8-112">*Buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0c8-113">經過維度和初始化的字串，將會接收對應至 Index 參數值的計數器路徑。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-113">Dimensioned and initialized string that will receive the counter path that corresponds to the value of the Index parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8c0c8-114">*BufferLength*</span><span class="sxs-lookup"><span data-stu-id="8c0c8-114">*BufferLength*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0c8-115">緩衝區所參考的字串中所能容納的最大字元數。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-115">Maximum number of characters that will fit in the string referenced by Buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c0c8-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c0c8-116">Return value</span></span>

<span data-ttu-id="8c0c8-117">函數會傳回復制到緩衝區的字元數。</span><span class="sxs-lookup"><span data-stu-id="8c0c8-117">The function returns the number of characters copied to Buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0c8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c0c8-118">Requirements</span></span>



| <span data-ttu-id="8c0c8-119">需求</span><span class="sxs-lookup"><span data-stu-id="8c0c8-119">Requirement</span></span> | <span data-ttu-id="8c0c8-120">值</span><span class="sxs-lookup"><span data-stu-id="8c0c8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0c8-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c0c8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8c0c8-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c0c8-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c0c8-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c0c8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8c0c8-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c0c8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8c0c8-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c0c8-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c0c8-126"><dt>Pdh. .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c8-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="8c0c8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8c0c8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c0c8-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c0c8-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c0c8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c0c8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c0c8-130">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="8c0c8-130">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="8c0c8-131">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="8c0c8-131">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="8c0c8-132">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="8c0c8-132">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




