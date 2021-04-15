---
description: 判斷 IAnalysisRegion 的區域是否與指定的矩形相交。
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'IAnalysisRegion：： IntersectsWith 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511696"
---
# <a name="ianalysisregionintersectswith-method"></a><span data-ttu-id="04d71-103">IAnalysisRegion：： IntersectsWith 方法</span><span class="sxs-lookup"><span data-stu-id="04d71-103">IAnalysisRegion::IntersectsWith method</span></span>

<span data-ttu-id="04d71-104">判斷 [**IAnalysisRegion**](ianalysisregion.md) 的區域是否與指定的矩形相交。</span><span class="sxs-lookup"><span data-stu-id="04d71-104">Determines whether the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d71-105">語法</span><span class="sxs-lookup"><span data-stu-id="04d71-105">Syntax</span></span>


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a><span data-ttu-id="04d71-106">參數</span><span class="sxs-lookup"><span data-stu-id="04d71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d71-107">*pRectangle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04d71-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04d71-108">要與之比較的矩形指標，以筆墨的空格座標表示。</span><span class="sxs-lookup"><span data-stu-id="04d71-108">A pointer to the rectangle with which to compare, in ink-space coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="04d71-109">*pfIsIntersecting* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="04d71-109">*pfIsIntersecting* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04d71-110">**變異 \_** 如果 [**IAnalysisRegion**](ianalysisregion.md)的區域與指定的矩形相交，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="04d71-110">**VARIANT\_TRUE** if the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d71-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="04d71-111">Return value</span></span>

<span data-ttu-id="04d71-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="04d71-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04d71-113">備註</span><span class="sxs-lookup"><span data-stu-id="04d71-113">Remarks</span></span>

<span data-ttu-id="04d71-114">比較是以筆墨空間座標表示。</span><span class="sxs-lookup"><span data-stu-id="04d71-114">The comparison is in ink-space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="04d71-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="04d71-115">Requirements</span></span>



| <span data-ttu-id="04d71-116">需求</span><span class="sxs-lookup"><span data-stu-id="04d71-116">Requirement</span></span> | <span data-ttu-id="04d71-117">值</span><span class="sxs-lookup"><span data-stu-id="04d71-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d71-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04d71-118">Minimum supported client</span></span><br/> | <span data-ttu-id="04d71-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04d71-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="04d71-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04d71-120">Minimum supported server</span></span><br/> | <span data-ttu-id="04d71-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="04d71-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="04d71-122">標頭</span><span class="sxs-lookup"><span data-stu-id="04d71-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="04d71-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="04d71-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="04d71-124">DLL</span><span class="sxs-lookup"><span data-stu-id="04d71-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04d71-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04d71-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="04d71-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04d71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d71-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="04d71-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="04d71-128">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="04d71-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




