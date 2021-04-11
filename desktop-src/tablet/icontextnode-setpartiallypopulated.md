---
description: 修改指出此 ICoNtextNode 為部分或完整擴展的值。
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'ICoNtextNode：： SetPartiallyPopulated 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026252"
---
# <a name="icontextnodesetpartiallypopulated-method"></a><span data-ttu-id="4eb31-103">ICoNtextNode：： SetPartiallyPopulated 方法</span><span class="sxs-lookup"><span data-stu-id="4eb31-103">IContextNode::SetPartiallyPopulated method</span></span>

<span data-ttu-id="4eb31-104">修改指出此 [**ICoNtextNode**](icontextnode.md) 為部分或完整擴展的值。</span><span class="sxs-lookup"><span data-stu-id="4eb31-104">Modifies the value that indicates whether this [**IContextNode**](icontextnode.md) is partially or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb31-105">語法</span><span class="sxs-lookup"><span data-stu-id="4eb31-105">Syntax</span></span>


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="4eb31-106">參數</span><span class="sxs-lookup"><span data-stu-id="4eb31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eb31-107">*fPartiallyPopulated* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4eb31-107">*fPartiallyPopulated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4eb31-108">**變異 \_** 如果已部分填入此 [**ICoNtextNode**](icontextnode.md) ，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="4eb31-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) is partially populated; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eb31-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4eb31-109">Return value</span></span>

<span data-ttu-id="4eb31-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="4eb31-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb31-111">備註</span><span class="sxs-lookup"><span data-stu-id="4eb31-111">Remarks</span></span>

<span data-ttu-id="4eb31-112">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="4eb31-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="4eb31-113">如需詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="4eb31-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="4eb31-114">虛擬化您的檔樹狀結構時，請務必設定 PropertyGuidsForCoNtextNodes RotatedBoundingBox 值， (在所有 CoNtextNode 物件上使用 CoNtextNode. AddPropertyValue) 。</span><span class="sxs-lookup"><span data-stu-id="4eb31-114">When virtualizing your document tree, be sure to set the PropertyGuidsForContextNodes.RotatedBoundingBox value (using ContextNode.AddPropertyValue) on all ContextNode objects.</span></span> <span data-ttu-id="4eb31-115">RotatedBoundingBox 屬性是由 InkAnalyzer 計算，而且根據預設，應該在所有寫入 CoNtextNodes 上。</span><span class="sxs-lookup"><span data-stu-id="4eb31-115">The RotatedBoundingBox property is calculated by the InkAnalyzer and by default should be on all writing ContextNodes.</span></span> <span data-ttu-id="4eb31-116">但是，如果您的應用程式會藉由設定 PartiallyPopulated 屬性來虛擬化分析結果，則在處理 PopulateCoNtextNode 事件時，請務必填入 RotatedBoundingBox 屬性。</span><span class="sxs-lookup"><span data-stu-id="4eb31-116">However, if your application virtualizes the analysis results by setting the PartiallyPopulated property, when handling the PopulateContextNode event be sure to populate the RotatedBoundingBox property.</span></span> <span data-ttu-id="4eb31-117">若無法設定 RotatedBoundingBox 屬性，將會導致目前的分析作業中使用的檔資料可能更多</span><span class="sxs-lookup"><span data-stu-id="4eb31-117">Failure to set the RotatedBoundingBox property will result in potentially more document data being used in the current analysis operation</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb31-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="4eb31-118">Requirements</span></span>



| <span data-ttu-id="4eb31-119">需求</span><span class="sxs-lookup"><span data-stu-id="4eb31-119">Requirement</span></span> | <span data-ttu-id="4eb31-120">值</span><span class="sxs-lookup"><span data-stu-id="4eb31-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb31-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4eb31-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb31-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4eb31-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4eb31-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4eb31-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb31-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="4eb31-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4eb31-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4eb31-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb31-126"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="4eb31-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4eb31-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4eb31-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4eb31-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4eb31-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4eb31-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4eb31-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb31-130">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="4eb31-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4eb31-131">**\_IAnalysisProxyEvents：:P opulateCoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="4eb31-131">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="4eb31-132">**ICoNtextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="4eb31-132">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="4eb31-133">**ICoNtextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="4eb31-133">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="4eb31-134">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="4eb31-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




