---
description: GetSignedLargeIntegerValue 方法會抓取索引鍵所指定的 LONGLONG 值 (type VT \_ I8) 。
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: 'IPortableDeviceValues：： GetSignedLargeIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5fc41c263ffdef540300a08f88665a6489fa9d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990072"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a><span data-ttu-id="448d9-103">IPortableDeviceValues：： GetSignedLargeIntegerValue 方法</span><span class="sxs-lookup"><span data-stu-id="448d9-103">IPortableDeviceValues::GetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="448d9-104">**GetSignedLargeIntegerValue** 方法會抓取索引鍵所指定的 **LONGLONG** 值 (type VT \_ I8) 。</span><span class="sxs-lookup"><span data-stu-id="448d9-104">The **GetSignedLargeIntegerValue** method retrieves a **LONGLONG** value (type VT\_I8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="448d9-105">語法</span><span class="sxs-lookup"><span data-stu-id="448d9-105">Syntax</span></span>


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="448d9-106">參數</span><span class="sxs-lookup"><span data-stu-id="448d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="448d9-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="448d9-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="448d9-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="448d9-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="448d9-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="448d9-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="448d9-110">所抓取之 **ULONG** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="448d9-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="448d9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="448d9-111">Return value</span></span>

<span data-ttu-id="448d9-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="448d9-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="448d9-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="448d9-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="448d9-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="448d9-114">Return code</span></span>                                                                                                            | <span data-ttu-id="448d9-115">Description</span><span class="sxs-lookup"><span data-stu-id="448d9-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="448d9-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="448d9-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="448d9-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="448d9-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="448d9-118"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="448d9-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="448d9-119">索引 *鍵* 所指定的屬性不是 **LONGLONG** 類型。</span><span class="sxs-lookup"><span data-stu-id="448d9-119">The property specified by *key* is not a **LONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="448d9-120"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="448d9-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="448d9-121">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="448d9-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="448d9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="448d9-122">Requirements</span></span>



| <span data-ttu-id="448d9-123">需求</span><span class="sxs-lookup"><span data-stu-id="448d9-123">Requirement</span></span> | <span data-ttu-id="448d9-124">值</span><span class="sxs-lookup"><span data-stu-id="448d9-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="448d9-125">標頭</span><span class="sxs-lookup"><span data-stu-id="448d9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="448d9-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="448d9-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="448d9-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="448d9-127">Library</span></span><br/> | <dl> <span data-ttu-id="448d9-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="448d9-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="448d9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="448d9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="448d9-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="448d9-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="448d9-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="448d9-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




