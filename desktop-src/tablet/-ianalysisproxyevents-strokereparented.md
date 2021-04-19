---
description: 當 IInkAnalyzer 將筆劃從一個 ICoNtextNode 物件移動到另一個時，就會發生。
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: '_IAnalysisProxyEvents：： StrokeReparented 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a587acb6534641d5d64981ab25247b0e23e4f347
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106982815"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a><span data-ttu-id="04515-103">\_IAnalysisProxyEvents：： StrokeReparented 事件</span><span class="sxs-lookup"><span data-stu-id="04515-103">\_IAnalysisProxyEvents::StrokeReparented event</span></span>

<span data-ttu-id="04515-104">當 [**IInkAnalyzer**](iinkanalyzer.md) 將筆劃從一個 [**ICoNtextNode**](icontextnode.md) 物件移動到另一個時，就會發生。</span><span class="sxs-lookup"><span data-stu-id="04515-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="04515-105">語法</span><span class="sxs-lookup"><span data-stu-id="04515-105">Syntax</span></span>


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="04515-106">參數</span><span class="sxs-lookup"><span data-stu-id="04515-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04515-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04515-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04515-108">移動筆劃的 [**IInkAnalyzer**](iinkanalyzer.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="04515-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="04515-109">*lStrokeIdToMove* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04515-109">*lStrokeIdToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04515-110">要移動之筆劃的識別碼。</span><span class="sxs-lookup"><span data-stu-id="04515-110">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="04515-111">*pSourceCoNtextNode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04515-111">*pSourceContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04515-112">要從中移動筆劃的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="04515-112">The [**IContextNode**](icontextnode.md) object from which the stroke is moved.</span></span>

</dd> <dt>

<span data-ttu-id="04515-113">*pDestinationCoNtextNode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04515-113">*pDestinationContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04515-114">要將筆劃移動至其中的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="04515-114">The [**IContextNode**](icontextnode.md) object to which the stroke is moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04515-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="04515-115">Return value</span></span>

<span data-ttu-id="04515-116">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="04515-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="04515-117">備註</span><span class="sxs-lookup"><span data-stu-id="04515-117">Remarks</span></span>

<span data-ttu-id="04515-118">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="04515-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="04515-119">此事件發生于筆墨分析的協調階段，或為了回應將筆劃資料從一個 ICoNtextNode 移至另一個 [](icontextnode.md)的 **IInkAnalyzer** 方法。</span><span class="sxs-lookup"><span data-stu-id="04515-119">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that moves stroke data from one [**IContextNode**](icontextnode.md) to another.</span></span>

<span data-ttu-id="04515-120">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="04515-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04515-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="04515-121">Requirements</span></span>



| <span data-ttu-id="04515-122">需求</span><span class="sxs-lookup"><span data-stu-id="04515-122">Requirement</span></span> | <span data-ttu-id="04515-123">值</span><span class="sxs-lookup"><span data-stu-id="04515-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04515-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04515-124">Minimum supported client</span></span><br/> | <span data-ttu-id="04515-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04515-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="04515-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04515-126">Minimum supported server</span></span><br/> | <span data-ttu-id="04515-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="04515-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="04515-128">標頭</span><span class="sxs-lookup"><span data-stu-id="04515-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="04515-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="04515-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="04515-130">DLL</span><span class="sxs-lookup"><span data-stu-id="04515-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04515-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04515-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="04515-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04515-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04515-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="04515-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="04515-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="04515-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="04515-135">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="04515-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="04515-136">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="04515-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="04515-137">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="04515-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="04515-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="04515-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




