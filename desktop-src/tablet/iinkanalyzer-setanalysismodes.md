---
description: 修改旗標，以控制 IInkAnalyzer 執行筆墨分析的方式。
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: 'IInkAnalyzer：： SetAnalysisModes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 826d31fd5b61db2332ef953d55b2cf6c6331995b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511645"
---
# <a name="iinkanalyzersetanalysismodes-method"></a><span data-ttu-id="7a094-103">IInkAnalyzer：： SetAnalysisModes 方法</span><span class="sxs-lookup"><span data-stu-id="7a094-103">IInkAnalyzer::SetAnalysisModes method</span></span>

<span data-ttu-id="7a094-104">修改旗標，以控制 [**IInkAnalyzer**](iinkanalyzer.md) 執行筆墨分析的方式。</span><span class="sxs-lookup"><span data-stu-id="7a094-104">Modifies flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a094-105">語法</span><span class="sxs-lookup"><span data-stu-id="7a094-105">Syntax</span></span>


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="7a094-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a094-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a094-107">*analysisMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a094-107">*analysisMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a094-108">[**AnalysisModes**](analysismodes.md)列舉值的位元組合。</span><span class="sxs-lookup"><span data-stu-id="7a094-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a094-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a094-109">Return value</span></span>

<span data-ttu-id="7a094-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="7a094-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a094-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a094-111">Requirements</span></span>



| <span data-ttu-id="7a094-112">需求</span><span class="sxs-lookup"><span data-stu-id="7a094-112">Requirement</span></span> | <span data-ttu-id="7a094-113">值</span><span class="sxs-lookup"><span data-stu-id="7a094-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a094-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a094-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7a094-115">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a094-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7a094-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a094-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7a094-117">都不支援</span><span class="sxs-lookup"><span data-stu-id="7a094-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7a094-118">標頭</span><span class="sxs-lookup"><span data-stu-id="7a094-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a094-119"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="7a094-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7a094-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7a094-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a094-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a094-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7a094-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a094-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a094-123">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="7a094-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7a094-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="7a094-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="7a094-125">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="7a094-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="7a094-126">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="7a094-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="7a094-127">**IInkAnalyzer：： GetAnalysisModes 方法**</span><span class="sxs-lookup"><span data-stu-id="7a094-127">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="7a094-128">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="7a094-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




