---
description: GetCount 方法會抓取此集合中的專案數。
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'IPortableDevicePropVariantCollection：： GetCount 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990547"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a><span data-ttu-id="f96a3-103">IPortableDevicePropVariantCollection：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="f96a3-103">IPortableDevicePropVariantCollection::GetCount method</span></span>

<span data-ttu-id="f96a3-104">**GetCount** 方法會抓取此集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="f96a3-104">The **GetCount** method retrieves the number of items in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f96a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="f96a3-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="f96a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="f96a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f96a3-107">*pcElems* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f96a3-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f96a3-108">**DWORD** 的指標，其中包含集合中的專案數。</span><span class="sxs-lookup"><span data-stu-id="f96a3-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f96a3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f96a3-109">Return value</span></span>

<span data-ttu-id="f96a3-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f96a3-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f96a3-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f96a3-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f96a3-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f96a3-112">Return code</span></span>                                                                               | <span data-ttu-id="f96a3-113">Description</span><span class="sxs-lookup"><span data-stu-id="f96a3-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="f96a3-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f96a3-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="f96a3-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f96a3-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="f96a3-116"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="f96a3-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="f96a3-117">必要的指標引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f96a3-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="f96a3-118">範例</span><span class="sxs-lookup"><span data-stu-id="f96a3-118">Examples</span></span>

<span data-ttu-id="f96a3-119">如需如何使用此方法的範例，請參閱抓取 [裝置所支援的功能分類](retrieving-the-functional-categories-supported-by-a-device.md)。</span><span class="sxs-lookup"><span data-stu-id="f96a3-119">For an example of how to use this method see [Retrieving the Functional Categories Supported by a Device](retrieving-the-functional-categories-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f96a3-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f96a3-120">Requirements</span></span>



| <span data-ttu-id="f96a3-121">需求</span><span class="sxs-lookup"><span data-stu-id="f96a3-121">Requirement</span></span> | <span data-ttu-id="f96a3-122">值</span><span class="sxs-lookup"><span data-stu-id="f96a3-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f96a3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f96a3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f96a3-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="f96a3-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f96a3-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="f96a3-125">Library</span></span><br/> | <dl> <span data-ttu-id="f96a3-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f96a3-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f96a3-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f96a3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96a3-128">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="f96a3-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="f96a3-129">正在抓取支援的服務事件</span><span class="sxs-lookup"><span data-stu-id="f96a3-129">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="f96a3-130">正在抓取支援的服務格式</span><span class="sxs-lookup"><span data-stu-id="f96a3-130">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="f96a3-131">正在抓取支援的服務方法</span><span class="sxs-lookup"><span data-stu-id="f96a3-131">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="f96a3-132">正在抓取裝置支援的功能分類</span><span class="sxs-lookup"><span data-stu-id="f96a3-132">Retrieving the Functional Categories Supported by a Device</span></span>](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="f96a3-133">設定多個物件的屬性</span><span class="sxs-lookup"><span data-stu-id="f96a3-133">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




