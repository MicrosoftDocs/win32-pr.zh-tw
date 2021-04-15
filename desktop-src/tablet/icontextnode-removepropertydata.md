---
description: 移除應用程式特定的資料片段。
ms.assetid: 41077c2f-39e3-4069-ac05-97f1785e37b7
title: 'ICoNtextNode：： RemovePropertyData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.RemovePropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4c2fd5924b206ee296c066a908d2a59b02019f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511672"
---
# <a name="icontextnoderemovepropertydata-method"></a><span data-ttu-id="e7497-103">ICoNtextNode：： RemovePropertyData 方法</span><span class="sxs-lookup"><span data-stu-id="e7497-103">IContextNode::RemovePropertyData method</span></span>

<span data-ttu-id="e7497-104">移除應用程式特定的資料片段。</span><span class="sxs-lookup"><span data-stu-id="e7497-104">Removes a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7497-105">語法</span><span class="sxs-lookup"><span data-stu-id="e7497-105">Syntax</span></span>


```C++
HRESULT RemovePropertyData(
  [in] const GUID *pPropertyDataId
);
```



## <a name="parameters"></a><span data-ttu-id="e7497-106">參數</span><span class="sxs-lookup"><span data-stu-id="e7497-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7497-107">*pPropertyDataId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e7497-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7497-108">要移除之資料的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7497-108">The identifier of the data to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7497-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7497-109">Return value</span></span>

<span data-ttu-id="e7497-110">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="e7497-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7497-111">備註</span><span class="sxs-lookup"><span data-stu-id="e7497-111">Remarks</span></span>

<span data-ttu-id="e7497-112">**E \_** 如果 *pPropertyDataId* 參數是其中一個 [內容節點屬性](context-node-properties.md)常數，則會傳回 INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="e7497-112">**E\_INVALIDARG** is returned if the *pPropertyDataId* parameter is one of the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7497-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7497-113">Requirements</span></span>



| <span data-ttu-id="e7497-114">需求</span><span class="sxs-lookup"><span data-stu-id="e7497-114">Requirement</span></span> | <span data-ttu-id="e7497-115">值</span><span class="sxs-lookup"><span data-stu-id="e7497-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7497-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7497-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e7497-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7497-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e7497-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7497-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e7497-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="e7497-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e7497-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e7497-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7497-121"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e7497-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e7497-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e7497-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7497-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7497-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e7497-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7497-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7497-125">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="e7497-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="e7497-126">**ICoNtextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e7497-126">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="e7497-127">**ICoNtextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e7497-127">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="e7497-128">**ICoNtextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="e7497-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="e7497-129">**ICoNtextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="e7497-129">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="e7497-130">**ICoNtextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="e7497-130">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="e7497-131">**ICoNtextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="e7497-131">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="e7497-132">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="e7497-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




