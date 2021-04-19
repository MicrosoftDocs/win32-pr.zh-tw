---
description: GetStringValue 方法會抓取索引鍵所指定的字串值 (type VT \_ LPWSTR) 。
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: 'IPortableDeviceValues：： GetStringValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fdb4741c36445af686b7721e1f5f04dd3e45f1e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000431"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a><span data-ttu-id="ac437-103">IPortableDeviceValues：： GetStringValue 方法</span><span class="sxs-lookup"><span data-stu-id="ac437-103">IPortableDeviceValues::GetStringValue method</span></span>

<span data-ttu-id="ac437-104">**GetStringValue** 方法會抓取索引鍵所指定的字串值 (type VT \_ LPWSTR) 。</span><span class="sxs-lookup"><span data-stu-id="ac437-104">The **GetStringValue** method retrieves a string value (type VT\_LPWSTR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac437-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac437-105">Syntax</span></span>


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="ac437-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac437-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac437-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac437-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac437-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ac437-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ac437-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ac437-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac437-110">已抓取 **LPWSTR** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="ac437-110">Pointer to the retrieved **LPWSTR** value.</span></span> <span data-ttu-id="ac437-111">呼叫端負責呼叫 **CoTaskMemFree** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="ac437-111">The caller is responsible for calling **CoTaskMemFree** to release the memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac437-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac437-112">Return value</span></span>

<span data-ttu-id="ac437-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ac437-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ac437-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ac437-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ac437-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ac437-115">Return code</span></span>                                                                                                            | <span data-ttu-id="ac437-116">Description</span><span class="sxs-lookup"><span data-stu-id="ac437-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac437-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ac437-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="ac437-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="ac437-118">The method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ac437-119"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="ac437-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="ac437-120">索引 *鍵* 所指定的屬性不是 **LPWSTR** 類型。</span><span class="sxs-lookup"><span data-stu-id="ac437-120">The property specified by *key* is not an **LPWSTR** type.</span></span><br/> |
| <dl> <span data-ttu-id="ac437-121"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="ac437-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="ac437-122">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="ac437-122">The property specified by *key* is not in the collection.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="ac437-123">範例</span><span class="sxs-lookup"><span data-stu-id="ac437-123">Examples</span></span>

<span data-ttu-id="ac437-124">如需如何使用此方法的範例，請參閱抓取 [支援的服務事件](retrieving-supported-events.md)。</span><span class="sxs-lookup"><span data-stu-id="ac437-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac437-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac437-125">Requirements</span></span>



| <span data-ttu-id="ac437-126">需求</span><span class="sxs-lookup"><span data-stu-id="ac437-126">Requirement</span></span> | <span data-ttu-id="ac437-127">值</span><span class="sxs-lookup"><span data-stu-id="ac437-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac437-128">標頭</span><span class="sxs-lookup"><span data-stu-id="ac437-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ac437-129"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac437-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac437-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="ac437-130">Library</span></span><br/> | <dl> <span data-ttu-id="ac437-131"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac437-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac437-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac437-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac437-133">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="ac437-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ac437-134">**IPortableDeviceValues：： GetAt**</span><span class="sxs-lookup"><span data-stu-id="ac437-134">**IPortableDeviceValues::GetAt**</span></span>](iportabledevicevalues-getat.md)
</dt> <dt>

[<span data-ttu-id="ac437-135">**IPortableDeviceValues：： SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="ac437-135">**IPortableDeviceValues::SetStringValue**</span></span>](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[<span data-ttu-id="ac437-136">正在抓取支援的服務事件</span><span class="sxs-lookup"><span data-stu-id="ac437-136">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="ac437-137">正在抓取支援的服務格式</span><span class="sxs-lookup"><span data-stu-id="ac437-137">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="ac437-138">正在抓取支援的服務方法</span><span class="sxs-lookup"><span data-stu-id="ac437-138">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




