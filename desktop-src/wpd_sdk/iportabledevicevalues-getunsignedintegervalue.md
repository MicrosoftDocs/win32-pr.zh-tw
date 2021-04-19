---
description: GetUnsignedIntegerValue 方法會抓取 (type VT \_ UI4) 由索引鍵指定的 ULONG 值。
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'IPortableDeviceValues：： GetUnsignedIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c7deb0b6ebfdb8feb90248f9d8e1cdf68411d9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989728"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a><span data-ttu-id="de462-103">IPortableDeviceValues：： GetUnsignedIntegerValue 方法</span><span class="sxs-lookup"><span data-stu-id="de462-103">IPortableDeviceValues::GetUnsignedIntegerValue method</span></span>

<span data-ttu-id="de462-104">**GetUnsignedIntegerValue** 方法會抓取 ( type VT \_ UI4) 由索引鍵指定的 ULONG 值。</span><span class="sxs-lookup"><span data-stu-id="de462-104">The **GetUnsignedIntegerValue** method retrieves a **ULONG** value (type VT\_UI4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="de462-105">語法</span><span class="sxs-lookup"><span data-stu-id="de462-105">Syntax</span></span>


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="de462-106">參數</span><span class="sxs-lookup"><span data-stu-id="de462-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de462-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de462-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de462-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="de462-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="de462-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="de462-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de462-110">所抓取之 **ULONG** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="de462-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de462-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="de462-111">Return value</span></span>

<span data-ttu-id="de462-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="de462-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="de462-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="de462-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="de462-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="de462-114">Return code</span></span>                                                                                                            | <span data-ttu-id="de462-115">Description</span><span class="sxs-lookup"><span data-stu-id="de462-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="de462-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="de462-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="de462-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="de462-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="de462-118"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="de462-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="de462-119">索引 *鍵* 所指定的屬性不是 **ULONG** 類型。</span><span class="sxs-lookup"><span data-stu-id="de462-119">The property specified by *key* is not a **ULONG** type.</span></span><br/>  |
| <dl> <span data-ttu-id="de462-120"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="de462-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="de462-121">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="de462-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="de462-122">範例</span><span class="sxs-lookup"><span data-stu-id="de462-122">Examples</span></span>

<span data-ttu-id="de462-123">如需如何使用此方法的範例，請參閱抓取 [支援的服務事件](retrieving-supported-events.md)。</span><span class="sxs-lookup"><span data-stu-id="de462-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de462-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="de462-124">Requirements</span></span>



| <span data-ttu-id="de462-125">需求</span><span class="sxs-lookup"><span data-stu-id="de462-125">Requirement</span></span> | <span data-ttu-id="de462-126">值</span><span class="sxs-lookup"><span data-stu-id="de462-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de462-127">標頭</span><span class="sxs-lookup"><span data-stu-id="de462-127">Header</span></span><br/>  | <dl> <span data-ttu-id="de462-128"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="de462-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="de462-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="de462-129">Library</span></span><br/> | <dl> <span data-ttu-id="de462-130"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="de462-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de462-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de462-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de462-132">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="de462-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="de462-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="de462-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span></span>](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="de462-134">正在抓取支援的服務事件</span><span class="sxs-lookup"><span data-stu-id="de462-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="de462-135">正在抓取支援的服務方法</span><span class="sxs-lookup"><span data-stu-id="de462-135">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="de462-136">正在抓取裝置所支援的轉譯功能</span><span class="sxs-lookup"><span data-stu-id="de462-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




