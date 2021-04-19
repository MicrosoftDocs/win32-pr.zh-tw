---
description: 針對所有與 IInkAnalyzer 相關聯的筆墨抓取10個分析替代項。
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: 'IInkAnalyzer：： GetAlternates 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 37219226e651e286a6d1d63accbd7e548b3b7807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973653"
---
# <a name="iinkanalyzergetalternates-method"></a><span data-ttu-id="e3908-103">IInkAnalyzer：： GetAlternates 方法</span><span class="sxs-lookup"><span data-stu-id="e3908-103">IInkAnalyzer::GetAlternates method</span></span>

<span data-ttu-id="e3908-104">針對所有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的筆墨抓取10個分析替代項。</span><span class="sxs-lookup"><span data-stu-id="e3908-104">Retrieves 10 analysis alternates for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3908-105">語法</span><span class="sxs-lookup"><span data-stu-id="e3908-105">Syntax</span></span>


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="e3908-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3908-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3908-107">*ppAlternates* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e3908-107">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3908-108">與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯之所有筆墨的前10個 [**IAnalysisAlternate**](ianalysisalternate.md)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e3908-108">A pointer to the top 10 [**IAnalysisAlternate**](ianalysisalternate.md) objects for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3908-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3908-109">Return value</span></span>

<span data-ttu-id="e3908-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="e3908-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3908-111">備註</span><span class="sxs-lookup"><span data-stu-id="e3908-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="e3908-112">若要避免記憶體流失，請在 *ppAlternates* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="e3908-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="e3908-113">Top 替代會傳回為集合的第一個替代。</span><span class="sxs-lookup"><span data-stu-id="e3908-113">The top alternate is returned as the first alternate of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3908-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3908-114">Requirements</span></span>



| <span data-ttu-id="e3908-115">需求</span><span class="sxs-lookup"><span data-stu-id="e3908-115">Requirement</span></span> | <span data-ttu-id="e3908-116">值</span><span class="sxs-lookup"><span data-stu-id="e3908-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3908-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3908-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3908-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3908-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e3908-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3908-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3908-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="e3908-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e3908-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e3908-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3908-122"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e3908-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e3908-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e3908-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3908-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3908-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e3908-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3908-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3908-126">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e3908-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e3908-127">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="e3908-127">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="e3908-128">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="e3908-128">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="e3908-129">**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="e3908-129">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="e3908-130">**IInkAnalyzer：： GetAlternatesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="e3908-130">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="e3908-131">**IInkAnalyzer：： ModifyTopAlternate 方法**</span><span class="sxs-lookup"><span data-stu-id="e3908-131">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="e3908-132">**IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法**</span><span class="sxs-lookup"><span data-stu-id="e3908-132">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="e3908-133">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="e3908-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

