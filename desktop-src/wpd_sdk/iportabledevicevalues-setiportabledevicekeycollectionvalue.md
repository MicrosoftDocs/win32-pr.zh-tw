---
description: SetIPortableDeviceKeyCollectionValue 方法會將新的 SetIPortableDeviceKeyCollectionValue 值新增 (type VT \_ UNKNOWN) 或覆寫現有的值。
ms.assetid: f470cb89-e7a0-470d-83d1-eb643b062e45
title: 'IPortableDeviceValues：： SetIPortableDeviceKeyCollectionValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: face82230b9dd3bf6cbde18aaee8dd857e17d0a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984021"
---
# <a name="iportabledevicevaluessetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="b90d8-103">IPortableDeviceValues：： SetIPortableDeviceKeyCollectionValue 方法</span><span class="sxs-lookup"><span data-stu-id="b90d8-103">IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="b90d8-104">**SetIPortableDeviceKeyCollectionValue** 方法會將新的 **SetIPortableDeviceKeyCollectionValue** 值新增 (type VT \_ UNKNOWN) 或覆寫現有的值。</span><span class="sxs-lookup"><span data-stu-id="b90d8-104">The **SetIPortableDeviceKeyCollectionValue** method adds a new **SetIPortableDeviceKeyCollectionValue** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="b90d8-105">語法</span><span class="sxs-lookup"><span data-stu-id="b90d8-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceKeyCollectionValue(
  [in] REFPROPERTYKEY               key,
  [in] IPortableDeviceKeyCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="b90d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="b90d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b90d8-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b90d8-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b90d8-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="b90d8-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="b90d8-109">*pValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b90d8-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b90d8-110">**IPortableDeviceKeyCollection** 介面的指標，指定新的值。</span><span class="sxs-lookup"><span data-stu-id="b90d8-110">Pointer to an **IPortableDeviceKeyCollection** interface that specifies the new value.</span></span> <span data-ttu-id="b90d8-111">SDK 會將參考複製到已提交的介面，並在其上呼叫 **AddRef** 。</span><span class="sxs-lookup"><span data-stu-id="b90d8-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b90d8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b90d8-112">Return value</span></span>

<span data-ttu-id="b90d8-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="b90d8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b90d8-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="b90d8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b90d8-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b90d8-115">Return code</span></span>                                                                          | <span data-ttu-id="b90d8-116">Description</span><span class="sxs-lookup"><span data-stu-id="b90d8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b90d8-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b90d8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b90d8-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="b90d8-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b90d8-119">備註</span><span class="sxs-lookup"><span data-stu-id="b90d8-119">Remarks</span></span>

<span data-ttu-id="b90d8-120">如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="b90d8-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="b90d8-121">會適當地釋放現有的金鑰記憶體。</span><span class="sxs-lookup"><span data-stu-id="b90d8-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="b90d8-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b90d8-122">Requirements</span></span>



| <span data-ttu-id="b90d8-123">需求</span><span class="sxs-lookup"><span data-stu-id="b90d8-123">Requirement</span></span> | <span data-ttu-id="b90d8-124">值</span><span class="sxs-lookup"><span data-stu-id="b90d8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b90d8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b90d8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b90d8-126"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="b90d8-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b90d8-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="b90d8-127">Library</span></span><br/> | <dl> <span data-ttu-id="b90d8-128"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b90d8-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b90d8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b90d8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b90d8-130">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="b90d8-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b90d8-131">**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="b90d8-131">**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)
</dt> </dl>

 

 




