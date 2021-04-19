---
description: 在 IInkAnalyzer 存取筆劃資料之前發生。
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: '_IAnalysisEvents：： UpdateStrokesCache 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5d16011d8c5fe571d228b632fecb7a973bafcbf5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106981755"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a><span data-ttu-id="c6710-103">\_IAnalysisEvents：： UpdateStrokesCache 事件</span><span class="sxs-lookup"><span data-stu-id="c6710-103">\_IAnalysisEvents::UpdateStrokesCache event</span></span>

<span data-ttu-id="c6710-104">在 [**IInkAnalyzer**](iinkanalyzer.md) 存取筆劃資料之前發生。</span><span class="sxs-lookup"><span data-stu-id="c6710-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6710-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6710-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="c6710-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6710-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6710-107">*ulStrokeIdsCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6710-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6710-108">*PlStrokeIds* 中的筆觸識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="c6710-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="c6710-109">*plStrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6710-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6710-110">已清除其封包資料之筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c6710-110">The identifiers of the strokes whose packet data has been cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6710-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6710-111">Return value</span></span>

<span data-ttu-id="c6710-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c6710-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6710-113">備註</span><span class="sxs-lookup"><span data-stu-id="c6710-113">Remarks</span></span>

<span data-ttu-id="c6710-114">當您存取已清除封包資料的一或多個筆劃時， [**IInkAnalyzer**](iinkanalyzer.md) 會在筆跡分析期間引發此事件。</span><span class="sxs-lookup"><span data-stu-id="c6710-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during ink analysis when it accesses one or more strokes for which the packet data has been cleared.</span></span> <span data-ttu-id="c6710-115">若要更新筆劃封包資料，請使用 [**IInkAnalyzer：： UpdateStrokesData 方法**](iinkanalyzer-updatestrokesdata.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c6710-115">To update the stroke packet data, use the [**IInkAnalyzer::UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) method.</span></span>

<span data-ttu-id="c6710-116">當 **IInkAnalyzer** 尚未設定節點的位置時， [**IInkAnalyzer**](iinkanalyzer.md)不會在存取部分填入的筆墨分葉節點時引發這個事件。</span><span class="sxs-lookup"><span data-stu-id="c6710-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise this event when accessing a partially populated ink leaf node when the location of the node has not been set by the **IInkAnalyzer**.</span></span>

<span data-ttu-id="c6710-117">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c6710-117">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6710-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6710-118">Requirements</span></span>



| <span data-ttu-id="c6710-119">需求</span><span class="sxs-lookup"><span data-stu-id="c6710-119">Requirement</span></span> | <span data-ttu-id="c6710-120">值</span><span class="sxs-lookup"><span data-stu-id="c6710-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6710-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6710-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c6710-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6710-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c6710-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6710-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c6710-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="c6710-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c6710-125">標頭</span><span class="sxs-lookup"><span data-stu-id="c6710-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6710-126"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c6710-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c6710-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c6710-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6710-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6710-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c6710-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6710-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6710-130">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="c6710-130">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="c6710-131">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="c6710-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="c6710-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c6710-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c6710-133">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="c6710-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="c6710-134">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="c6710-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="c6710-135">**IInkAnalyzer：： UpdateStrokesData 方法**</span><span class="sxs-lookup"><span data-stu-id="c6710-135">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="c6710-136">**ICoNtextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="c6710-136">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="c6710-137">**ICoNtextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="c6710-137">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="c6710-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="c6710-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




