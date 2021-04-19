---
description: GetUnsignedLargeIntegerValue 方法會抓取索引鍵所指定的 ULONGLONG 值 (type VT \_ UI8) 。
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: 'IPortableDeviceValues：： GetUnsignedLargeIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 48f6093f32d43737b1999c3474f74569ecd3f8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000709"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a><span data-ttu-id="62c67-103">IPortableDeviceValues：： GetUnsignedLargeIntegerValue 方法</span><span class="sxs-lookup"><span data-stu-id="62c67-103">IPortableDeviceValues::GetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="62c67-104">**GetUnsignedLargeIntegerValue** 方法會抓取索引鍵所指定的 **ULONGLONG** 值 (type VT \_ UI8) 。</span><span class="sxs-lookup"><span data-stu-id="62c67-104">The **GetUnsignedLargeIntegerValue** method retrieves a **ULONGLONG** value (type VT\_UI8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c67-105">語法</span><span class="sxs-lookup"><span data-stu-id="62c67-105">Syntax</span></span>


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="62c67-106">參數</span><span class="sxs-lookup"><span data-stu-id="62c67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c67-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62c67-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c67-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="62c67-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="62c67-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="62c67-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62c67-110">已抓取 **ULONGLONG** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="62c67-110">Pointer to the retrieved **ULONGLONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c67-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="62c67-111">Return value</span></span>

<span data-ttu-id="62c67-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="62c67-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="62c67-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="62c67-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="62c67-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="62c67-114">Return code</span></span>                                                                                                            | <span data-ttu-id="62c67-115">Description</span><span class="sxs-lookup"><span data-stu-id="62c67-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62c67-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="62c67-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="62c67-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="62c67-117">The method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="62c67-118"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="62c67-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="62c67-119">索引 *鍵* 所指定的屬性不是 **ULONGLONG** 類型。</span><span class="sxs-lookup"><span data-stu-id="62c67-119">The property specified by *key* is not a **ULONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="62c67-120"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="62c67-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="62c67-121">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="62c67-121">The property specified by *key* is not in the collection.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="62c67-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="62c67-122">Requirements</span></span>



| <span data-ttu-id="62c67-123">需求</span><span class="sxs-lookup"><span data-stu-id="62c67-123">Requirement</span></span> | <span data-ttu-id="62c67-124">值</span><span class="sxs-lookup"><span data-stu-id="62c67-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62c67-125">標頭</span><span class="sxs-lookup"><span data-stu-id="62c67-125">Header</span></span><br/>  | <dl> <span data-ttu-id="62c67-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="62c67-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="62c67-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="62c67-127">Library</span></span><br/> | <dl> <span data-ttu-id="62c67-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="62c67-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c67-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62c67-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c67-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="62c67-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="62c67-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="62c67-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




