---
description: SetStringValue 方法會將新的字串值新增 (type VT \_ LPWSTR) 或覆寫現有的字串值。
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'IPortableDeviceValues：： SetStringValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981347"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a><span data-ttu-id="d3bdb-103">IPortableDeviceValues：： SetStringValue 方法</span><span class="sxs-lookup"><span data-stu-id="d3bdb-103">IPortableDeviceValues::SetStringValue method</span></span>

<span data-ttu-id="d3bdb-104">**SetStringValue** 方法會將新的字串值新增 (type VT \_ LPWSTR) 或覆寫現有的字串值。</span><span class="sxs-lookup"><span data-stu-id="d3bdb-104">The **SetStringValue** method adds a new string value (type VT\_LPWSTR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3bdb-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3bdb-105">Syntax</span></span>


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a><span data-ttu-id="d3bdb-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3bdb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3bdb-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3bdb-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3bdb-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="d3bdb-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="d3bdb-109">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3bdb-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3bdb-110">指定新值的 **LPCWSTR** 。</span><span class="sxs-lookup"><span data-stu-id="d3bdb-110">A **LPCWSTR** that specifies the new value.</span></span> <span data-ttu-id="d3bdb-111">會複製字串，讓呼叫端可以在呼叫這個方法之後釋放配置給這個值的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d3bdb-111">The string is copied, so the caller can release the memory allocated for this value after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3bdb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3bdb-112">Return value</span></span>

<span data-ttu-id="d3bdb-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d3bdb-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d3bdb-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d3bdb-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d3bdb-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d3bdb-115">Return code</span></span>                                                                          | <span data-ttu-id="d3bdb-116">Description</span><span class="sxs-lookup"><span data-stu-id="d3bdb-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d3bdb-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d3bdb-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d3bdb-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d3bdb-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3bdb-119">備註</span><span class="sxs-lookup"><span data-stu-id="d3bdb-119">Remarks</span></span>

<span data-ttu-id="d3bdb-120">任何現有的金鑰記憶體都會適當地發行。</span><span class="sxs-lookup"><span data-stu-id="d3bdb-120">Any existing key memory will be released appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="d3bdb-121">範例</span><span class="sxs-lookup"><span data-stu-id="d3bdb-121">Examples</span></span>

<span data-ttu-id="d3bdb-122">如需如何使用此方法的範例，請參閱 [指定用戶端資訊](specifying-client-information.md)。</span><span class="sxs-lookup"><span data-stu-id="d3bdb-122">For an example of how to use this method, see [Specifying Client Information](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3bdb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3bdb-123">Requirements</span></span>



| <span data-ttu-id="d3bdb-124">需求</span><span class="sxs-lookup"><span data-stu-id="d3bdb-124">Requirement</span></span> | <span data-ttu-id="d3bdb-125">值</span><span class="sxs-lookup"><span data-stu-id="d3bdb-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3bdb-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d3bdb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d3bdb-127"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3bdb-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3bdb-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3bdb-128">Library</span></span><br/> | <dl> <span data-ttu-id="d3bdb-129"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3bdb-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3bdb-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3bdb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3bdb-131">將資源新增至物件</span><span class="sxs-lookup"><span data-stu-id="d3bdb-131">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="d3bdb-132">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="d3bdb-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d3bdb-133">**IPortableDeviceValues：： GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="d3bdb-133">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[<span data-ttu-id="d3bdb-134">設定單一物件的屬性</span><span class="sxs-lookup"><span data-stu-id="d3bdb-134">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="d3bdb-135">設定多個物件的屬性</span><span class="sxs-lookup"><span data-stu-id="d3bdb-135">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> <dt>

[<span data-ttu-id="d3bdb-136">指定用戶端資訊</span><span class="sxs-lookup"><span data-stu-id="d3bdb-136">Specifying Client Information</span></span>](specifying-client-information.md)
</dt> <dt>

[<span data-ttu-id="d3bdb-137">寫入內容物件屬性</span><span class="sxs-lookup"><span data-stu-id="d3bdb-137">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




