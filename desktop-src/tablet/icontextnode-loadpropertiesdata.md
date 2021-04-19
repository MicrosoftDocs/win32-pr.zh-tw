---
description: 針對先前使用 ICoNtextNode：： SavePropertiesData 建立的位元組陣列，重新建立應用程式特定和內部屬性資料。
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'ICoNtextNode：： LoadPropertiesData 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc495aaa52ebfbca088f954b34f22f9d6e1e53d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971229"
---
# <a name="icontextnodeloadpropertiesdata-method"></a><span data-ttu-id="f0db0-103">ICoNtextNode：： LoadPropertiesData 方法</span><span class="sxs-lookup"><span data-stu-id="f0db0-103">IContextNode::LoadPropertiesData method</span></span>

<span data-ttu-id="f0db0-104">針對先前使用 [**ICoNtextNode：： SavePropertiesData**](icontextnode-savepropertiesdata.md)建立的位元組陣列，重新建立應用程式特定和內部屬性資料。</span><span class="sxs-lookup"><span data-stu-id="f0db0-104">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0db0-105">語法</span><span class="sxs-lookup"><span data-stu-id="f0db0-105">Syntax</span></span>


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="f0db0-106">參數</span><span class="sxs-lookup"><span data-stu-id="f0db0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0db0-107">*cbPropertiesDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0db0-107">*cbPropertiesDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0db0-108">屬性資料陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="f0db0-108">The size of the properties data array.</span></span>

</dd> <dt>

<span data-ttu-id="f0db0-109">*pbPropertiesData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0db0-109">*pbPropertiesData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0db0-110">8位不帶正負號的整數陣列，包含要載入的屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="f0db0-110">The 8-bit unsigned integer array containing property information to load.</span></span>

</dd> <dt>

<span data-ttu-id="f0db0-111">*pfSuccessful* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f0db0-111">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0db0-112">**變異 \_** 如果成功載入屬性資料，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f0db0-112">**VARIANT\_TRUE** if the property data loaded successfully; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0db0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0db0-113">Return value</span></span>

<span data-ttu-id="f0db0-114">如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="f0db0-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0db0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0db0-115">Requirements</span></span>



| <span data-ttu-id="f0db0-116">需求</span><span class="sxs-lookup"><span data-stu-id="f0db0-116">Requirement</span></span> | <span data-ttu-id="f0db0-117">值</span><span class="sxs-lookup"><span data-stu-id="f0db0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0db0-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0db0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f0db0-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0db0-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f0db0-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0db0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f0db0-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="f0db0-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f0db0-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f0db0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0db0-123"><dt>IACom (也需要 IACom \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="f0db0-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f0db0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f0db0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0db0-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0db0-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f0db0-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0db0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0db0-127">**ICoNtextNode**</span><span class="sxs-lookup"><span data-stu-id="f0db0-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f0db0-128">**ICoNtextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f0db0-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="f0db0-129">**ICoNtextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f0db0-129">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="f0db0-130">**ICoNtextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="f0db0-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="f0db0-131">**ICoNtextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="f0db0-131">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="f0db0-132">**ICoNtextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="f0db0-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="f0db0-133">**ICoNtextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="f0db0-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="f0db0-134">筆跡分析參考</span><span class="sxs-lookup"><span data-stu-id="f0db0-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




