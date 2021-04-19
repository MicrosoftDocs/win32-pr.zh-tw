---
description: 在可辨識的字串中尋找對應于 ICoNtextNode 物件集合的文字範圍。
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'IInkAnalyzer：： GetTextRangeFromNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da27206a33ca58cebd10192393c4cf2efd1d5919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973287"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a><span data-ttu-id="d16cd-103">IInkAnalyzer：： GetTextRangeFromNodes 方法</span><span class="sxs-lookup"><span data-stu-id="d16cd-103">IInkAnalyzer::GetTextRangeFromNodes method</span></span>

<span data-ttu-id="d16cd-104">在可辨識的字串中尋找對應于 [**ICoNtextNode**](icontextnode.md) 物件集合的文字範圍。</span><span class="sxs-lookup"><span data-stu-id="d16cd-104">Finds the text range in the recognized string that corresponds to a collection of [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="d16cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="d16cd-105">Syntax</span></span>


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a><span data-ttu-id="d16cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="d16cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d16cd-107">*plStart* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d16cd-107">*plStart* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d16cd-108">表示文字範圍開頭的32位帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="d16cd-108">A 32-bit signed integer that indicates the start of the text range.</span></span> <span data-ttu-id="d16cd-109">這個參數會以未初始化的狀態傳遞。</span><span class="sxs-lookup"><span data-stu-id="d16cd-109">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="d16cd-110">*plLength* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d16cd-110">*plLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d16cd-111">表示文字範圍長度的32位帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="d16cd-111">A 32-bit signed integer that indicates the length of the text range.</span></span> <span data-ttu-id="d16cd-112">這個參數會以未初始化的狀態傳遞。</span><span class="sxs-lookup"><span data-stu-id="d16cd-112">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="d16cd-113">*pNodesToSearch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d16cd-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d16cd-114">要尋找其文字範圍之 [**ICoNtextNode**](icontextnode.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="d16cd-114">The collection of [**IContextNode**](icontextnode.md) objects for which to find the text range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d16cd-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d16cd-115">Return value</span></span>

<span data-ttu-id="d16cd-116">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="d16cd-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d16cd-117">備註</span><span class="sxs-lookup"><span data-stu-id="d16cd-117">Remarks</span></span>

<span data-ttu-id="d16cd-118">如果 *pNodesToSearch* 包含不連續的 [**ICoNtextNode**](icontextnode.md) 物件，這個方法會傳回最小的文字範圍，其中涵蓋所有的 **ICoNtextNode** 物件。</span><span class="sxs-lookup"><span data-stu-id="d16cd-118">If *pNodesToSearch* contains [**IContextNode**](icontextnode.md) objects that are not adjacent, this method returns the smallest text range that covers all of the **IContextNode** objects.</span></span>

<span data-ttu-id="d16cd-119">\_當 *pNodesToSearch* 包含未與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的 [**ICoNtextNode**](icontextnode.md)時，這個方法會擲回 E INVALIDARG 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="d16cd-119">This method throws an E\_INVALIDARG exception when *pNodesToSearch* contains an [**IContextNode**](icontextnode.md) that is not associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d16cd-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d16cd-120">Requirements</span></span>



| <span data-ttu-id="d16cd-121">需求</span><span class="sxs-lookup"><span data-stu-id="d16cd-121">Requirement</span></span> | <span data-ttu-id="d16cd-122">值</span><span class="sxs-lookup"><span data-stu-id="d16cd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d16cd-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d16cd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d16cd-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d16cd-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d16cd-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d16cd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d16cd-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="d16cd-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d16cd-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d16cd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d16cd-128"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d16cd-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d16cd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d16cd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d16cd-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d16cd-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d16cd-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d16cd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d16cd-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d16cd-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




