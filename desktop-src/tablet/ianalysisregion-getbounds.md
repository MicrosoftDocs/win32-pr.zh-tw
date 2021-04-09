---
description: 取得 IAnalysisRegion 的周框。
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'IAnalysisRegion：： GetBounds 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690615"
---
# <a name="ianalysisregiongetbounds-method"></a><span data-ttu-id="3ee28-103">IAnalysisRegion：： GetBounds 方法</span><span class="sxs-lookup"><span data-stu-id="3ee28-103">IAnalysisRegion::GetBounds method</span></span>

<span data-ttu-id="3ee28-104">取得 [**IAnalysisRegion**](ianalysisregion.md)的周框。</span><span class="sxs-lookup"><span data-stu-id="3ee28-104">Gets the bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ee28-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ee28-105">Syntax</span></span>


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="3ee28-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ee28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ee28-107">*pBoundingRectangle* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3ee28-107">*pBoundingRectangle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee28-108">[**IAnalysisRegion**](ianalysisregion.md)的周框（以筆墨空間座標表示）。</span><span class="sxs-lookup"><span data-stu-id="3ee28-108">The bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md) in ink space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ee28-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ee28-109">Return value</span></span>

<span data-ttu-id="3ee28-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="3ee28-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ee28-111">備註</span><span class="sxs-lookup"><span data-stu-id="3ee28-111">Remarks</span></span>

<span data-ttu-id="3ee28-112">範圍是以筆墨空間座標表示。</span><span class="sxs-lookup"><span data-stu-id="3ee28-112">The bounds are in ink-space coordinates.</span></span>

<span data-ttu-id="3ee28-113">如果 [**IAnalysisRegion**](ianalysisregion.md) 代表無限區域，則左側和頂端界限為 **int \_ MIN**，右邊和下界限則為 **int \_ MAX**。</span><span class="sxs-lookup"><span data-stu-id="3ee28-113">If the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite area, the left and top bounds are **INT\_MIN**; and the right and bottom bounds are **INT\_MAX**.</span></span>

<span data-ttu-id="3ee28-114">如果 [**IAnalysisRegion**](ianalysisregion.md) 代表空白區域，則矩形的所有界限都是0。</span><span class="sxs-lookup"><span data-stu-id="3ee28-114">If the [**IAnalysisRegion**](ianalysisregion.md) represents an empty area, all the bounds of the rectangle are 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ee28-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ee28-115">Requirements</span></span>



| <span data-ttu-id="3ee28-116">需求</span><span class="sxs-lookup"><span data-stu-id="3ee28-116">Requirement</span></span> | <span data-ttu-id="3ee28-117">值</span><span class="sxs-lookup"><span data-stu-id="3ee28-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee28-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ee28-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3ee28-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ee28-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3ee28-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ee28-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3ee28-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="3ee28-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3ee28-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3ee28-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ee28-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="3ee28-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3ee28-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3ee28-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ee28-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ee28-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3ee28-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ee28-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee28-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="3ee28-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="3ee28-128">**IAnalysisRegion：： GetRegionScans 方法**</span><span class="sxs-lookup"><span data-stu-id="3ee28-128">**IAnalysisRegion::GetRegionScans Method**</span></span>](ianalysisregion-getregionscans.md)
</dt> <dt>

[<span data-ttu-id="3ee28-129">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="3ee28-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




