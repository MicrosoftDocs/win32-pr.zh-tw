---
description: 抓取 ICoNtextNode 物件內筆劃的識別碼陣列。
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'ICoNtextNode：： GetStrokeIds 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 25592cd245eba135fa7e459ff3c5c5207fc6ff0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113384"
---
# <a name="icontextnodegetstrokeids-method"></a><span data-ttu-id="8cf29-103">ICoNtextNode：： GetStrokeIds 方法</span><span class="sxs-lookup"><span data-stu-id="8cf29-103">IContextNode::GetStrokeIds method</span></span>

<span data-ttu-id="8cf29-104">抓取 [**ICoNtextNode**](icontextnode.md) 物件內筆劃的識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="8cf29-104">Retrieves an array of identifiers for the strokes within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf29-105">語法</span><span class="sxs-lookup"><span data-stu-id="8cf29-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="8cf29-106">參數</span><span class="sxs-lookup"><span data-stu-id="8cf29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf29-107">*pulStrokeIdsCount* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8cf29-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf29-108">筆劃的數目。</span><span class="sxs-lookup"><span data-stu-id="8cf29-108">The number of strokes.</span></span> <span data-ttu-id="8cf29-109">未使用傳入的值。</span><span class="sxs-lookup"><span data-stu-id="8cf29-109">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8cf29-110">*pplStrokes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8cf29-110">*pplStrokes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf29-111">這個 [**ICoNtextNode**](icontextnode.md) 物件之筆觸識別碼陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="8cf29-111">A pointer to the array of stroke identifiers for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf29-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8cf29-112">Return value</span></span>

<span data-ttu-id="8cf29-113">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="8cf29-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8cf29-114">備註</span><span class="sxs-lookup"><span data-stu-id="8cf29-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8cf29-115">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *pplStrokes* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8cf29-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokes* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8cf29-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8cf29-116">Requirements</span></span>



| <span data-ttu-id="8cf29-117">需求</span><span class="sxs-lookup"><span data-stu-id="8cf29-117">Requirement</span></span> | <span data-ttu-id="8cf29-118">值</span><span class="sxs-lookup"><span data-stu-id="8cf29-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf29-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8cf29-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf29-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8cf29-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8cf29-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8cf29-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf29-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="8cf29-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8cf29-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8cf29-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf29-124"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="8cf29-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8cf29-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8cf29-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cf29-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cf29-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8cf29-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8cf29-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf29-128">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="8cf29-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8cf29-129">**ICoNtextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="8cf29-129">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="8cf29-130">**ICoNtextNode::GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="8cf29-130">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="8cf29-131">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="8cf29-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

