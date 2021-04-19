---
description: GetBufferValue 方法會抓取位元組陣列值， (type \_ \|) 由索引鍵指定的 vt 向量 VT \_ UI1。
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'IPortableDeviceValues：： GetBufferValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e5b98bb412ed648cf6ac74ec457b1e6032c009ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987909"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a><span data-ttu-id="54dd0-103">IPortableDeviceValues：： GetBufferValue 方法</span><span class="sxs-lookup"><span data-stu-id="54dd0-103">IPortableDeviceValues::GetBufferValue method</span></span>

<span data-ttu-id="54dd0-104">**GetBufferValue** 方法會抓取 **位元組陣列** 值， (type \_ \|) 由索引鍵指定的 vt 向量 VT \_ UI1。</span><span class="sxs-lookup"><span data-stu-id="54dd0-104">The **GetBufferValue** method retrieves a **byte array** value (type VT\_VECTOR \| VT\_UI1) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="54dd0-105">語法</span><span class="sxs-lookup"><span data-stu-id="54dd0-105">Syntax</span></span>


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
);
```



## <a name="parameters"></a><span data-ttu-id="54dd0-106">參數</span><span class="sxs-lookup"><span data-stu-id="54dd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54dd0-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54dd0-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54dd0-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="54dd0-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="54dd0-109">*ppValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="54dd0-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54dd0-110">所抓取 \*\*位元組 \* \*_ 值的指標。呼叫者負責呼叫 _ CoTaskMemFree 來釋放記憶體\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="54dd0-110">Pointer to the retrieved \**BYTE\**_ value. The caller is responsible for freeing the memory by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="54dd0-111">*pcbValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="54dd0-111">*pcbValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54dd0-112">*PpValue* 大小的指標（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="54dd0-112">Pointer to the size of *ppValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54dd0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="54dd0-113">Return value</span></span>

<span data-ttu-id="54dd0-114">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="54dd0-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="54dd0-115">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="54dd0-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="54dd0-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="54dd0-116">Return code</span></span>                                                                                                            | <span data-ttu-id="54dd0-117">Description</span><span class="sxs-lookup"><span data-stu-id="54dd0-117">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="54dd0-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="54dd0-118"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="54dd0-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="54dd0-119">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="54dd0-120"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="54dd0-120"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="54dd0-121">索引 *鍵* 所指定的屬性不是 **位元組** \* 類型。</span><span class="sxs-lookup"><span data-stu-id="54dd0-121">The property specified by *key* is not a **BYTE**\* type.</span></span><br/> |
| <dl> <span data-ttu-id="54dd0-122"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="54dd0-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="54dd0-123">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="54dd0-123">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54dd0-124">備註</span><span class="sxs-lookup"><span data-stu-id="54dd0-124">Remarks</span></span>

<span data-ttu-id="54dd0-125">不支援取出 **Null** 緩衝區或零大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="54dd0-125">Retrieving a **NULL** buffer or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="54dd0-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="54dd0-126">Requirements</span></span>



| <span data-ttu-id="54dd0-127">需求</span><span class="sxs-lookup"><span data-stu-id="54dd0-127">Requirement</span></span> | <span data-ttu-id="54dd0-128">值</span><span class="sxs-lookup"><span data-stu-id="54dd0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54dd0-129">標頭</span><span class="sxs-lookup"><span data-stu-id="54dd0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="54dd0-130"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="54dd0-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="54dd0-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="54dd0-131">Library</span></span><br/> | <dl> <span data-ttu-id="54dd0-132"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="54dd0-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54dd0-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54dd0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54dd0-134">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="54dd0-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="54dd0-135">**IPortableDeviceValues::SetBufferValue**</span><span class="sxs-lookup"><span data-stu-id="54dd0-135">**IPortableDeviceValues::SetBufferValue**</span></span>](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




