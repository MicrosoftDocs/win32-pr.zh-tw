---
description: GetIPortableDeviceValuesValue 方法會抓取索引鍵所指定的 IPortableDeviceValues 值， (類型 \_ 為 VT 未知) 。
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'IPortableDeviceValues：： GetIPortableDeviceValuesValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9583ea157c1e3395fd9814b1a2e78af3f1985b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984419"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a><span data-ttu-id="5090b-103">IPortableDeviceValues：： GetIPortableDeviceValuesValue 方法</span><span class="sxs-lookup"><span data-stu-id="5090b-103">IPortableDeviceValues::GetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="5090b-104">**GetIPortableDeviceValuesValue** 方法會抓取索引鍵所指定的 **IPortableDeviceValues** 值， (類型 \_ 為 VT 未知) 。</span><span class="sxs-lookup"><span data-stu-id="5090b-104">The **GetIPortableDeviceValuesValue** method retrieves an **IPortableDeviceValues** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="5090b-105">語法</span><span class="sxs-lookup"><span data-stu-id="5090b-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="5090b-106">參數</span><span class="sxs-lookup"><span data-stu-id="5090b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5090b-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5090b-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5090b-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="5090b-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="5090b-109">*ppValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5090b-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5090b-110">接收已抓取 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="5090b-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span> <span data-ttu-id="5090b-111">呼叫端負責在抓取的介面上呼叫 **Release** 。</span><span class="sxs-lookup"><span data-stu-id="5090b-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5090b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5090b-112">Return value</span></span>

<span data-ttu-id="5090b-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="5090b-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5090b-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="5090b-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5090b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5090b-115">Return code</span></span>                                                                                                            | <span data-ttu-id="5090b-116">Description</span><span class="sxs-lookup"><span data-stu-id="5090b-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5090b-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5090b-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="5090b-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="5090b-118">The method succeeded.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="5090b-119"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="5090b-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="5090b-120">索引 *鍵* 所指定的屬性不是 **IPortableDeviceValues** 介面。</span><span class="sxs-lookup"><span data-stu-id="5090b-120">The property specified by *key* is not an **IPortableDeviceValues** interface.</span></span><br/> |
| <dl> <span data-ttu-id="5090b-121"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="5090b-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="5090b-122">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="5090b-122">The property specified by *key* is not in the collection.</span></span><br/>                      |



 

## <a name="examples"></a><span data-ttu-id="5090b-123">範例</span><span class="sxs-lookup"><span data-stu-id="5090b-123">Examples</span></span>

<span data-ttu-id="5090b-124">如需如何使用此方法的範例，請參閱抓取 [支援的服務事件](retrieving-supported-events.md)。</span><span class="sxs-lookup"><span data-stu-id="5090b-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5090b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5090b-125">Requirements</span></span>



| <span data-ttu-id="5090b-126">需求</span><span class="sxs-lookup"><span data-stu-id="5090b-126">Requirement</span></span> | <span data-ttu-id="5090b-127">值</span><span class="sxs-lookup"><span data-stu-id="5090b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5090b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="5090b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5090b-129"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="5090b-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5090b-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="5090b-130">Library</span></span><br/> | <dl> <span data-ttu-id="5090b-131"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5090b-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5090b-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5090b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5090b-133">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="5090b-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="5090b-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span><span class="sxs-lookup"><span data-stu-id="5090b-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[<span data-ttu-id="5090b-135">正在抓取支援的服務事件</span><span class="sxs-lookup"><span data-stu-id="5090b-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="5090b-136">正在抓取裝置所支援的轉譯功能</span><span class="sxs-lookup"><span data-stu-id="5090b-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




