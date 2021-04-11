---
description: 變更指定之筆劃的型別。
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'IInkAnalyzer：： SetStrokeType 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a5f77cbefb200bad973c0f2cf28fea5d3efe1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113320"
---
# <a name="iinkanalyzersetstroketype-method"></a><span data-ttu-id="e41dd-103">IInkAnalyzer：： SetStrokeType 方法</span><span class="sxs-lookup"><span data-stu-id="e41dd-103">IInkAnalyzer::SetStrokeType method</span></span>

<span data-ttu-id="e41dd-104">變更指定之筆劃的型別。</span><span class="sxs-lookup"><span data-stu-id="e41dd-104">Changes the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="e41dd-105">語法</span><span class="sxs-lookup"><span data-stu-id="e41dd-105">Syntax</span></span>


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="e41dd-106">參數</span><span class="sxs-lookup"><span data-stu-id="e41dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e41dd-107">*lStrokeId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e41dd-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41dd-108">要指派 *StrokeType* 之筆劃的筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="e41dd-108">The stroke identifier of the stroke to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="e41dd-109">*StrokeType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e41dd-109">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41dd-110">要指派給筆劃的 [**StrokeType**](stroketype.md) 值。</span><span class="sxs-lookup"><span data-stu-id="e41dd-110">The [**StrokeType**](stroketype.md) value to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e41dd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e41dd-111">Return value</span></span>

<span data-ttu-id="e41dd-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="e41dd-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e41dd-113">備註</span><span class="sxs-lookup"><span data-stu-id="e41dd-113">Remarks</span></span>

<span data-ttu-id="e41dd-114">如果筆劃的類型是 [**StrokeType**](stroketype.md) 值 StrokeType 非 **\_ 分類**，則 [**IInkAnalyzer**](iinkanalyzer.md) 會在筆跡分析期間將筆劃分類。</span><span class="sxs-lookup"><span data-stu-id="e41dd-114">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="e41dd-115">否則， **IInkAnalyzer** 會使用筆劃上設定的類型。</span><span class="sxs-lookup"><span data-stu-id="e41dd-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="e41dd-116">[**IInkAnalyzer**](iinkanalyzer.md)不會將筆劃類型值設定為筆跡分析的一部分。</span><span class="sxs-lookup"><span data-stu-id="e41dd-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="e41dd-117">若要指定或變更筆觸類型，請使用 **IInkAnalyzer：： SetStrokeType 方法** 或 [**IInkAnalyzer：： SetStrokesType 方法**](iinkanalyzer-setstrokestype.md)。</span><span class="sxs-lookup"><span data-stu-id="e41dd-117">To specify or change the stroke type, use **IInkAnalyzer::SetStrokeType Method** or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

<span data-ttu-id="e41dd-118">如果筆劃與非未分類筆墨節點的 [**ICoNtextNode**](icontextnode.md) 相關聯 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) ，這個方法會將筆劃移至包含相同語言之筆觸的非分類筆墨節點。</span><span class="sxs-lookup"><span data-stu-id="e41dd-118">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="e41dd-119">如果沒有這類內容節點，這個方法會建立新的非分類筆墨節點，並將筆劃加入其中。</span><span class="sxs-lookup"><span data-stu-id="e41dd-119">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="e41dd-120">未分類的筆墨節點是 UnclassifiedInk 類型的 **ICoNtextNode** 。</span><span class="sxs-lookup"><span data-stu-id="e41dd-120">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="e41dd-121">如果這個方法從非未分類筆墨節點的 [**ICoNtextNode**](icontextnode.md) 移動筆劃，此方法也會將筆劃的周框方塊新增至 ink 分析器的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。</span><span class="sxs-lookup"><span data-stu-id="e41dd-121">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="e41dd-122">如果 *StrokeType* 參數符合筆觸的目前型別，則這個方法不會移動筆劃。</span><span class="sxs-lookup"><span data-stu-id="e41dd-122">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="e41dd-123">在與已 NodeTypeAndProperties 確認的 CoNtextNode 相關聯的筆劃上設定筆劃類型，將會引發 InvalidOperationException。</span><span class="sxs-lookup"><span data-stu-id="e41dd-123">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="e41dd-124">如果指定的筆劃沒有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會傳回而不更新 **IInkAnalyzer**。</span><span class="sxs-lookup"><span data-stu-id="e41dd-124">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e41dd-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e41dd-125">Requirements</span></span>



| <span data-ttu-id="e41dd-126">需求</span><span class="sxs-lookup"><span data-stu-id="e41dd-126">Requirement</span></span> | <span data-ttu-id="e41dd-127">值</span><span class="sxs-lookup"><span data-stu-id="e41dd-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e41dd-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e41dd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e41dd-129">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e41dd-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e41dd-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e41dd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e41dd-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="e41dd-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e41dd-132">標頭</span><span class="sxs-lookup"><span data-stu-id="e41dd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e41dd-133"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e41dd-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e41dd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e41dd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e41dd-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e41dd-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e41dd-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e41dd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41dd-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e41dd-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e41dd-138">**IInkAnalyzer：： GetStrokeType 方法**</span><span class="sxs-lookup"><span data-stu-id="e41dd-138">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="e41dd-139">**IInkAnalyzer：： SetStrokesType 方法**</span><span class="sxs-lookup"><span data-stu-id="e41dd-139">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="e41dd-140">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="e41dd-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




