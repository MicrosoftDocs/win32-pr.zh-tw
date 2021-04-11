---
description: 取得指定之全域唯一識別碼 (GUID) 的 ICoNtextNode 物件。
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: 'IInkAnalyzer：： FindNode 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 66771678253f1724653d87ad9c54d474a9ceceb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026249"
---
# <a name="iinkanalyzerfindnode-method"></a><span data-ttu-id="5c098-103">IInkAnalyzer：： FindNode 方法</span><span class="sxs-lookup"><span data-stu-id="5c098-103">IInkAnalyzer::FindNode method</span></span>

<span data-ttu-id="5c098-104">取得指定之全域唯一識別碼 (GUID) 的 [**ICoNtextNode**](icontextnode.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="5c098-104">Retrieves the [**IContextNode**](icontextnode.md) object for a specified globally unique identifier (GUID).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c098-105">語法</span><span class="sxs-lookup"><span data-stu-id="5c098-105">Syntax</span></span>


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a><span data-ttu-id="5c098-106">參數</span><span class="sxs-lookup"><span data-stu-id="5c098-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c098-107">*pId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5c098-107">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c098-108">[**ICoNtextNode**](icontextnode.md)物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c098-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5c098-109">*ppCoNtextNodeFound* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5c098-109">*ppContextNodeFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c098-110">具有 *pId* 識別碼之 [**ICoNtextNode**](icontextnode.md)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="5c098-110">A pointer to the [**IContextNode**](icontextnode.md) object with the *pId* identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c098-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c098-111">Return value</span></span>

<span data-ttu-id="5c098-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="5c098-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c098-113">備註</span><span class="sxs-lookup"><span data-stu-id="5c098-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="5c098-114">若要避免記憶體流失，請在 *ppCoNtextNodeFound* 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。</span><span class="sxs-lookup"><span data-stu-id="5c098-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="5c098-115">如果沒有這類 [**ICoNtextNode**](icontextnode.md) 物件做為 [**IInkAnalyzer**](iinkanalyzer.md) 根節點的子系，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="5c098-115">If no such [**IContextNode**](icontextnode.md) object exists as a descendant of the [**IInkAnalyzer**](iinkanalyzer.md) root node, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c098-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c098-116">Requirements</span></span>



| <span data-ttu-id="5c098-117">需求</span><span class="sxs-lookup"><span data-stu-id="5c098-117">Requirement</span></span> | <span data-ttu-id="5c098-118">值</span><span class="sxs-lookup"><span data-stu-id="5c098-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c098-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c098-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c098-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c098-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5c098-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c098-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c098-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="5c098-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5c098-123">標頭</span><span class="sxs-lookup"><span data-stu-id="5c098-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c098-124"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="5c098-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5c098-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5c098-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c098-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c098-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5c098-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c098-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c098-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="5c098-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5c098-129">**IInkAnalyzer：： FindInkLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="5c098-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="5c098-130">**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="5c098-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="5c098-131">**IInkAnalyzer：： FindLeafNodes 方法**</span><span class="sxs-lookup"><span data-stu-id="5c098-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="5c098-132">**IInkAnalyzer：： FindNodesOfType 方法**</span><span class="sxs-lookup"><span data-stu-id="5c098-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="5c098-133">**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**</span><span class="sxs-lookup"><span data-stu-id="5c098-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="5c098-134">**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="5c098-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="5c098-135">**IInkAnalyzer：： FindNodesWithCallBack 方法**</span><span class="sxs-lookup"><span data-stu-id="5c098-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="5c098-136">**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**</span><span class="sxs-lookup"><span data-stu-id="5c098-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="5c098-137">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="5c098-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

