---
description: 實行 IInkAnalyzer 介面。
ms.assetid: f17de375-a0fe-4024-bf2a-60f8de8b0345
title: 'InkAnalyzer 類別 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalyzer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 49eeb04b1568bbef785f7d750315e0ea39491d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999851"
---
# <a name="inkanalyzer-class"></a><span data-ttu-id="c0ea4-103">InkAnalyzer 類別</span><span class="sxs-lookup"><span data-stu-id="c0ea4-103">InkAnalyzer class</span></span>

<span data-ttu-id="c0ea4-104">實行 [**IInkAnalyzer**](iinkanalyzer.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="c0ea4-104">Implements the [**IInkAnalyzer**](iinkanalyzer.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0ea4-105">備註</span><span class="sxs-lookup"><span data-stu-id="c0ea4-105">Remarks</span></span>

<span data-ttu-id="c0ea4-106">這個類別會實 [**IInkAnalyzer**](iinkanalyzer.md) COM 介面。</span><span class="sxs-lookup"><span data-stu-id="c0ea4-106">This class implements the [**IInkAnalyzer**](iinkanalyzer.md) COM interface.</span></span>

<span data-ttu-id="c0ea4-107">[ \_ IAnalysisEvents](-ianalysisevents.md)是事件的預設來源，並提供 [**IInkAnalyzer**](iinkanalyzer.md)的標準事件。</span><span class="sxs-lookup"><span data-stu-id="c0ea4-107">[\_IAnalysisEvents](-ianalysisevents.md) is the default source of events and provides standard events for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="c0ea4-108">[**\_ IAnalysisProxyEvents**](-ianalysisproxyevents.md)會提供 [**IInkAnalyzer**](iinkanalyzer.md)的資料 proxy 事件。</span><span class="sxs-lookup"><span data-stu-id="c0ea4-108">[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md) provides the data proxy events for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="c0ea4-109">如需詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="c0ea4-109">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ea4-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0ea4-110">Requirements</span></span>



| <span data-ttu-id="c0ea4-111">需求</span><span class="sxs-lookup"><span data-stu-id="c0ea4-111">Requirement</span></span> | <span data-ttu-id="c0ea4-112">值</span><span class="sxs-lookup"><span data-stu-id="c0ea4-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ea4-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0ea4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ea4-114">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0ea4-114">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c0ea4-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0ea4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ea4-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="c0ea4-116">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c0ea4-117">標頭</span><span class="sxs-lookup"><span data-stu-id="c0ea4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0ea4-118"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c0ea4-118"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c0ea4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c0ea4-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0ea4-120"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0ea4-120"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c0ea4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0ea4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ea4-122">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="c0ea4-122">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="c0ea4-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="c0ea4-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="c0ea4-124">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="c0ea4-124">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="c0ea4-125">**ICoNtextLink**</span><span class="sxs-lookup"><span data-stu-id="c0ea4-125">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="c0ea4-126">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="c0ea4-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c0ea4-127">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="c0ea4-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




