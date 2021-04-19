---
description: GetSignedIntegerValue 方法會抓取 (type VT \_ I4) 由索引鍵指定的 LONG 值。
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
title: 'IPortableDeviceValues：： GetSignedIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2fe0c2f8714d3fa28f61624924eba169f9f1c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990095"
---
# <a name="iportabledevicevaluesgetsignedintegervalue-method"></a><span data-ttu-id="33cae-103">IPortableDeviceValues：： GetSignedIntegerValue 方法</span><span class="sxs-lookup"><span data-stu-id="33cae-103">IPortableDeviceValues::GetSignedIntegerValue method</span></span>

<span data-ttu-id="33cae-104">**GetSignedIntegerValue** 方法會抓取 ( type VT \_ I4) 由索引鍵指定的 LONG 值。</span><span class="sxs-lookup"><span data-stu-id="33cae-104">The **GetSignedIntegerValue** method retrieves a **LONG** value (type VT\_I4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="33cae-105">語法</span><span class="sxs-lookup"><span data-stu-id="33cae-105">Syntax</span></span>


```C++
HRESULT GetSignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONG           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="33cae-106">參數</span><span class="sxs-lookup"><span data-stu-id="33cae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33cae-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33cae-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33cae-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="33cae-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="33cae-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="33cae-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33cae-110">已抓取之 **完整** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="33cae-110">Pointer to the retrieved **LONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33cae-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="33cae-111">Return value</span></span>

<span data-ttu-id="33cae-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="33cae-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="33cae-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="33cae-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="33cae-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="33cae-114">Return code</span></span>                                                                                                            | <span data-ttu-id="33cae-115">Description</span><span class="sxs-lookup"><span data-stu-id="33cae-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="33cae-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="33cae-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="33cae-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="33cae-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="33cae-118"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="33cae-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="33cae-119">索引 *鍵* 指定的屬性不是 **LONG** 類型。</span><span class="sxs-lookup"><span data-stu-id="33cae-119">The property specified by *key* is not a **LONG** type.</span></span><br/>   |
| <dl> <span data-ttu-id="33cae-120"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="33cae-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="33cae-121">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="33cae-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="33cae-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="33cae-122">Requirements</span></span>



| <span data-ttu-id="33cae-123">需求</span><span class="sxs-lookup"><span data-stu-id="33cae-123">Requirement</span></span> | <span data-ttu-id="33cae-124">值</span><span class="sxs-lookup"><span data-stu-id="33cae-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33cae-125">標頭</span><span class="sxs-lookup"><span data-stu-id="33cae-125">Header</span></span><br/>  | <dl> <span data-ttu-id="33cae-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="33cae-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="33cae-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="33cae-127">Library</span></span><br/> | <dl> <span data-ttu-id="33cae-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="33cae-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33cae-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33cae-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33cae-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="33cae-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="33cae-131">**IPortableDeviceValues::SetSignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="33cae-131">**IPortableDeviceValues::SetSignedIntegerValue**</span></span>](iportabledevicevalues-setsignedintegervalue.md)
</dt> </dl>

 

 




