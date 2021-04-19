---
description: SetIUnknownValue 方法會將新的 IUnknown 值新增 (類型 VT \_ 未知) 或覆寫現有的值。
ms.assetid: 292adf45-439c-4aae-9b17-e4d9ed701eda
title: 'IPortableDeviceValues：： SetIUnknownValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2c3a27fe5ea89359884d70162000b5164b7c1aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994031"
---
# <a name="iportabledevicevaluessetiunknownvalue-method"></a><span data-ttu-id="f3847-103">IPortableDeviceValues：： SetIUnknownValue 方法</span><span class="sxs-lookup"><span data-stu-id="f3847-103">IPortableDeviceValues::SetIUnknownValue method</span></span>

<span data-ttu-id="f3847-104">**SetIUnknownValue** 方法會將新的 **IUnknown** 值新增 (類型 VT \_ 未知) 或覆寫現有的值。</span><span class="sxs-lookup"><span data-stu-id="f3847-104">The **SetIUnknownValue** method adds a new **IUnknown** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3847-105">語法</span><span class="sxs-lookup"><span data-stu-id="f3847-105">Syntax</span></span>


```C++
HRESULT SetIUnknownValue(
  [in] REFPROPERTYKEY key,
  [in] IUnknown       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="f3847-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3847-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3847-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3847-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3847-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="f3847-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="f3847-109">*pValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3847-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3847-110">指定新值的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f3847-110">A pointer to an **IUnknown** interface that specifies the new value.</span></span> <span data-ttu-id="f3847-111">SDK 會將參考複製到已提交的介面，並在其上呼叫 **AddRef** 。</span><span class="sxs-lookup"><span data-stu-id="f3847-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3847-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3847-112">Return value</span></span>

<span data-ttu-id="f3847-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f3847-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f3847-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f3847-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f3847-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f3847-115">Return code</span></span>                                                                          | <span data-ttu-id="f3847-116">Description</span><span class="sxs-lookup"><span data-stu-id="f3847-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f3847-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f3847-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f3847-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f3847-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f3847-119">備註</span><span class="sxs-lookup"><span data-stu-id="f3847-119">Remarks</span></span>

<span data-ttu-id="f3847-120">如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="f3847-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="f3847-121">會適當地釋放現有的金鑰記憶體。</span><span class="sxs-lookup"><span data-stu-id="f3847-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3847-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3847-122">Requirements</span></span>



| <span data-ttu-id="f3847-123">需求</span><span class="sxs-lookup"><span data-stu-id="f3847-123">Requirement</span></span> | <span data-ttu-id="f3847-124">值</span><span class="sxs-lookup"><span data-stu-id="f3847-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3847-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f3847-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f3847-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3847-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3847-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="f3847-127">Library</span></span><br/> | <dl> <span data-ttu-id="f3847-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3847-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3847-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3847-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3847-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="f3847-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f3847-131">**IPortableDeviceValues::GetIUnknownValue**</span><span class="sxs-lookup"><span data-stu-id="f3847-131">**IPortableDeviceValues::GetIUnknownValue**</span></span>](iportabledevicevalues-getiunknownvalue.md)
</dt> </dl>

 

 




