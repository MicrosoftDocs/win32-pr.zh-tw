---
description: GetIPortableDeviceKeyCollectionValue 方法會抓取索引鍵所指定的 IPortableDeviceKeyCollection 值， (類型 \_ 為 VT 未知) 。
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'IPortableDeviceValues：： GetIPortableDeviceKeyCollectionValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976077"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="bddd7-103">IPortableDeviceValues：： GetIPortableDeviceKeyCollectionValue 方法</span><span class="sxs-lookup"><span data-stu-id="bddd7-103">IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="bddd7-104">**GetIPortableDeviceKeyCollectionValue** 方法會抓取索引鍵所指定的 **IPortableDeviceKeyCollection** 值， (類型 \_ 為 VT 未知) 。</span><span class="sxs-lookup"><span data-stu-id="bddd7-104">The **GetIPortableDeviceKeyCollectionValue** method retrieves an **IPortableDeviceKeyCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="bddd7-105">語法</span><span class="sxs-lookup"><span data-stu-id="bddd7-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="bddd7-106">參數</span><span class="sxs-lookup"><span data-stu-id="bddd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bddd7-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bddd7-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bddd7-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="bddd7-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="bddd7-109">*ppValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bddd7-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bddd7-110">已抓取 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) 介面指標的指標。</span><span class="sxs-lookup"><span data-stu-id="bddd7-110">Pointer to the retrieved [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface pointer.</span></span> <span data-ttu-id="bddd7-111">呼叫端負責在抓取的介面上呼叫 **Release** 。</span><span class="sxs-lookup"><span data-stu-id="bddd7-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bddd7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bddd7-112">Return value</span></span>

<span data-ttu-id="bddd7-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bddd7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bddd7-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="bddd7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bddd7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bddd7-115">Return code</span></span>                                                                                                            | <span data-ttu-id="bddd7-116">Description</span><span class="sxs-lookup"><span data-stu-id="bddd7-116">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bddd7-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bddd7-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="bddd7-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="bddd7-118">The method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="bddd7-119"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="bddd7-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="bddd7-120">索引 *鍵* 所指定的屬性不是 **IPortableDeviceKeyCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="bddd7-120">The property specified by *key* is not an **IPortableDeviceKeyCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="bddd7-121"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="bddd7-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="bddd7-122">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="bddd7-122">The property specified by *key* is not in the collection.</span></span><br/>                             |



 

## <a name="examples"></a><span data-ttu-id="bddd7-123">範例</span><span class="sxs-lookup"><span data-stu-id="bddd7-123">Examples</span></span>

<span data-ttu-id="bddd7-124">如需如何使用此方法的範例，請參閱抓取 [支援的服務事件](retrieving-supported-events.md)。</span><span class="sxs-lookup"><span data-stu-id="bddd7-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bddd7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bddd7-125">Requirements</span></span>



| <span data-ttu-id="bddd7-126">需求</span><span class="sxs-lookup"><span data-stu-id="bddd7-126">Requirement</span></span> | <span data-ttu-id="bddd7-127">值</span><span class="sxs-lookup"><span data-stu-id="bddd7-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bddd7-128">標頭</span><span class="sxs-lookup"><span data-stu-id="bddd7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bddd7-129"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="bddd7-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="bddd7-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="bddd7-130">Library</span></span><br/> | <dl> <span data-ttu-id="bddd7-131"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bddd7-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bddd7-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bddd7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddd7-133">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="bddd7-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="bddd7-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="bddd7-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[<span data-ttu-id="bddd7-135">正在抓取支援的服務事件</span><span class="sxs-lookup"><span data-stu-id="bddd7-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="bddd7-136">正在抓取支援的服務方法</span><span class="sxs-lookup"><span data-stu-id="bddd7-136">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




