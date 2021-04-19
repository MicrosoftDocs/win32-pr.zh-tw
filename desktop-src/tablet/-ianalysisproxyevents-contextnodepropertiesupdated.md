---
description: 在 IInkAnalyzer 更新 ICoNtextNode 物件的一或多個屬性之後發生。
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: '_IAnalysisProxyEvents：： CoNtextNodePropertiesUpdated 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106991948"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a><span data-ttu-id="66772-103">\_IAnalysisProxyEvents：： CoNtextNodePropertiesUpdated 事件</span><span class="sxs-lookup"><span data-stu-id="66772-103">\_IAnalysisProxyEvents::ContextNodePropertiesUpdated event</span></span>

<span data-ttu-id="66772-104">在 [**IInkAnalyzer**](iinkanalyzer.md) 更新 [**ICoNtextNode**](icontextnode.md) 物件的一或多個屬性之後發生。</span><span class="sxs-lookup"><span data-stu-id="66772-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="66772-105">語法</span><span class="sxs-lookup"><span data-stu-id="66772-105">Syntax</span></span>


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a><span data-ttu-id="66772-106">參數</span><span class="sxs-lookup"><span data-stu-id="66772-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66772-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66772-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66772-108">更新屬性的 [**IInkAnalyzer**](iinkanalyzer.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="66772-108">The [**IInkAnalyzer**](iinkanalyzer.md) object updating the properties.</span></span>

</dd> <dt>

<span data-ttu-id="66772-109">*pCoNtextNodeUpdated* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66772-109">*pContextNodeUpdated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66772-110">已更新其屬性的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="66772-110">The [**IContextNode**](icontextnode.md) object whose properties are updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66772-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="66772-111">Return value</span></span>

<span data-ttu-id="66772-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="66772-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="66772-113">備註</span><span class="sxs-lookup"><span data-stu-id="66772-113">Remarks</span></span>

<span data-ttu-id="66772-114">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="66772-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="66772-115">此事件發生于筆墨分析的協調階段，或為了回應變更 ([**ICoNtextNode**](icontextnode.md) 屬性的筆墨分析器方法，請參閱 [**ICoNtextNode：： GetPropertyData**](icontextnode-getpropertydata.md)) 。</span><span class="sxs-lookup"><span data-stu-id="66772-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that changes the properties of an [**IContextNode**](icontextnode.md) (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)).</span></span>

<span data-ttu-id="66772-116">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="66772-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66772-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="66772-117">Requirements</span></span>



| <span data-ttu-id="66772-118">需求</span><span class="sxs-lookup"><span data-stu-id="66772-118">Requirement</span></span> | <span data-ttu-id="66772-119">值</span><span class="sxs-lookup"><span data-stu-id="66772-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66772-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66772-120">Minimum supported client</span></span><br/> | <span data-ttu-id="66772-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66772-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="66772-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66772-122">Minimum supported server</span></span><br/> | <span data-ttu-id="66772-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="66772-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="66772-124">標頭</span><span class="sxs-lookup"><span data-stu-id="66772-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="66772-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="66772-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="66772-126">DLL</span><span class="sxs-lookup"><span data-stu-id="66772-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66772-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66772-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="66772-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66772-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66772-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="66772-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="66772-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="66772-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="66772-131">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="66772-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="66772-132">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="66772-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="66772-133">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="66772-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="66772-134">內容節點屬性</span><span class="sxs-lookup"><span data-stu-id="66772-134">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="66772-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="66772-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




