---
description: SetUnsignedLargeIntegerValue 方法會將新的 ULONGLONG 值新增 (type VT \_ UI8) 或覆寫現有的值。
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
title: 'IPortableDeviceValues：： SetUnsignedLargeIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c1ade76b4242c7508cb325e90c567349afcdc9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992874"
---
# <a name="iportabledevicevaluessetunsignedlargeintegervalue-method"></a><span data-ttu-id="ffa22-103">IPortableDeviceValues：： SetUnsignedLargeIntegerValue 方法</span><span class="sxs-lookup"><span data-stu-id="ffa22-103">IPortableDeviceValues::SetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="ffa22-104">**SetUnsignedLargeIntegerValue** 方法會將新的 **ULONGLONG** 值新增 (type VT \_ UI8) 或覆寫現有的值。</span><span class="sxs-lookup"><span data-stu-id="ffa22-104">The **SetUnsignedLargeIntegerValue** method adds a new **ULONGLONG** value (type VT\_UI8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa22-105">語法</span><span class="sxs-lookup"><span data-stu-id="ffa22-105">Syntax</span></span>


```C++
HRESULT SetUnsignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONGLONG      Value
);
```



## <a name="parameters"></a><span data-ttu-id="ffa22-106">參數</span><span class="sxs-lookup"><span data-stu-id="ffa22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa22-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffa22-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa22-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="ffa22-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="ffa22-109">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffa22-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa22-110">指定新值的 **ULONGLONG** 。</span><span class="sxs-lookup"><span data-stu-id="ffa22-110">A **ULONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffa22-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ffa22-111">Return value</span></span>

<span data-ttu-id="ffa22-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ffa22-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ffa22-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ffa22-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ffa22-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ffa22-114">Return code</span></span>                                                                          | <span data-ttu-id="ffa22-115">Description</span><span class="sxs-lookup"><span data-stu-id="ffa22-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ffa22-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ffa22-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ffa22-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="ffa22-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ffa22-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffa22-118">Requirements</span></span>



| <span data-ttu-id="ffa22-119">需求</span><span class="sxs-lookup"><span data-stu-id="ffa22-119">Requirement</span></span> | <span data-ttu-id="ffa22-120">值</span><span class="sxs-lookup"><span data-stu-id="ffa22-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa22-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ffa22-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ffa22-122"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="ffa22-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ffa22-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="ffa22-123">Library</span></span><br/> | <dl> <span data-ttu-id="ffa22-124"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffa22-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffa22-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffa22-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa22-126">將資源新增至物件</span><span class="sxs-lookup"><span data-stu-id="ffa22-126">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="ffa22-127">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="ffa22-127">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ffa22-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="ffa22-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-getunsignedlargeintegervalue.md)
</dt> </dl>

 

 




