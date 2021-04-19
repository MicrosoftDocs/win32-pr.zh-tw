---
description: GetBoolValue 方法會抓取布林值， (由索引 \_ 鍵指定的 VT BOOL) 類型。
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'IPortableDeviceValues：： GetBoolValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994248"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a><span data-ttu-id="bca4d-103">IPortableDeviceValues：： GetBoolValue 方法</span><span class="sxs-lookup"><span data-stu-id="bca4d-103">IPortableDeviceValues::GetBoolValue method</span></span>

<span data-ttu-id="bca4d-104">**GetBoolValue** 方法會抓取 **布林** 值， (由索引 \_ 鍵指定的 VT BOOL) 類型。</span><span class="sxs-lookup"><span data-stu-id="bca4d-104">The **GetBoolValue** method retrieves a **Boolean** value (type VT\_BOOL) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="bca4d-105">語法</span><span class="sxs-lookup"><span data-stu-id="bca4d-105">Syntax</span></span>


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="bca4d-106">參數</span><span class="sxs-lookup"><span data-stu-id="bca4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bca4d-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bca4d-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bca4d-108">指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="bca4d-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="bca4d-109">*pValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bca4d-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bca4d-110">已抓取之 **BOOL** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="bca4d-110">Pointer to the retrieved **BOOL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bca4d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bca4d-111">Return value</span></span>

<span data-ttu-id="bca4d-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bca4d-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bca4d-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="bca4d-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bca4d-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bca4d-114">Return code</span></span>                                                                                                            | <span data-ttu-id="bca4d-115">Description</span><span class="sxs-lookup"><span data-stu-id="bca4d-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="bca4d-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bca4d-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="bca4d-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="bca4d-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="bca4d-118"><dt>**將 \_ 電子 \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="bca4d-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="bca4d-119">索引 *鍵* 所指定的屬性不是 **BOOL** 類型。</span><span class="sxs-lookup"><span data-stu-id="bca4d-119">The property specified by *key* is not a **BOOL** type.</span></span><br/>   |
| <dl> <span data-ttu-id="bca4d-120"><dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt></span><span class="sxs-lookup"><span data-stu-id="bca4d-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="bca4d-121">索引 *鍵* 所指定的屬性不在集合中。</span><span class="sxs-lookup"><span data-stu-id="bca4d-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="bca4d-122">範例</span><span class="sxs-lookup"><span data-stu-id="bca4d-122">Examples</span></span>

<span data-ttu-id="bca4d-123">如需如何使用此方法的範例，請參閱 [設定單一物件的屬性](setting-properties-for-a-single-object.md)。</span><span class="sxs-lookup"><span data-stu-id="bca4d-123">For an example of how to use this method, see [Setting Properties for a Single Object](setting-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bca4d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="bca4d-124">Requirements</span></span>



| <span data-ttu-id="bca4d-125">需求</span><span class="sxs-lookup"><span data-stu-id="bca4d-125">Requirement</span></span> | <span data-ttu-id="bca4d-126">值</span><span class="sxs-lookup"><span data-stu-id="bca4d-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bca4d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="bca4d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bca4d-128"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="bca4d-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="bca4d-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="bca4d-129">Library</span></span><br/> | <dl> <span data-ttu-id="bca4d-130"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bca4d-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bca4d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bca4d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bca4d-132">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="bca4d-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="bca4d-133">**IPortableDeviceValues：： SetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="bca4d-133">**IPortableDeviceValues::SetBoolValue**</span></span>](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[<span data-ttu-id="bca4d-134">正在抓取支援的服務事件</span><span class="sxs-lookup"><span data-stu-id="bca4d-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="bca4d-135">設定單一物件的屬性</span><span class="sxs-lookup"><span data-stu-id="bca4d-135">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="bca4d-136">寫入內容物件屬性</span><span class="sxs-lookup"><span data-stu-id="bca4d-136">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




