---
description: 在筆跡分析器于兩個 ICoNtextNode 物件之間加入 ICoNtextLink 物件之前發生。
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: '_IAnalysisProxyEvents：： CoNtextNodeLinkAdding 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 341c551064869532e8b51ddecdbe1d5a78878abd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106995884"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a><span data-ttu-id="8dd61-103">\_IAnalysisProxyEvents：： CoNtextNodeLinkAdding 事件</span><span class="sxs-lookup"><span data-stu-id="8dd61-103">\_IAnalysisProxyEvents::ContextNodeLinkAdding event</span></span>

<span data-ttu-id="8dd61-104">在筆跡分析器于兩個 [**ICoNtextNode**](icontextnode.md)物件之間加入 [**ICoNtextLink**](icontextlink.md)物件之前發生。</span><span class="sxs-lookup"><span data-stu-id="8dd61-104">Occurs before the ink analyzer adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dd61-105">語法</span><span class="sxs-lookup"><span data-stu-id="8dd61-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a><span data-ttu-id="8dd61-106">參數</span><span class="sxs-lookup"><span data-stu-id="8dd61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dd61-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8dd61-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd61-108">新增連結的 [**IInkAnalyzer**](iinkanalyzer.md) 。</span><span class="sxs-lookup"><span data-stu-id="8dd61-108">The [**IInkAnalyzer**](iinkanalyzer.md) adding the link.</span></span>

</dd> <dt>

<span data-ttu-id="8dd61-109">*pCoNtextLinkToBeAdded* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8dd61-109">*pContextLinkToBeAdded* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dd61-110">要加入的 [**ICoNtextLink**](icontextlink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="8dd61-110">The [**IContextLink**](icontextlink.md) object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dd61-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8dd61-111">Return value</span></span>

<span data-ttu-id="8dd61-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="8dd61-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8dd61-113">備註</span><span class="sxs-lookup"><span data-stu-id="8dd61-113">Remarks</span></span>

<span data-ttu-id="8dd61-114">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="8dd61-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="8dd61-115">此事件發生于筆墨分析的協調階段，或為了回應將新的 [**ICoNtextLink**](icontextlink.md) 新增至 [**ICoNtextNode**](icontextnode.md)的筆墨分析器方法。</span><span class="sxs-lookup"><span data-stu-id="8dd61-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that adds a new [**IContextLink**](icontextlink.md) to an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="8dd61-116">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="8dd61-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8dd61-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8dd61-117">Requirements</span></span>



| <span data-ttu-id="8dd61-118">需求</span><span class="sxs-lookup"><span data-stu-id="8dd61-118">Requirement</span></span> | <span data-ttu-id="8dd61-119">值</span><span class="sxs-lookup"><span data-stu-id="8dd61-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd61-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8dd61-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8dd61-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8dd61-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8dd61-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8dd61-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8dd61-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="8dd61-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8dd61-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8dd61-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dd61-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="8dd61-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8dd61-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8dd61-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dd61-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dd61-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8dd61-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8dd61-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dd61-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="8dd61-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="8dd61-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8dd61-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8dd61-131">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="8dd61-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8dd61-132">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="8dd61-132">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="8dd61-133">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="8dd61-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="8dd61-134">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="8dd61-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="8dd61-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="8dd61-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




