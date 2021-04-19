---
description: GetIUnknownValue 方法會抓取 IUnknown 介面值， (輸入 \_ 由索引鍵指定的 VT 未知) 。
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'IPortableDeviceValues：： GetIUnknownValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995975"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a><span data-ttu-id="48a09-103">IPortableDeviceValues：： GetIUnknownValue 方法</span><span class="sxs-lookup"><span data-stu-id="48a09-103">IPortableDeviceValues::GetIUnknownValue method</span></span>

<span data-ttu-id="48a09-104">**GetIUnknownValue** 方法會抓取 **IUnknown** 介面值， (輸入由索引鍵指定的 VT \_ 未知) 。</span><span class="sxs-lookup"><span data-stu-id="48a09-104">The **GetIUnknownValue** method retrieves an **IUnknown** interface value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a09-105">語法</span><span class="sxs-lookup"><span data-stu-id="48a09-105">Syntax</span></span>


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="48a09-106">參數</span><span class="sxs-lookup"><span data-stu-id="48a09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a09-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48a09-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48a09-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="48a09-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="48a09-109">*ppValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="48a09-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48a09-110">接收所抓取 **IUnknown** 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="48a09-110">Address of a variable that receives a pointer to the retrieved **IUnknown** interface.</span></span> <span data-ttu-id="48a09-111">呼叫端負責在抓取的介面上呼叫 **Release** 。</span><span class="sxs-lookup"><span data-stu-id="48a09-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a09-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="48a09-112">Return value</span></span>

<span data-ttu-id="48a09-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="48a09-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="48a09-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="48a09-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="48a09-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="48a09-115">Return code</span></span>                                                                                                            | <span data-ttu-id="48a09-116">Description</span><span class="sxs-lookup"><span data-stu-id="48a09-116">Description</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48a09-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="48a09-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="48a09-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="48a09-118">The method succeeded.</span></span><br/>                                             |
| <dl> <span data-ttu-id="48a09-119"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="48a09-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="48a09-120">索引 *鍵* 所指定的屬性不是 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="48a09-120">The property specified by *key* is not an **IUnknown** interface.</span></span><br/> |
| <dl> <span data-ttu-id="48a09-121"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="48a09-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="48a09-122">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="48a09-122">The property specified by *key* is not in the collection.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="48a09-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="48a09-123">Requirements</span></span>



| <span data-ttu-id="48a09-124">需求</span><span class="sxs-lookup"><span data-stu-id="48a09-124">Requirement</span></span> | <span data-ttu-id="48a09-125">值</span><span class="sxs-lookup"><span data-stu-id="48a09-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a09-126">標頭</span><span class="sxs-lookup"><span data-stu-id="48a09-126">Header</span></span><br/>  | <dl> <span data-ttu-id="48a09-127"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="48a09-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="48a09-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="48a09-128">Library</span></span><br/> | <dl> <span data-ttu-id="48a09-129"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="48a09-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48a09-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48a09-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a09-131">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="48a09-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="48a09-132">**IPortableDeviceValues::SetIUnknownValue**</span><span class="sxs-lookup"><span data-stu-id="48a09-132">**IPortableDeviceValues::SetIUnknownValue**</span></span>](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




