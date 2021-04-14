---
description: 判斷 ICoNtextNode 物件是否包含儲存在指定之識別碼下的資料。
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'ICoNtextNode：： ContainsPropertyData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469144"
---
# <a name="icontextnodecontainspropertydata-method"></a><span data-ttu-id="1e357-103">ICoNtextNode：： ContainsPropertyData 方法</span><span class="sxs-lookup"><span data-stu-id="1e357-103">IContextNode::ContainsPropertyData method</span></span>

<span data-ttu-id="1e357-104">判斷 [**ICoNtextNode**](icontextnode.md) 物件是否包含儲存在指定之識別碼下的資料。</span><span class="sxs-lookup"><span data-stu-id="1e357-104">Determines whether the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e357-105">語法</span><span class="sxs-lookup"><span data-stu-id="1e357-105">Syntax</span></span>


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a><span data-ttu-id="1e357-106">參數</span><span class="sxs-lookup"><span data-stu-id="1e357-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e357-107">*pPropertyDataId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e357-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e357-108">資料的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e357-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="1e357-109">*pbContains* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1e357-109">*pbContains* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e357-110">**變異 \_** 如果 [**ICoNtextNode**](icontextnode.md)物件包含在指定的識別碼下儲存的資料，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="1e357-110">**VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e357-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e357-111">Return value</span></span>

<span data-ttu-id="1e357-112">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="1e357-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1e357-113">備註</span><span class="sxs-lookup"><span data-stu-id="1e357-113">Remarks</span></span>

<span data-ttu-id="1e357-114">除了應用程式專屬的資料之外，您也可以使用這個方法來判斷這個 [**ICoNtextNode**](icontextnode.md) 是否包含其他內部資料 (請參閱) 的 [ [分析提示屬性](analysis-hint-properties.md) ] 和 [ [內容節點屬性](context-node-properties.md) ]。</span><span class="sxs-lookup"><span data-stu-id="1e357-114">In addition to application-specific data, you can also use this method to determine whether this [**IContextNode**](icontextnode.md) contains other internal data (see [Analysis Hint Properties](analysis-hint-properties.md) and [Context Node Properties](context-node-properties.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e357-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e357-115">Requirements</span></span>



| <span data-ttu-id="1e357-116">需求</span><span class="sxs-lookup"><span data-stu-id="1e357-116">Requirement</span></span> | <span data-ttu-id="1e357-117">值</span><span class="sxs-lookup"><span data-stu-id="1e357-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e357-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e357-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e357-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e357-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1e357-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e357-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e357-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="1e357-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1e357-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1e357-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e357-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="1e357-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1e357-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1e357-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e357-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e357-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1e357-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e357-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e357-127">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="1e357-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1e357-128">**ICoNtextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="1e357-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="1e357-129">**ICoNtextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="1e357-129">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="1e357-130">**ICoNtextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="1e357-130">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="1e357-131">**ICoNtextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="1e357-131">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="1e357-132">**ICoNtextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="1e357-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="1e357-133">**ICoNtextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="1e357-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="1e357-134">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="1e357-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




