---
description: IPortableDevicePropVariantCollection：： GetAt 方法-GetAt 方法會依據以零為基底的索引，從集合中抓取專案。
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'IPortableDevicePropVariantCollection：： GetAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b901e8fcfa065813e4c0942632f80901800ef0a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106796"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a><span data-ttu-id="1660f-103">IPortableDevicePropVariantCollection：： GetAt 方法</span><span class="sxs-lookup"><span data-stu-id="1660f-103">IPortableDevicePropVariantCollection::GetAt method</span></span>

<span data-ttu-id="1660f-104">**GetAt** 方法會依據以零為基底的索引，從集合中抓取專案。</span><span class="sxs-lookup"><span data-stu-id="1660f-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1660f-105">語法</span><span class="sxs-lookup"><span data-stu-id="1660f-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="1660f-106">參數</span><span class="sxs-lookup"><span data-stu-id="1660f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1660f-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1660f-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1660f-108">**DWORD** ，其中包含要抓取之專案的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="1660f-108">**DWORD** that contains the zero-based index of the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="1660f-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1660f-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1660f-110">**PROPVARIANT** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="1660f-110">Pointer to a **PROPVARIANT** structure.</span></span> <span data-ttu-id="1660f-111">呼叫端會負責呼叫 **PropVariantClear** 來釋出這個記憶體。</span><span class="sxs-lookup"><span data-stu-id="1660f-111">The caller is responsible for freeing this memory by calling **PropVariantClear**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1660f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1660f-112">Return value</span></span>

<span data-ttu-id="1660f-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="1660f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1660f-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="1660f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1660f-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1660f-115">Return code</span></span>                                                                                  | <span data-ttu-id="1660f-116">Description</span><span class="sxs-lookup"><span data-stu-id="1660f-116">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="1660f-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1660f-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1660f-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="1660f-118">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="1660f-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="1660f-119"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="1660f-120">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1660f-120">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="1660f-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1660f-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1660f-122">傳入的索引超出範圍。</span><span class="sxs-lookup"><span data-stu-id="1660f-122">The index that was passed in was out of range.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="1660f-123">範例</span><span class="sxs-lookup"><span data-stu-id="1660f-123">Examples</span></span>

<span data-ttu-id="1660f-124">如需如何使用此方法的範例，請參閱抓取 [裝置所支援的功能分類](retrieving-the-functional-categories-supported-by-a-device.md)。</span><span class="sxs-lookup"><span data-stu-id="1660f-124">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1660f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1660f-125">Requirements</span></span>



| <span data-ttu-id="1660f-126">需求</span><span class="sxs-lookup"><span data-stu-id="1660f-126">Requirement</span></span> | <span data-ttu-id="1660f-127">值</span><span class="sxs-lookup"><span data-stu-id="1660f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1660f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1660f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1660f-129"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="1660f-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1660f-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="1660f-130">Library</span></span><br/> | <dl> <span data-ttu-id="1660f-131"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1660f-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1660f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1660f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1660f-133">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="1660f-133">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="1660f-134">從持續性唯一識別碼中取出物件識別碼</span><span class="sxs-lookup"><span data-stu-id="1660f-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[<span data-ttu-id="1660f-135">正在抓取支援的服務事件</span><span class="sxs-lookup"><span data-stu-id="1660f-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="1660f-136">正在抓取支援的服務格式</span><span class="sxs-lookup"><span data-stu-id="1660f-136">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="1660f-137">正在抓取支援的服務方法</span><span class="sxs-lookup"><span data-stu-id="1660f-137">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="1660f-138">正在抓取裝置支援的內容類型</span><span class="sxs-lookup"><span data-stu-id="1660f-138">Retrieving the Content Types Supported by a Device</span></span>](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="1660f-139">正在抓取裝置支援的功能分類</span><span class="sxs-lookup"><span data-stu-id="1660f-139">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="1660f-140">正在抓取裝置的功能物件識別碼</span><span class="sxs-lookup"><span data-stu-id="1660f-140">Retrieving the Functional Object Identifiers for a Device</span></span>](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[<span data-ttu-id="1660f-141">正在抓取裝置所支援的轉譯功能</span><span class="sxs-lookup"><span data-stu-id="1660f-141">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="1660f-142">設定多個物件的屬性</span><span class="sxs-lookup"><span data-stu-id="1660f-142">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




