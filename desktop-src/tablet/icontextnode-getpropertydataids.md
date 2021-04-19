---
description: 抓取具有屬性資料的識別碼。
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'ICoNtextNode：： GetPropertyDataIds 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cdbc0ec0a613feccb4064a88f4723538439f4532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970440"
---
# <a name="icontextnodegetpropertydataids-method"></a><span data-ttu-id="40497-103">ICoNtextNode：： GetPropertyDataIds 方法</span><span class="sxs-lookup"><span data-stu-id="40497-103">IContextNode::GetPropertyDataIds method</span></span>

<span data-ttu-id="40497-104">抓取具有屬性資料的識別碼。</span><span class="sxs-lookup"><span data-stu-id="40497-104">Retrieves the identifiers for which there is property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="40497-105">語法</span><span class="sxs-lookup"><span data-stu-id="40497-105">Syntax</span></span>


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a><span data-ttu-id="40497-106">參數</span><span class="sxs-lookup"><span data-stu-id="40497-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40497-107">*pulGuidCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="40497-107">*pulGuidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40497-108">屬性的數目。</span><span class="sxs-lookup"><span data-stu-id="40497-108">The number of properties.</span></span>

</dd> <dt>

<span data-ttu-id="40497-109">*ppGuids* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="40497-109">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40497-110">具有屬性資料的識別碼。</span><span class="sxs-lookup"><span data-stu-id="40497-110">The identifiers for which there is property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40497-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="40497-111">Return value</span></span>

<span data-ttu-id="40497-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="40497-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="40497-113">備註</span><span class="sxs-lookup"><span data-stu-id="40497-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="40497-114">若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppGuids* 的記憶體。</span><span class="sxs-lookup"><span data-stu-id="40497-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="40497-115">這個方法會傳回已加入之屬性資料的應用程式特定識別碼。</span><span class="sxs-lookup"><span data-stu-id="40497-115">This method returns the application-specific identifiers for property data that has been added.</span></span> <span data-ttu-id="40497-116">它也會傳回內部屬性資料的識別碼，此識別碼是由 [內容節點屬性](context-node-properties.md) 常數所描述。</span><span class="sxs-lookup"><span data-stu-id="40497-116">It also returns the identifiers for the internal property data, which are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="40497-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="40497-117">Requirements</span></span>



| <span data-ttu-id="40497-118">需求</span><span class="sxs-lookup"><span data-stu-id="40497-118">Requirement</span></span> | <span data-ttu-id="40497-119">值</span><span class="sxs-lookup"><span data-stu-id="40497-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40497-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40497-120">Minimum supported client</span></span><br/> | <span data-ttu-id="40497-121">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40497-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="40497-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40497-122">Minimum supported server</span></span><br/> | <span data-ttu-id="40497-123">都不支援</span><span class="sxs-lookup"><span data-stu-id="40497-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="40497-124">標頭</span><span class="sxs-lookup"><span data-stu-id="40497-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="40497-125"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="40497-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="40497-126">DLL</span><span class="sxs-lookup"><span data-stu-id="40497-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40497-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40497-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="40497-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40497-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40497-129">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="40497-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="40497-130">**ICoNtextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="40497-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="40497-131">**ICoNtextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="40497-131">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="40497-132">**ICoNtextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="40497-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="40497-133">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="40497-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

