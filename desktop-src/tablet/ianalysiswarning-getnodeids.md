---
description: 傳回與這個警告相關聯之任何相關內容節點的識別碼。
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'IAnalysisWarning：： GetNodeIds 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511688"
---
# <a name="ianalysiswarninggetnodeids-method"></a><span data-ttu-id="e32f8-103">IAnalysisWarning：： GetNodeIds 方法</span><span class="sxs-lookup"><span data-stu-id="e32f8-103">IAnalysisWarning::GetNodeIds method</span></span>

<span data-ttu-id="e32f8-104">傳回與這個警告相關聯之任何相關內容節點的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e32f8-104">Returns the identifiers of any relevant context nodes that are associated with this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="e32f8-105">語法</span><span class="sxs-lookup"><span data-stu-id="e32f8-105">Syntax</span></span>


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a><span data-ttu-id="e32f8-106">參數</span><span class="sxs-lookup"><span data-stu-id="e32f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e32f8-107">*pulCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e32f8-107">*pulCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e32f8-108"> (Guid) 在 *ppNodeIds* 中的全域唯一識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="e32f8-108">The number of globally unique identifiers (GUIDs) in *ppNodeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="e32f8-109">*ppNodeIds* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e32f8-109">*ppNodeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e32f8-110">Guid 陣列的指標，可識別與此分析警告相關聯的內容節點，如果沒有任何內容節點與警告相關聯，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="e32f8-110">A pointer to an array of GUIDs that identifies the context nodes that are associated with this analysis warning, or **NULL** if no context nodes are associated with the warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e32f8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e32f8-111">Return value</span></span>

<span data-ttu-id="e32f8-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="e32f8-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e32f8-113">備註</span><span class="sxs-lookup"><span data-stu-id="e32f8-113">Remarks</span></span>

<span data-ttu-id="e32f8-114">如果 *ppNodeIds* 傳遞為 **Null**，則 **GetNodeIds** 方法會傳回 **S \_ OK** ，而且在 *pulCount* 中會傳回矩形的數目。</span><span class="sxs-lookup"><span data-stu-id="e32f8-114">If *ppNodeIds* is passed as **NULL**, the **GetNodeIds** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="e32f8-115">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppNodeIds* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e32f8-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppNodeIds* when you no longer need the information.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e32f8-116">範例</span><span class="sxs-lookup"><span data-stu-id="e32f8-116">Examples</span></span>

<span data-ttu-id="e32f8-117">下列範例顯示如何取得 [**IAnalysisWarning**](ianalysiswarning.md)中的 [**ICoNtextNode**](icontextnode.md)物件，以及 `warning` 如何只取得 **ICoNtextNode** 物件的數目</span><span class="sxs-lookup"><span data-stu-id="e32f8-117">The following example shows how to get the [**IContextNode**](icontextnode.md) objects that are in the [**IAnalysisWarning**](ianalysiswarning.md), `warning`, and how to get only the number of **IContextNode** objects</span></span>


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="e32f8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e32f8-118">Requirements</span></span>



| <span data-ttu-id="e32f8-119">需求</span><span class="sxs-lookup"><span data-stu-id="e32f8-119">Requirement</span></span> | <span data-ttu-id="e32f8-120">值</span><span class="sxs-lookup"><span data-stu-id="e32f8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e32f8-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e32f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e32f8-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e32f8-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e32f8-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e32f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e32f8-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="e32f8-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e32f8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e32f8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e32f8-126"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e32f8-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e32f8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e32f8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e32f8-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e32f8-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e32f8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e32f8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e32f8-130">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="e32f8-130">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="e32f8-131">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="e32f8-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e32f8-132">**IInkAnalyzer：： FindNode 方法**</span><span class="sxs-lookup"><span data-stu-id="e32f8-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="e32f8-133">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="e32f8-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

