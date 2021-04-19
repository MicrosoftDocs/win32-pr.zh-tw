---
description: ChangeType 方法會將集合中的所有專案轉換為指定的 VARTYPE。
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'IPortableDevicePropVariantCollection：： ChangeType 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d843b62d273b28f7a694c37358742e4f3365be21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994769"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a><span data-ttu-id="5b625-103">IPortableDevicePropVariantCollection：： ChangeType 方法</span><span class="sxs-lookup"><span data-stu-id="5b625-103">IPortableDevicePropVariantCollection::ChangeType method</span></span>

<span data-ttu-id="5b625-104">**ChangeType** 方法會將集合中的所有專案轉換為指定的 VARTYPE。</span><span class="sxs-lookup"><span data-stu-id="5b625-104">The **ChangeType** method converts all items in the collection to the specified VARTYPE.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b625-105">語法</span><span class="sxs-lookup"><span data-stu-id="5b625-105">Syntax</span></span>


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a><span data-ttu-id="5b625-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b625-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b625-107">*vt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b625-107">*vt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b625-108">指定要將集合中的所有專案轉換成的 **VARTYPE** 。</span><span class="sxs-lookup"><span data-stu-id="5b625-108">Specifies the **VARTYPE** to which you want to convert all items in the collection.</span></span> <span data-ttu-id="5b625-109">範例類型包括 VT \_ UI4 和 vt \_ UI8。</span><span class="sxs-lookup"><span data-stu-id="5b625-109">Example types include VT\_UI4 and VT\_UI8.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b625-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b625-110">Return value</span></span>

<span data-ttu-id="5b625-111">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="5b625-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5b625-112">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="5b625-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5b625-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5b625-113">Return code</span></span>                                                                          | <span data-ttu-id="5b625-114">Description</span><span class="sxs-lookup"><span data-stu-id="5b625-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5b625-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5b625-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5b625-116">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="5b625-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5b625-117">備註</span><span class="sxs-lookup"><span data-stu-id="5b625-117">Remarks</span></span>

<span data-ttu-id="5b625-118">如果此方法失敗，則集合可能會保持為中繼狀態，而某些成員會進行轉換，而且不會轉換。</span><span class="sxs-lookup"><span data-stu-id="5b625-118">If this method fails, the collection may be left in an intermediate state, with some members converted and some not converted.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b625-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b625-119">Requirements</span></span>



| <span data-ttu-id="5b625-120">需求</span><span class="sxs-lookup"><span data-stu-id="5b625-120">Requirement</span></span> | <span data-ttu-id="5b625-121">值</span><span class="sxs-lookup"><span data-stu-id="5b625-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b625-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5b625-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5b625-123"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="5b625-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b625-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="5b625-124">Library</span></span><br/> | <dl> <span data-ttu-id="5b625-125"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b625-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b625-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b625-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b625-127">**IPortableDevicePropVariantCollection 介面**</span><span class="sxs-lookup"><span data-stu-id="5b625-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




