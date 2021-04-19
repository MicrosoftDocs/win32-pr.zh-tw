---
description: GetErrorValue 方法會抓取 (的 HRESULT 值， \_) 由索引鍵指定的 VT 錯誤。
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
title: 'IPortableDeviceValues：： GetErrorValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 86e5dacfa398cfe2bb57bfd289e4c8e792f14a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981291"
---
# <a name="iportabledevicevaluesgeterrorvalue-method"></a><span data-ttu-id="d5bcb-103">IPortableDeviceValues：： GetErrorValue 方法</span><span class="sxs-lookup"><span data-stu-id="d5bcb-103">IPortableDeviceValues::GetErrorValue method</span></span>

<span data-ttu-id="d5bcb-104">**GetErrorValue** 方法會抓取 (的 **HRESULT** 值， \_) 由索引鍵指定的 VT 錯誤。</span><span class="sxs-lookup"><span data-stu-id="d5bcb-104">The **GetErrorValue** method retrieves an **HRESULT** value (type VT\_ERROR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5bcb-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5bcb-105">Syntax</span></span>


```C++
HRESULT GetErrorValue(
  [in]  REFPROPERTYKEY key,
  [out] HRESULT        *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="d5bcb-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5bcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5bcb-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5bcb-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5bcb-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="d5bcb-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d5bcb-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d5bcb-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5bcb-110">已抓取之 **HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="d5bcb-110">Pointer to the retrieved **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5bcb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5bcb-111">Return value</span></span>

<span data-ttu-id="d5bcb-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d5bcb-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d5bcb-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d5bcb-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d5bcb-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d5bcb-114">Return code</span></span>                                                                                                            | <span data-ttu-id="d5bcb-115">Description</span><span class="sxs-lookup"><span data-stu-id="d5bcb-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5bcb-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d5bcb-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="d5bcb-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d5bcb-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="d5bcb-118"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="d5bcb-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="d5bcb-119">索引 *鍵* 所指定的屬性不是 **HRESULT** 型別。</span><span class="sxs-lookup"><span data-stu-id="d5bcb-119">The property specified by *key* is not an **HRESULT** type.</span></span><br/> |
| <dl> <span data-ttu-id="d5bcb-120"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="d5bcb-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="d5bcb-121">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="d5bcb-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="d5bcb-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5bcb-122">Requirements</span></span>



| <span data-ttu-id="d5bcb-123">需求</span><span class="sxs-lookup"><span data-stu-id="d5bcb-123">Requirement</span></span> | <span data-ttu-id="d5bcb-124">值</span><span class="sxs-lookup"><span data-stu-id="d5bcb-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5bcb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d5bcb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d5bcb-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5bcb-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5bcb-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5bcb-127">Library</span></span><br/> | <dl> <span data-ttu-id="d5bcb-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5bcb-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5bcb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5bcb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5bcb-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="d5bcb-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d5bcb-131">**IPortableDeviceValues::SetErrorValue**</span><span class="sxs-lookup"><span data-stu-id="d5bcb-131">**IPortableDeviceValues::SetErrorValue**</span></span>](iportabledevicevalues-seterrorvalue.md)
</dt> </dl>

 

 




