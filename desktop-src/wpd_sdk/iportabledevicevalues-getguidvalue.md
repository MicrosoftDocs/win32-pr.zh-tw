---
description: GetGuidValue 方法會抓取索引鍵所指定的 GUID 值 (類型的 VT \_ CLSID) 。
ms.assetid: 1cfa75e8-2c3b-4893-954e-dae25a6b8220
title: 'IPortableDeviceValues：： GetGuidValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 362672daad835a2e843edeaf6dc517884c25f1ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979466"
---
# <a name="iportabledevicevaluesgetguidvalue-method"></a><span data-ttu-id="52ad5-103">IPortableDeviceValues：： GetGuidValue 方法</span><span class="sxs-lookup"><span data-stu-id="52ad5-103">IPortableDeviceValues::GetGuidValue method</span></span>

<span data-ttu-id="52ad5-104">**GetGuidValue** 方法會抓取索引鍵所指定的 **GUID** 值 (類型的 VT \_ CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="52ad5-104">The **GetGuidValue** method retrieves a **GUID** value (type VT\_CLSID) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="52ad5-105">語法</span><span class="sxs-lookup"><span data-stu-id="52ad5-105">Syntax</span></span>


```C++
HRESULT GetGuidValue(
  [in]  REFPROPERTYKEY key,
  [out] GUID           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="52ad5-106">參數</span><span class="sxs-lookup"><span data-stu-id="52ad5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52ad5-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52ad5-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ad5-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="52ad5-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="52ad5-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="52ad5-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ad5-110">已抓取 **GUID** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="52ad5-110">Pointer to the retrieved **GUID** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52ad5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="52ad5-111">Return value</span></span>

<span data-ttu-id="52ad5-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="52ad5-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="52ad5-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="52ad5-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="52ad5-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="52ad5-114">Return code</span></span>                                                                                                            | <span data-ttu-id="52ad5-115">Description</span><span class="sxs-lookup"><span data-stu-id="52ad5-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="52ad5-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="52ad5-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="52ad5-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="52ad5-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="52ad5-118"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="52ad5-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="52ad5-119">索引 *鍵* 所指定的屬性不是 **GUID** 類型。</span><span class="sxs-lookup"><span data-stu-id="52ad5-119">The property specified by *key* is not a **GUID** type.</span></span><br/>   |
| <dl> <span data-ttu-id="52ad5-120"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="52ad5-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="52ad5-121">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="52ad5-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="52ad5-122">範例</span><span class="sxs-lookup"><span data-stu-id="52ad5-122">Examples</span></span>

<span data-ttu-id="52ad5-123">如需如何使用此方法的範例，請參閱抓取 [支援的服務方法](retrieving-supported-methods.md)。</span><span class="sxs-lookup"><span data-stu-id="52ad5-123">For an example of how to use this method, see [Retrieving Supported Service Methods](retrieving-supported-methods.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52ad5-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="52ad5-124">Requirements</span></span>



| <span data-ttu-id="52ad5-125">需求</span><span class="sxs-lookup"><span data-stu-id="52ad5-125">Requirement</span></span> | <span data-ttu-id="52ad5-126">值</span><span class="sxs-lookup"><span data-stu-id="52ad5-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52ad5-127">標頭</span><span class="sxs-lookup"><span data-stu-id="52ad5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="52ad5-128"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="52ad5-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="52ad5-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="52ad5-129">Library</span></span><br/> | <dl> <span data-ttu-id="52ad5-130"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="52ad5-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52ad5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52ad5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ad5-132">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="52ad5-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="52ad5-133">**IPortableDeviceValues::SetGuidValue**</span><span class="sxs-lookup"><span data-stu-id="52ad5-133">**IPortableDeviceValues::SetGuidValue**</span></span>](iportabledevicevalues-setguidvalue.md)
</dt> <dt>

[<span data-ttu-id="52ad5-134">正在抓取支援的服務方法</span><span class="sxs-lookup"><span data-stu-id="52ad5-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="52ad5-135">正在抓取裝置所支援的轉譯功能</span><span class="sxs-lookup"><span data-stu-id="52ad5-135">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




