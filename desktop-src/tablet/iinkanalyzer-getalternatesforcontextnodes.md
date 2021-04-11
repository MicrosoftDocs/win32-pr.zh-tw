---
description: 抓取指定 ICoNtextNodes 集合中節點的分析替代項。
ms.assetid: 7d047808-4360-442d-8fd9-4ee4aeeed2c9
title: 'IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71c53e4a8e0989d836d63db5c5cae8c89d56fcf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113344"
---
# <a name="iinkanalyzergetalternatesforcontextnodes-method"></a><span data-ttu-id="d512a-103">IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法</span><span class="sxs-lookup"><span data-stu-id="d512a-103">IInkAnalyzer::GetAlternatesForContextNodes method</span></span>

<span data-ttu-id="d512a-104">抓取指定 [**ICoNtextNodes**](icontextnodes.md) 集合中節點的分析替代項。</span><span class="sxs-lookup"><span data-stu-id="d512a-104">Retrieves analysis alternates for the nodes in a specified [**IContextNodes**](icontextnodes.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d512a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d512a-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForContextNodes(
  [in]  IContextNodes      *pContextNodes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="d512a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d512a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d512a-107">*pCoNtextNodes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d512a-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d512a-108">傳回其分析替代專案的 [**ICoNtextNodes**](icontextnodes.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="d512a-108">The [**IContextNodes**](icontextnodes.md) collection for which the analysis alternatives are returned.</span></span>

</dd> <dt>

<span data-ttu-id="d512a-109">*ulMaximumAlternates* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d512a-109">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d512a-110">要傳回的最大替代專案數目。</span><span class="sxs-lookup"><span data-stu-id="d512a-110">The maximum number of alternatives to return.</span></span>

</dd> <dt>

<span data-ttu-id="d512a-111">*ppAlternates* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d512a-111">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d512a-112">包含分析替代專案的 [**IAnalysisAlternates**](ianalysisalternates.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d512a-112">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d512a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d512a-113">Return value</span></span>

<span data-ttu-id="d512a-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="d512a-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d512a-115">備註</span><span class="sxs-lookup"><span data-stu-id="d512a-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="d512a-116">若要避免記憶體流失，請在 *ppAlternates* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="d512a-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="d512a-117">Top [**IAnalysisAlternate**](ianalysisalternate.md) 會傳回為集合的第一個替代。</span><span class="sxs-lookup"><span data-stu-id="d512a-117">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="d512a-118">*PCoNtextNodes* 中的 [**ICoNtextNode**](icontextnode.md)物件不需要代表檔的相鄰區域。</span><span class="sxs-lookup"><span data-stu-id="d512a-118">The [**IContextNode**](icontextnode.md) objects in *pContextNodes* do not have to represent adjacent areas of the document.</span></span>

<span data-ttu-id="d512a-119">針對節點中的每個分析提示， [**IInkAnalyzer**](iinkanalyzer.md) 只會傳回最上層的替代項。</span><span class="sxs-lookup"><span data-stu-id="d512a-119">For each analysis hint in nodes, the [**IInkAnalyzer**](iinkanalyzer.md) returns only the top alternate.</span></span>

## <a name="requirements"></a><span data-ttu-id="d512a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d512a-120">Requirements</span></span>



| <span data-ttu-id="d512a-121">需求</span><span class="sxs-lookup"><span data-stu-id="d512a-121">Requirement</span></span> | <span data-ttu-id="d512a-122">值</span><span class="sxs-lookup"><span data-stu-id="d512a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d512a-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d512a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d512a-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d512a-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d512a-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d512a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d512a-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="d512a-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d512a-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d512a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d512a-128"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="d512a-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d512a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d512a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d512a-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d512a-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d512a-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d512a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d512a-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="d512a-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="d512a-133">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="d512a-133">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="d512a-134">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="d512a-134">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="d512a-135">**IInkAnalyzer：： GetAlternates 方法**</span><span class="sxs-lookup"><span data-stu-id="d512a-135">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="d512a-136">**IInkAnalyzer：： GetAlternatesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="d512a-136">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="d512a-137">**IInkAnalyzer：： ModifyTopAlternate 方法**</span><span class="sxs-lookup"><span data-stu-id="d512a-137">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="d512a-138">**IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法**</span><span class="sxs-lookup"><span data-stu-id="d512a-138">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="d512a-139">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="d512a-139">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

