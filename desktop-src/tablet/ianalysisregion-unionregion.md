---
description: 將這個 IAnalysisRegion 的區域展開至具有指定 IAnalysisRegion 的聯集所建立的區域。
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'IAnalysisRegion：： UnionRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 587986973c4ae4bebaeed3c031c746bc4f842c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973289"
---
# <a name="ianalysisregionunionregion-method"></a><span data-ttu-id="97e3c-103">IAnalysisRegion：： UnionRegion 方法</span><span class="sxs-lookup"><span data-stu-id="97e3c-103">IAnalysisRegion::UnionRegion method</span></span>

<span data-ttu-id="97e3c-104">將這個 [**IAnalysisRegion**](ianalysisregion.md) 的區域展開至具有指定 **IAnalysisRegion** 的聯集所建立的區域。</span><span class="sxs-lookup"><span data-stu-id="97e3c-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="97e3c-105">語法</span><span class="sxs-lookup"><span data-stu-id="97e3c-105">Syntax</span></span>


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a><span data-ttu-id="97e3c-106">參數</span><span class="sxs-lookup"><span data-stu-id="97e3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97e3c-107">*pRegionToUnion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97e3c-107">*pRegionToUnion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97e3c-108">要合併的 [**IAnalysisRegion**](ianalysisregion.md) 。</span><span class="sxs-lookup"><span data-stu-id="97e3c-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to combine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97e3c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="97e3c-109">Return value</span></span>

<span data-ttu-id="97e3c-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="97e3c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="97e3c-111">備註</span><span class="sxs-lookup"><span data-stu-id="97e3c-111">Remarks</span></span>

<span data-ttu-id="97e3c-112">如果任一區域都是無限的，則新區域也是無限的。</span><span class="sxs-lookup"><span data-stu-id="97e3c-112">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e3c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="97e3c-113">Requirements</span></span>



| <span data-ttu-id="97e3c-114">需求</span><span class="sxs-lookup"><span data-stu-id="97e3c-114">Requirement</span></span> | <span data-ttu-id="97e3c-115">值</span><span class="sxs-lookup"><span data-stu-id="97e3c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97e3c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97e3c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="97e3c-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97e3c-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="97e3c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97e3c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="97e3c-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="97e3c-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="97e3c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="97e3c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="97e3c-121"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="97e3c-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="97e3c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="97e3c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97e3c-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97e3c-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="97e3c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97e3c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e3c-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="97e3c-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="97e3c-126">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="97e3c-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="97e3c-127">**IAnalysisRegion：： ExcludeRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="97e3c-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="97e3c-128">**IAnalysisRegion：： IntersectRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="97e3c-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="97e3c-129">**IAnalysisRegion：： IntersectRegion 方法**</span><span class="sxs-lookup"><span data-stu-id="97e3c-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="97e3c-130">**IAnalysisRegion：： UnionRectangle 方法**</span><span class="sxs-lookup"><span data-stu-id="97e3c-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="97e3c-131">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="97e3c-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




