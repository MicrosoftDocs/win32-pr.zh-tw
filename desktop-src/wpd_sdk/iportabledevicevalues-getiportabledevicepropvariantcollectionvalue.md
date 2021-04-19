---
description: GetIPortableDevicePropVariantCollectionValue 方法會抓取索引鍵所指定的 IPortableDevicePropVariantCollection 值， (類型 \_ 為 VT 未知) 。
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'IPortableDeviceValues：： GetIPortableDevicePropVariantCollectionValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7deb73d10f2e2daa5d06d6cb4394c43778af2ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996279"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="a1af7-103">IPortableDeviceValues：： GetIPortableDevicePropVariantCollectionValue 方法</span><span class="sxs-lookup"><span data-stu-id="a1af7-103">IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="a1af7-104">**GetIPortableDevicePropVariantCollectionValue** 方法會抓取索引鍵所指定的 **IPortableDevicePropVariantCollection** 值， (類型 \_ 為 VT 未知) 。</span><span class="sxs-lookup"><span data-stu-id="a1af7-104">The **GetIPortableDevicePropVariantCollectionValue** method retrieves an **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1af7-105">語法</span><span class="sxs-lookup"><span data-stu-id="a1af7-105">Syntax</span></span>


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="a1af7-106">參數</span><span class="sxs-lookup"><span data-stu-id="a1af7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1af7-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a1af7-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1af7-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a1af7-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a1af7-109">*ppValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a1af7-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1af7-110">接收已抓取 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="a1af7-110">Address of a variable that receives a pointer to the retrieved [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface.</span></span> <span data-ttu-id="a1af7-111">呼叫端負責在抓取的介面上呼叫 **Release** 。</span><span class="sxs-lookup"><span data-stu-id="a1af7-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1af7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1af7-112">Return value</span></span>

<span data-ttu-id="a1af7-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="a1af7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a1af7-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="a1af7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a1af7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a1af7-115">Return code</span></span>                                                                                                            | <span data-ttu-id="a1af7-116">Description</span><span class="sxs-lookup"><span data-stu-id="a1af7-116">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a1af7-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a1af7-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="a1af7-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="a1af7-118">The method succeeded.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="a1af7-119"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="a1af7-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="a1af7-120">索引 *鍵* 所指定的屬性不是 **IPortableDevicePropVariantCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="a1af7-120">The property specified by *key* is not an **IPortableDevicePropVariantCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="a1af7-121"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="a1af7-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="a1af7-122">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="a1af7-122">The property specified by *key* is not in the collection.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="a1af7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1af7-123">Requirements</span></span>



| <span data-ttu-id="a1af7-124">需求</span><span class="sxs-lookup"><span data-stu-id="a1af7-124">Requirement</span></span> | <span data-ttu-id="a1af7-125">值</span><span class="sxs-lookup"><span data-stu-id="a1af7-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1af7-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a1af7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a1af7-127"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1af7-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1af7-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1af7-128">Library</span></span><br/> | <dl> <span data-ttu-id="a1af7-129"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1af7-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1af7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1af7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1af7-131">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="a1af7-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a1af7-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="a1af7-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




