---
description: 在 IInkAnalyzer 刪除兩個 ICoNtextNode 物件之間的 ICoNtextLink 物件之前發生。
ms.assetid: bc9716b8-8793-4886-aff4-d880024129a6
title: '_IAnalysisProxyEvents：： CoNtextNodeLinkDeleting 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc4ba9586fc4c520b9ee44b039bd56f8ef2ade3c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195791"
---
# <a name="_ianalysisproxyeventscontextnodelinkdeleting-event"></a><span data-ttu-id="d2e74-103">\_IAnalysisProxyEvents：： CoNtextNodeLinkDeleting 事件</span><span class="sxs-lookup"><span data-stu-id="d2e74-103">\_IAnalysisProxyEvents::ContextNodeLinkDeleting event</span></span>

<span data-ttu-id="d2e74-104">在 [**IInkAnalyzer**](iinkanalyzer.md)刪除兩個 [**ICoNtextNode**](icontextnode.md)物件之間的 [**ICoNtextLink**](icontextlink.md)物件之前發生。</span><span class="sxs-lookup"><span data-stu-id="d2e74-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2e74-105">語法</span><span class="sxs-lookup"><span data-stu-id="d2e74-105">Syntax</span></span>


```C++
HRESULT ContextNodeLinkDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeDeleted
);
```



## <a name="parameters"></a><span data-ttu-id="d2e74-106">參數</span><span class="sxs-lookup"><span data-stu-id="d2e74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2e74-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2e74-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2e74-108">刪除連結的 [**IInkAnalyzer**](iinkanalyzer.md) 。</span><span class="sxs-lookup"><span data-stu-id="d2e74-108">The [**IInkAnalyzer**](iinkanalyzer.md) deleting the link.</span></span>

</dd> <dt>

<span data-ttu-id="d2e74-109">*pCoNtextLinkToBeDeleted* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2e74-109">*pContextLinkToBeDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2e74-110">要刪除的 [**ICoNtextLink**](icontextlink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d2e74-110">The [**IContextLink**](icontextlink.md) object to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2e74-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2e74-111">Return value</span></span>

<span data-ttu-id="d2e74-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="d2e74-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d2e74-113">備註</span><span class="sxs-lookup"><span data-stu-id="d2e74-113">Remarks</span></span>

<span data-ttu-id="d2e74-114">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="d2e74-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="d2e74-115">此事件發生于筆墨分析的協調階段，或為了回應從 [**ICoNtextNode**](icontextnode.md)移除 [**ICoNtextLink**](icontextlink.md)的 **IInkAnalyzer** 方法。</span><span class="sxs-lookup"><span data-stu-id="d2e74-115">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that removes an [**IContextLink**](icontextlink.md) from an [**IContextNode**](icontextnode.md).</span></span>

<span data-ttu-id="d2e74-116">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="d2e74-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2e74-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2e74-117">Requirements</span></span>



| <span data-ttu-id="d2e74-118">需求</span><span class="sxs-lookup"><span data-stu-id="d2e74-118">Requirement</span></span> | <span data-ttu-id="d2e74-119">值</span><span class="sxs-lookup"><span data-stu-id="d2e74-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e74-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2e74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d2e74-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2e74-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d2e74-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2e74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d2e74-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="d2e74-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d2e74-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d2e74-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2e74-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d2e74-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d2e74-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d2e74-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2e74-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2e74-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d2e74-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2e74-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e74-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="d2e74-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="d2e74-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d2e74-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d2e74-131">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="d2e74-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="d2e74-132">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="d2e74-132">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d2e74-133">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="d2e74-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="d2e74-134">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="d2e74-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="d2e74-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="d2e74-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




