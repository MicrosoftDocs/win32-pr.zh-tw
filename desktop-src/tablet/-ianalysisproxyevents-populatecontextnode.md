---
description: 發生于 IInkAnalyzer 在部分填入的 ICoNtextNode 物件區域內執行分析之前。
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: '_IAnalysisProxyEvents：:P opulateCoNtextNode 事件 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e8aebe4ba777d62f90aa00c45ea0f1644e2b8183
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104195800"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a><span data-ttu-id="95c99-103">\_IAnalysisProxyEvents：:P opulateCoNtextNode 事件</span><span class="sxs-lookup"><span data-stu-id="95c99-103">\_IAnalysisProxyEvents::PopulateContextNode event</span></span>

<span data-ttu-id="95c99-104">發生于 [**IInkAnalyzer**](iinkanalyzer.md) 在部分填入的 [**ICoNtextNode**](icontextnode.md) 物件區域內執行分析之前。</span><span class="sxs-lookup"><span data-stu-id="95c99-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="95c99-105">語法</span><span class="sxs-lookup"><span data-stu-id="95c99-105">Syntax</span></span>


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a><span data-ttu-id="95c99-106">參數</span><span class="sxs-lookup"><span data-stu-id="95c99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95c99-107">*pInkAnalyzer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95c99-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c99-108">要執行分析的 [**IInkAnalyzer**](iinkanalyzer.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="95c99-108">The [**IInkAnalyzer**](iinkanalyzer.md) object about to perform analysis.</span></span>

</dd> <dt>

<span data-ttu-id="95c99-109">*pCoNtextNodeToPopulate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95c99-109">*pContextNodeToPopulate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95c99-110">部分填入的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="95c99-110">The partially populated [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95c99-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95c99-111">Return value</span></span>

<span data-ttu-id="95c99-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="95c99-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95c99-113">備註</span><span class="sxs-lookup"><span data-stu-id="95c99-113">Remarks</span></span>

<span data-ttu-id="95c99-114">當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用此事件。</span><span class="sxs-lookup"><span data-stu-id="95c99-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="95c99-115">當 **IInkAnalyzer** 引發這個事件時，您的應用程式應該會填入 *pCoNtextNodeToPopulate*。</span><span class="sxs-lookup"><span data-stu-id="95c99-115">When the **IInkAnalyzer** raises this event, your application should populate the *pContextNodeToPopulate*.</span></span> <span data-ttu-id="95c99-116">在分析階段， **IInkAnalyzer** 會引發此事件，以取得其正在分析筆墨之區域的資訊。</span><span class="sxs-lookup"><span data-stu-id="95c99-116">During the analysis phase, the **IInkAnalyzer** raises this event to get information for areas in which it is analyzing ink.</span></span>

<span data-ttu-id="95c99-117">如果檔包含 *pCoNtextNodeToPopulate* 的連結，您的應用程式應該建立並新增這些連結。</span><span class="sxs-lookup"><span data-stu-id="95c99-117">If the document contains links for the *pContextNodeToPopulate*, your application should create and add these links.</span></span> <span data-ttu-id="95c99-118">此程式需要來源和目的地節點（包括其祖系）在這個事件的事件處理常式結束之前完全填入 (請參閱 [**ICoNtextLink：： GetSourceNode**](icontextlink-getsourcenode.md) 和 [**ICoNtextLink：： GetDestinationNode**](icontextlink-getdestinationnode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="95c99-118">This process requires that both the source and destination nodes, including their ancestors, are fully populated before the event handler for this event exits (see [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) and [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).</span></span>

<span data-ttu-id="95c99-119">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="95c99-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="95c99-120">在背景分析期間， [**IInkAnalyzer**](iinkanalyzer.md)會在引發 [**\_ IAnalysisEvents：： ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)事件之後引發此事件。</span><span class="sxs-lookup"><span data-stu-id="95c99-120">During background analysis, the [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="95c99-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="95c99-121">Requirements</span></span>



| <span data-ttu-id="95c99-122">需求</span><span class="sxs-lookup"><span data-stu-id="95c99-122">Requirement</span></span> | <span data-ttu-id="95c99-123">值</span><span class="sxs-lookup"><span data-stu-id="95c99-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95c99-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95c99-124">Minimum supported client</span></span><br/> | <span data-ttu-id="95c99-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95c99-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="95c99-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95c99-126">Minimum supported server</span></span><br/> | <span data-ttu-id="95c99-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="95c99-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="95c99-128">標頭</span><span class="sxs-lookup"><span data-stu-id="95c99-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="95c99-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="95c99-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="95c99-130">DLL</span><span class="sxs-lookup"><span data-stu-id="95c99-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95c99-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95c99-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="95c99-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95c99-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c99-133">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="95c99-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="95c99-134">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="95c99-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="95c99-135">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="95c99-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="95c99-136">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="95c99-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="95c99-137">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="95c99-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="95c99-138">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="95c99-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




