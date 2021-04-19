---
description: 抓取造成此警告的分析提示。
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'IAnalysisWarning：： GetHint 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c38a22b799eb6836a85a42748f60207ee7e997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966726"
---
# <a name="ianalysiswarninggethint-method"></a><span data-ttu-id="01666-103">IAnalysisWarning：： GetHint 方法</span><span class="sxs-lookup"><span data-stu-id="01666-103">IAnalysisWarning::GetHint method</span></span>

<span data-ttu-id="01666-104">抓取造成此警告的分析提示。</span><span class="sxs-lookup"><span data-stu-id="01666-104">Retrieves the analysis hint that caused this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="01666-105">語法</span><span class="sxs-lookup"><span data-stu-id="01666-105">Syntax</span></span>


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="01666-106">參數</span><span class="sxs-lookup"><span data-stu-id="01666-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01666-107">*pAnalysisHint* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="01666-107">*pAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01666-108">造成此警告的分析提示內容節點，如果分析提示未造成此警告，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="01666-108">The analysis hint context node that caused this warning, or **NULL** if an analysis hint did not cause this warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01666-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="01666-109">Return value</span></span>

<span data-ttu-id="01666-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="01666-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="01666-111">備註</span><span class="sxs-lookup"><span data-stu-id="01666-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="01666-112">若要避免記憶體流失， [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) \* 當您不再需要流量分析提示內容節點時，請在 *pAnalysisHint* 上呼叫 IUnknown：： Release。</span><span class="sxs-lookup"><span data-stu-id="01666-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAnalysisHint* when you no longer need to use the analysis hint context node.</span></span>

 

<span data-ttu-id="01666-113">產生 [**IAnalysisWarning**](ianalysiswarning.md) 的分析提示範例是包含拼寫不正確之模擬的分析提示。</span><span class="sxs-lookup"><span data-stu-id="01666-113">An example of an analysis hint that generates an [**IAnalysisWarning**](ianalysiswarning.md) is an analysis hint that contains an incorrectly spelled factoid.</span></span> <span data-ttu-id="01666-114">在此情況下，「筆跡分析」會傳回 [**IAnalysisStatus**](ianalysisstatus.md) ，其中包含的 **IAnalysisWarning** 會以拼錯的模擬項參考分析提示內容節點。</span><span class="sxs-lookup"><span data-stu-id="01666-114">In this case, ink analysis returns an [**IAnalysisStatus**](ianalysisstatus.md) that contains an **IAnalysisWarning** that references the analysis hint context node with the misspelled factoid.</span></span> <span data-ttu-id="01666-115">此外，在此情況下，分析警告的 [**IAnalysisWarning：： GetWarningCode**](ianalysiswarning-getwarningcode.md)方法會傳回 **AnalysisWarningCode \_ FactoidNotSupported** 的 [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode)值。</span><span class="sxs-lookup"><span data-stu-id="01666-115">Also, in this case, the analysis warning's [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md) method returns an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_FactoidNotSupported**.</span></span>

## <a name="requirements"></a><span data-ttu-id="01666-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="01666-116">Requirements</span></span>



| <span data-ttu-id="01666-117">需求</span><span class="sxs-lookup"><span data-stu-id="01666-117">Requirement</span></span> | <span data-ttu-id="01666-118">值</span><span class="sxs-lookup"><span data-stu-id="01666-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01666-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01666-119">Minimum supported client</span></span><br/> | <span data-ttu-id="01666-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01666-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="01666-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01666-121">Minimum supported server</span></span><br/> | <span data-ttu-id="01666-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="01666-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="01666-123">標頭</span><span class="sxs-lookup"><span data-stu-id="01666-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="01666-124"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="01666-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="01666-125">DLL</span><span class="sxs-lookup"><span data-stu-id="01666-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01666-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01666-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="01666-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="01666-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01666-128">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="01666-128">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="01666-129">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="01666-129">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="01666-130">**IInkAnalyzer：：分析方法**</span><span class="sxs-lookup"><span data-stu-id="01666-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="01666-131">**IInkAnalyzer：： BackgroundAnalyze 方法**</span><span class="sxs-lookup"><span data-stu-id="01666-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="01666-132">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="01666-132">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="01666-133">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="01666-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

