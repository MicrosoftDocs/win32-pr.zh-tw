---
description: 抓取所有附加至 IInkAnalyzer 並具有指定名稱的分析提示 ICoNtextNode 物件。
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'IInkAnalyzer：： GetAnalysisHintsByName 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d86b18bfb8cf17097a36e35fc638dd9bd763d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191406"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a><span data-ttu-id="60287-103">IInkAnalyzer：： GetAnalysisHintsByName 方法</span><span class="sxs-lookup"><span data-stu-id="60287-103">IInkAnalyzer::GetAnalysisHintsByName method</span></span>

<span data-ttu-id="60287-104">抓取所有附加至 [**IInkAnalyzer**](iinkanalyzer.md)並具有指定名稱的分析提示 [**ICoNtextNode**](icontextnode.md)物件。</span><span class="sxs-lookup"><span data-stu-id="60287-104">Retrieves all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md) and that have the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="60287-105">語法</span><span class="sxs-lookup"><span data-stu-id="60287-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="60287-106">參數</span><span class="sxs-lookup"><span data-stu-id="60287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60287-107">*hintName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60287-107">*hintName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60287-108">要搜尋的提示名稱。</span><span class="sxs-lookup"><span data-stu-id="60287-108">The hint name for which to search.</span></span>

</dd> <dt>

<span data-ttu-id="60287-109">*ppAnalysisHints* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="60287-109">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60287-110">分析提示會 [**ICoNtextNode**](icontextnode.md) [**IInkAnalyzer**](iinkanalyzer.md) 中具有指定名稱的物件。</span><span class="sxs-lookup"><span data-stu-id="60287-110">The analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) that have the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60287-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="60287-111">Return value</span></span>

<span data-ttu-id="60287-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md) 傳回值。</span><span class="sxs-lookup"><span data-stu-id="60287-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="60287-113">備註</span><span class="sxs-lookup"><span data-stu-id="60287-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="60287-114">若要避免記憶體流失，請在 *ppAnalysisHints* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="60287-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="60287-115">如果沒有將這類分析提示節點附加至 [**IInkAnalyzer**](iinkanalyzer.md)，這個方法會傳回空集合。</span><span class="sxs-lookup"><span data-stu-id="60287-115">This method returns an empty collection if no such analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="60287-116">分析提示節點是 [**ICoNtextNode**](icontextnode.md) ，其內容節點類型為 AnalysisHint (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md) 和 [內容節點類型](context-node-types.md)) 。</span><span class="sxs-lookup"><span data-stu-id="60287-116">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="60287-117">若要將內容資訊加入至提示，請使用 [**ICoNtextNode：： AddPropertyData**](icontextnode-addpropertydata.md) ，並將 *pPropertyDataId* 參數設定為 [分析提示屬性](analysis-hint-properties.md) 常數中 (guid) 的其中一個全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="60287-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="60287-118">若要尋找內容節點上設定的屬性值，請使用 [**ICoNtextNode：： GetPropertyDataIds**](icontextnode-getpropertydataids.md)。</span><span class="sxs-lookup"><span data-stu-id="60287-118">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="60287-119">若要尋找屬性的值，請使用 [**ICoNtextNode：： GetPropertyData**](icontextnode-getpropertydata.md)。</span><span class="sxs-lookup"><span data-stu-id="60287-119">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60287-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="60287-120">Requirements</span></span>



| <span data-ttu-id="60287-121">需求</span><span class="sxs-lookup"><span data-stu-id="60287-121">Requirement</span></span> | <span data-ttu-id="60287-122">值</span><span class="sxs-lookup"><span data-stu-id="60287-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60287-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60287-123">Minimum supported client</span></span><br/> | <span data-ttu-id="60287-124">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60287-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="60287-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60287-125">Minimum supported server</span></span><br/> | <span data-ttu-id="60287-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="60287-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="60287-127">標頭</span><span class="sxs-lookup"><span data-stu-id="60287-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="60287-128"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="60287-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="60287-129">DLL</span><span class="sxs-lookup"><span data-stu-id="60287-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60287-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60287-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="60287-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60287-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60287-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="60287-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="60287-133">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="60287-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="60287-134">**IInkAnalyzer：： CreateAnalysisHint 方法**</span><span class="sxs-lookup"><span data-stu-id="60287-134">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="60287-135">**IInkAnalyzer：:D eleteAnalysisHint 方法**</span><span class="sxs-lookup"><span data-stu-id="60287-135">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="60287-136">**IInkAnalyzer：： GetAnalysisHints 方法**</span><span class="sxs-lookup"><span data-stu-id="60287-136">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="60287-137">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="60287-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

