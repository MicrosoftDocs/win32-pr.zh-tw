---
description: 為 IInkAnalyzer 建立新的自訂辨識器節點。
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'IInkAnalyzer：： CreateCustomRecognizer 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191409"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a><span data-ttu-id="ee1ba-103">IInkAnalyzer：： CreateCustomRecognizer 方法</span><span class="sxs-lookup"><span data-stu-id="ee1ba-103">IInkAnalyzer::CreateCustomRecognizer method</span></span>

<span data-ttu-id="ee1ba-104">為 [**IInkAnalyzer**](iinkanalyzer.md)建立新的自訂辨識器節點。</span><span class="sxs-lookup"><span data-stu-id="ee1ba-104">Creates a new custom recognizer node for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee1ba-105">語法</span><span class="sxs-lookup"><span data-stu-id="ee1ba-105">Syntax</span></span>


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="ee1ba-106">參數</span><span class="sxs-lookup"><span data-stu-id="ee1ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee1ba-107">*pInkAnalysisRecognizerId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ee1ba-107">*pInkAnalysisRecognizerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee1ba-108">要建立節點之 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 的全域唯一識別碼 (GUID) 。</span><span class="sxs-lookup"><span data-stu-id="ee1ba-108">The globally unique identifier (GUID) of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) for which to create a node.</span></span>

</dd> <dt>

<span data-ttu-id="ee1ba-109">*ppCoNtextNode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ee1ba-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee1ba-110">[**ICoNtextNode**](icontextnode.md)物件的指標，代表新的自訂辨識器節點。</span><span class="sxs-lookup"><span data-stu-id="ee1ba-110">A pointer to the [**IContextNode**](icontextnode.md) object representing the new custom recognizer node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee1ba-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee1ba-111">Return value</span></span>

<span data-ttu-id="ee1ba-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="ee1ba-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee1ba-113">備註</span><span class="sxs-lookup"><span data-stu-id="ee1ba-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ee1ba-114">若要避免記憶體流失，請在 ppCoNtextNode 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="ee1ba-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on ppContextNode when you no longer need to use the object.</span></span>

 

<span data-ttu-id="ee1ba-115">這個方法會建立具有 CustomRecognizer 類型的新 [**ICoNtextNode**](icontextnode.md) (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ee1ba-115">This method creates a new [**IContextNode**](icontextnode.md) with a type of CustomRecognizer (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="ee1ba-116">然後，它會將新的自訂辨識器節點新增至 [**IInkAnalyzer**](iinkanalyzer.md) 物件根節點的子節點集合 (請參閱 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 和 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)) 。</span><span class="sxs-lookup"><span data-stu-id="ee1ba-116">It then adds the new custom recognizer node to the subnodes collection of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee1ba-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee1ba-117">Requirements</span></span>



| <span data-ttu-id="ee1ba-118">需求</span><span class="sxs-lookup"><span data-stu-id="ee1ba-118">Requirement</span></span> | <span data-ttu-id="ee1ba-119">值</span><span class="sxs-lookup"><span data-stu-id="ee1ba-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1ba-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ee1ba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ee1ba-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ee1ba-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ee1ba-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ee1ba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ee1ba-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="ee1ba-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ee1ba-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ee1ba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee1ba-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="ee1ba-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ee1ba-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ee1ba-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee1ba-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee1ba-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ee1ba-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee1ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1ba-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ee1ba-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ee1ba-130">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="ee1ba-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ee1ba-131">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="ee1ba-131">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="ee1ba-132">**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**</span><span class="sxs-lookup"><span data-stu-id="ee1ba-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="ee1ba-133">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="ee1ba-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

