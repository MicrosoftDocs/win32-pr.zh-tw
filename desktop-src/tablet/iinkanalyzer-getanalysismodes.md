---
description: 抓取旗標，以控制 IInkAnalyzer 執行筆墨分析的方式。
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: 'IInkAnalyzer：： GetAnalysisModes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d03ec255b10dd607889768795b00f5b2aff4dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971411"
---
# <a name="iinkanalyzergetanalysismodes-method"></a><span data-ttu-id="4bc8a-103">IInkAnalyzer：： GetAnalysisModes 方法</span><span class="sxs-lookup"><span data-stu-id="4bc8a-103">IInkAnalyzer::GetAnalysisModes method</span></span>

<span data-ttu-id="4bc8a-104">抓取旗標，以控制 [**IInkAnalyzer**](iinkanalyzer.md) 執行筆墨分析的方式。</span><span class="sxs-lookup"><span data-stu-id="4bc8a-104">Retrieves flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc8a-105">語法</span><span class="sxs-lookup"><span data-stu-id="4bc8a-105">Syntax</span></span>


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="4bc8a-106">參數</span><span class="sxs-lookup"><span data-stu-id="4bc8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bc8a-107">*pAnalysisMode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4bc8a-107">*pAnalysisMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bc8a-108">[**AnalysisModes**](analysismodes.md)列舉值的位元組合。</span><span class="sxs-lookup"><span data-stu-id="4bc8a-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bc8a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bc8a-109">Return value</span></span>

<span data-ttu-id="4bc8a-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="4bc8a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bc8a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bc8a-111">Requirements</span></span>



| <span data-ttu-id="4bc8a-112">需求</span><span class="sxs-lookup"><span data-stu-id="4bc8a-112">Requirement</span></span> | <span data-ttu-id="4bc8a-113">值</span><span class="sxs-lookup"><span data-stu-id="4bc8a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bc8a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bc8a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4bc8a-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bc8a-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4bc8a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bc8a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4bc8a-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="4bc8a-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4bc8a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="4bc8a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bc8a-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="4bc8a-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4bc8a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4bc8a-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bc8a-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bc8a-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4bc8a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bc8a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc8a-123">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4bc8a-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4bc8a-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="4bc8a-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="4bc8a-125">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="4bc8a-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="4bc8a-126">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="4bc8a-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="4bc8a-127">**IInkAnalyzer：： SetAnalysisModes 方法**</span><span class="sxs-lookup"><span data-stu-id="4bc8a-127">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="4bc8a-128">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="4bc8a-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




