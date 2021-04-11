---
description: 新增應用程式特定資料的片段。
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'ICoNtextNode：： AddPropertyData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed318520b8ac83acbc8ed615002fababe2a4b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113392"
---
# <a name="icontextnodeaddpropertydata-method"></a><span data-ttu-id="6a062-103">ICoNtextNode：： AddPropertyData 方法</span><span class="sxs-lookup"><span data-stu-id="6a062-103">IContextNode::AddPropertyData method</span></span>

<span data-ttu-id="6a062-104">新增應用程式特定資料的片段。</span><span class="sxs-lookup"><span data-stu-id="6a062-104">Adds a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a062-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a062-105">Syntax</span></span>


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a><span data-ttu-id="6a062-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a062-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a062-107">*pPropertyDataId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a062-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a062-108"> (GUID) 的全域唯一識別碼，用來識別資料的類型。</span><span class="sxs-lookup"><span data-stu-id="6a062-108">A globally unique identifier (GUID) that is used to identify the type of data.</span></span>

</dd> <dt>

<span data-ttu-id="6a062-109">*ulPropertyDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a062-109">*ulPropertyDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a062-110">資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6a062-110">The size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6a062-111">*pbPropertiesData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a062-111">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a062-112">\[在中，大小 \_ 為 (ulPropertyDataSize) \]</span><span class="sxs-lookup"><span data-stu-id="6a062-112">\[in, size\_is(ulPropertyDataSize)\]</span></span>

<span data-ttu-id="6a062-113">8位不帶正負號的整數陣列，包含要加入的屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="6a062-113">An 8-bit unsigned integer array containing the property information to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a062-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a062-114">Return value</span></span>

<span data-ttu-id="6a062-115">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="6a062-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a062-116">備註</span><span class="sxs-lookup"><span data-stu-id="6a062-116">Remarks</span></span>

<span data-ttu-id="6a062-117">使用 **ICoNtextNode：： AddPropertyData** 來建立資料與內容節點之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="6a062-117">Use **IContextNode::AddPropertyData** to associate data with a context node.</span></span> <span data-ttu-id="6a062-118">若要稍後取出資料，請使用 [**ICoNtextNode：： GetPropertyData**](icontextnode-getpropertydata.md)。</span><span class="sxs-lookup"><span data-stu-id="6a062-118">To retrieve the data later, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

<span data-ttu-id="6a062-119">筆墨分析器可能會刪除節點作為筆墨分析的一部分，除非確認內容節點 (請參閱 [**ICoNtextNode：： Confirm**](icontextnode-confirm.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6a062-119">The ink analyzer may delete the node as part of ink analysis, unless the context node is confirmed (see [**IContextNode::Confirm**](icontextnode-confirm.md)).</span></span> <span data-ttu-id="6a062-120">如需有關同步處理應用程式資料與 [**IInkAnalyzer**](iinkanalyzer.md)的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="6a062-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a062-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a062-121">Requirements</span></span>



| <span data-ttu-id="6a062-122">需求</span><span class="sxs-lookup"><span data-stu-id="6a062-122">Requirement</span></span> | <span data-ttu-id="6a062-123">值</span><span class="sxs-lookup"><span data-stu-id="6a062-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a062-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6a062-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6a062-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6a062-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6a062-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6a062-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6a062-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="6a062-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6a062-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6a062-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a062-129"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="6a062-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6a062-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6a062-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a062-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a062-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6a062-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a062-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a062-133">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="6a062-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6a062-134">**ICoNtextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="6a062-134">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="6a062-135">**ICoNtextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="6a062-135">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="6a062-136">**ICoNtextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="6a062-136">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="6a062-137">**ICoNtextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="6a062-137">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="6a062-138">**ICoNtextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="6a062-138">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="6a062-139">**ICoNtextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="6a062-139">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




