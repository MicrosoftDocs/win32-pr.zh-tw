---
description: 包含物件的集合，這些物件會執行 IAnalysisAlternate 介面，且為筆跡分析的結果。
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: 'IAnalysisAlternates 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970825"
---
# <a name="ianalysisalternates-interface"></a><span data-ttu-id="3e6a3-103">IAnalysisAlternates 介面</span><span class="sxs-lookup"><span data-stu-id="3e6a3-103">IAnalysisAlternates interface</span></span>

<span data-ttu-id="3e6a3-104">包含物件的集合，這些物件會執行 [**IAnalysisAlternate**](ianalysisalternate.md) 介面，且為筆跡分析的結果。</span><span class="sxs-lookup"><span data-stu-id="3e6a3-104">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="3e6a3-105">成員</span><span class="sxs-lookup"><span data-stu-id="3e6a3-105">Members</span></span>

<span data-ttu-id="3e6a3-106">**IAnalysisAlternates** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="3e6a3-106">The **IAnalysisAlternates** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3e6a3-107">**IAnalysisAlternates** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3e6a3-107">**IAnalysisAlternates** also has these types of members:</span></span>

-   [<span data-ttu-id="3e6a3-108">方法</span><span class="sxs-lookup"><span data-stu-id="3e6a3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3e6a3-109">方法</span><span class="sxs-lookup"><span data-stu-id="3e6a3-109">Methods</span></span>

<span data-ttu-id="3e6a3-110">**IAnalysisAlternates** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3e6a3-110">The **IAnalysisAlternates** interface has these methods.</span></span>



| <span data-ttu-id="3e6a3-111">方法</span><span class="sxs-lookup"><span data-stu-id="3e6a3-111">Method</span></span>                                                                   | <span data-ttu-id="3e6a3-112">描述</span><span class="sxs-lookup"><span data-stu-id="3e6a3-112">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e6a3-113">**GetAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-113">**GetAnalysisAlternate**</span></span>](ianalysisalternates-getanalysisalternate.md) | <span data-ttu-id="3e6a3-114">抓取集合中位於指定索引位置的 [**IAnalysisAlternate**](ianalysisalternate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3e6a3-114">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span><br/>                   |
| [<span data-ttu-id="3e6a3-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-115">**GetCount**</span></span>](ianalysisalternates-getcount.md)                         | <span data-ttu-id="3e6a3-116">捕獲 **IAnalysisAlternates** 集合中包含的 [**IAnalysisAlternate**](ianalysisalternate.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="3e6a3-116">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the **IAnalysisAlternates** collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e6a3-117">備註</span><span class="sxs-lookup"><span data-stu-id="3e6a3-117">Remarks</span></span>

<span data-ttu-id="3e6a3-118">這個介面相當於 .NET Framework 中的 [**AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) 類別。</span><span class="sxs-lookup"><span data-stu-id="3e6a3-118">This interface is equivalent to the [**System.Windows.Ink.AnalysisCore.AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e6a3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e6a3-119">Requirements</span></span>



| <span data-ttu-id="3e6a3-120">需求</span><span class="sxs-lookup"><span data-stu-id="3e6a3-120">Requirement</span></span> | <span data-ttu-id="3e6a3-121">值</span><span class="sxs-lookup"><span data-stu-id="3e6a3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e6a3-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e6a3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3e6a3-123">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e6a3-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3e6a3-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e6a3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3e6a3-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="3e6a3-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3e6a3-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3e6a3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e6a3-127"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="3e6a3-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3e6a3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3e6a3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e6a3-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e6a3-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3e6a3-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e6a3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e6a3-131">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-131">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="3e6a3-132">**IInkAnalyzer：： GetAlternates 方法**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-132">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="3e6a3-133">**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-133">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="3e6a3-134">**IInkAnalyzer：： GetAlternatesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="3e6a3-134">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="3e6a3-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="3e6a3-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

