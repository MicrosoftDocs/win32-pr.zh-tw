---
description: GetIPortableDeviceValuesCollectionValue 方法會抓取索引鍵所指定的 IPortableDeviceValuesCollection 值， (類型 \_ 為 VT 未知) 。
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'IPortableDeviceValues：： GetIPortableDeviceValuesCollectionValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994247"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="dea32-103">IPortableDeviceValues：： GetIPortableDeviceValuesCollectionValue 方法</span><span class="sxs-lookup"><span data-stu-id="dea32-103">IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="dea32-104">**GetIPortableDeviceValuesCollectionValue** 方法會抓取索引鍵所指定的 **IPortableDeviceValuesCollection** 值， (類型 \_ 為 VT 未知) 。</span><span class="sxs-lookup"><span data-stu-id="dea32-104">The **GetIPortableDeviceValuesCollectionValue** method retrieves an **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea32-105">語法</span><span class="sxs-lookup"><span data-stu-id="dea32-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="dea32-106">參數</span><span class="sxs-lookup"><span data-stu-id="dea32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea32-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dea32-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea32-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="dea32-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="dea32-109">*ppValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dea32-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea32-110">接收已抓取 [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="dea32-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) interface.</span></span> <span data-ttu-id="dea32-111">呼叫端負責在抓取的介面上呼叫 **Release** 。</span><span class="sxs-lookup"><span data-stu-id="dea32-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea32-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dea32-112">Return value</span></span>

<span data-ttu-id="dea32-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="dea32-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dea32-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="dea32-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dea32-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dea32-115">Return code</span></span>                                                                                                            | <span data-ttu-id="dea32-116">Description</span><span class="sxs-lookup"><span data-stu-id="dea32-116">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dea32-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dea32-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="dea32-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="dea32-118">The method succeeded.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="dea32-119"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="dea32-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="dea32-120">索引 *鍵* 所指定的屬性不是 **IPortableDeviceValuesCollection** 介面。</span><span class="sxs-lookup"><span data-stu-id="dea32-120">The property specified by *key* is not an **IPortableDeviceValuesCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="dea32-121"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="dea32-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="dea32-122">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="dea32-122">The property specified by *key* is not in the collection.</span></span><br/>                                |



 

## <a name="examples"></a><span data-ttu-id="dea32-123">範例</span><span class="sxs-lookup"><span data-stu-id="dea32-123">Examples</span></span>

<span data-ttu-id="dea32-124">如需如何使用此方法的範例，請參閱抓取 [裝置所支援的轉譯功能](retrieving-the-rendering-capabilities-supported-by-a-device.md)。</span><span class="sxs-lookup"><span data-stu-id="dea32-124">For an example of how to use this method, see [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dea32-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="dea32-125">Requirements</span></span>



| <span data-ttu-id="dea32-126">需求</span><span class="sxs-lookup"><span data-stu-id="dea32-126">Requirement</span></span> | <span data-ttu-id="dea32-127">值</span><span class="sxs-lookup"><span data-stu-id="dea32-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea32-128">標頭</span><span class="sxs-lookup"><span data-stu-id="dea32-128">Header</span></span><br/>  | <dl> <span data-ttu-id="dea32-129"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="dea32-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="dea32-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="dea32-130">Library</span></span><br/> | <dl> <span data-ttu-id="dea32-131"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dea32-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dea32-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dea32-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea32-133">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="dea32-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="dea32-134">正在抓取裝置所支援的轉譯功能</span><span class="sxs-lookup"><span data-stu-id="dea32-134">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="dea32-135">**SetIPortableDeviceValuesCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="dea32-135">**SetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




