---
description: 取得附加至 IInkAnalyzer 的所有分析提示 ICoNtextNode 物件。
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'IInkAnalyzer：： GetAnalysisHints 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c5ce66eeb6362ed74f1df1a38f220603d3a30117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113340"
---
# <a name="iinkanalyzergetanalysishints-method"></a><span data-ttu-id="82c99-103">IInkAnalyzer：： GetAnalysisHints 方法</span><span class="sxs-lookup"><span data-stu-id="82c99-103">IInkAnalyzer::GetAnalysisHints method</span></span>

<span data-ttu-id="82c99-104">取得附加至 [**IInkAnalyzer**](iinkanalyzer.md)的所有分析提示 [**ICoNtextNode**](icontextnode.md)物件。</span><span class="sxs-lookup"><span data-stu-id="82c99-104">Gets all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="82c99-105">語法</span><span class="sxs-lookup"><span data-stu-id="82c99-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="82c99-106">參數</span><span class="sxs-lookup"><span data-stu-id="82c99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82c99-107">*ppAnalysisHints* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82c99-107">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82c99-108">[**IInkAnalyzer**](iinkanalyzer.md)中所有分析提示 [**ICoNtextNode**](icontextnode.md)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="82c99-108">A pointer to all the analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82c99-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="82c99-109">Return value</span></span>

<span data-ttu-id="82c99-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="82c99-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="82c99-111">備註</span><span class="sxs-lookup"><span data-stu-id="82c99-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="82c99-112">若要避免記憶體流失，請在 *ppAnalysisHints* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="82c99-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="82c99-113">如果沒有任何分析提示節點附加至 [**IInkAnalyzer**](iinkanalyzer.md)，這個方法會傳回空集合。</span><span class="sxs-lookup"><span data-stu-id="82c99-113">This method returns an empty collection if no analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="82c99-114">分析提示節點是 [**ICoNtextNode**](icontextnode.md) ，其內容節點類型為 AnalysisHint (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [內容節點類型](context-node-types.md)) 。</span><span class="sxs-lookup"><span data-stu-id="82c99-114">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="82c99-115">若要將內容資訊加入至提示，請使用 [**ICoNtextNode：： AddPropertyData**](icontextnode-addpropertydata.md) ，並將 *pPropertyDataId* 參數設定為 [分析提示屬性](analysis-hint-properties.md) 常數中 (guid) 的其中一個全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="82c99-115">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="82c99-116">若要尋找內容節點上設定的屬性值，請使用 [**ICoNtextNode：： GetPropertyDataIds**](icontextnode-getpropertydataids.md)。</span><span class="sxs-lookup"><span data-stu-id="82c99-116">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="82c99-117">若要尋找屬性的值，請使用 [**ICoNtextNode：： GetPropertyData**](icontextnode-getpropertydata.md)。</span><span class="sxs-lookup"><span data-stu-id="82c99-117">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82c99-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="82c99-118">Requirements</span></span>



| <span data-ttu-id="82c99-119">需求</span><span class="sxs-lookup"><span data-stu-id="82c99-119">Requirement</span></span> | <span data-ttu-id="82c99-120">值</span><span class="sxs-lookup"><span data-stu-id="82c99-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82c99-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82c99-121">Minimum supported client</span></span><br/> | <span data-ttu-id="82c99-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82c99-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="82c99-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82c99-123">Minimum supported server</span></span><br/> | <span data-ttu-id="82c99-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="82c99-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="82c99-125">標頭</span><span class="sxs-lookup"><span data-stu-id="82c99-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="82c99-126"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="82c99-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="82c99-127">DLL</span><span class="sxs-lookup"><span data-stu-id="82c99-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82c99-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82c99-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="82c99-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82c99-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82c99-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="82c99-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="82c99-131">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="82c99-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="82c99-132">**IInkAnalyzer：： CreateAnalysisHint 方法**</span><span class="sxs-lookup"><span data-stu-id="82c99-132">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="82c99-133">**IInkAnalyzer：:D eleteAnalysisHint 方法**</span><span class="sxs-lookup"><span data-stu-id="82c99-133">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="82c99-134">**IInkAnalyzer：： GetAnalysisHintsByName 方法**</span><span class="sxs-lookup"><span data-stu-id="82c99-134">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="82c99-135">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="82c99-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

