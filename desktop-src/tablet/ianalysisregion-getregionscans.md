---
description: 捕獲定義 IAnalysisRegion 區域的矩形陣列。
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'IAnalysisRegion：： GetRegionScans 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973290"
---
# <a name="ianalysisregiongetregionscans-method"></a><span data-ttu-id="e9909-103">IAnalysisRegion：： GetRegionScans 方法</span><span class="sxs-lookup"><span data-stu-id="e9909-103">IAnalysisRegion::GetRegionScans method</span></span>

<span data-ttu-id="e9909-104">捕獲定義 [**IAnalysisRegion**](ianalysisregion.md)區域的矩形陣列。</span><span class="sxs-lookup"><span data-stu-id="e9909-104">Retrieves an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9909-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9909-105">Syntax</span></span>


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a><span data-ttu-id="e9909-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9909-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9909-107">*pulCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9909-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9909-108">*PRegionScans* 中傳回的矩形數目。</span><span class="sxs-lookup"><span data-stu-id="e9909-108">The number of rectangles returned in *pRegionScans*.</span></span>

</dd> <dt>

<span data-ttu-id="e9909-109">*pRegionScans* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9909-109">*pRegionScans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9909-110">矩形陣列的指標，該陣列定義 [**IAnalysisRegion**](ianalysisregion.md)的區域。</span><span class="sxs-lookup"><span data-stu-id="e9909-110">A pointer to an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9909-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9909-111">Return value</span></span>

<span data-ttu-id="e9909-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="e9909-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9909-113">備註</span><span class="sxs-lookup"><span data-stu-id="e9909-113">Remarks</span></span>

<span data-ttu-id="e9909-114">如果 *pRegionScans* 傳遞為 **Null**，則 **GetRegionScans** 方法會傳回 **S \_ OK** ，而且在 *pulCount* 中會傳回矩形的數目。</span><span class="sxs-lookup"><span data-stu-id="e9909-114">If *pRegionScans* is passed as **NULL**, the **GetRegionScans** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="e9909-115">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *pRegionScans* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e9909-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pRegionScans* when you no longer need the information.</span></span>

 

<span data-ttu-id="e9909-116">矩形的界限為筆墨空間座標。</span><span class="sxs-lookup"><span data-stu-id="e9909-116">The bounds of the rectangles are in ink-space coordinates.</span></span>

<span data-ttu-id="e9909-117">傳回之矩形的聯集代表 [**IAnalysisRegion**](ianalysisregion.md)的區域。</span><span class="sxs-lookup"><span data-stu-id="e9909-117">The union of the returned rectangles represents the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e9909-118">範例</span><span class="sxs-lookup"><span data-stu-id="e9909-118">Examples</span></span>

<span data-ttu-id="e9909-119">下列範例顯示如何取得定義 [**IAnalysisRegion**](ianalysisregion.md)區域的矩形， `region` 以及如何只取得矩形的數目。</span><span class="sxs-lookup"><span data-stu-id="e9909-119">The following example shows how to get the rectangles that define the area of the [**IAnalysisRegion**](ianalysisregion.md), `region` and how to get only the number of rectangles.</span></span>


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="e9909-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9909-120">Requirements</span></span>



| <span data-ttu-id="e9909-121">需求</span><span class="sxs-lookup"><span data-stu-id="e9909-121">Requirement</span></span> | <span data-ttu-id="e9909-122">值</span><span class="sxs-lookup"><span data-stu-id="e9909-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9909-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9909-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e9909-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9909-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e9909-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9909-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e9909-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="e9909-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e9909-127">標頭</span><span class="sxs-lookup"><span data-stu-id="e9909-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9909-128"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e9909-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e9909-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e9909-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9909-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9909-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e9909-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9909-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9909-132">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="e9909-132">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="e9909-133">**IAnalysisRegion：： GetBounds 方法**</span><span class="sxs-lookup"><span data-stu-id="e9909-133">**IAnalysisRegion::GetBounds Method**</span></span>](ianalysisregion-getbounds.md)
</dt> <dt>

[<span data-ttu-id="e9909-134">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="e9909-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

