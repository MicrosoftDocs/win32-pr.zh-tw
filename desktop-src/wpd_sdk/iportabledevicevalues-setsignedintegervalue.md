---
description: SetSignedIntegerValue 方法會將新的 LONG 值新增 (type VT \_ I4) 或覆寫現有的值。
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
title: 'IPortableDeviceValues：： SetSignedIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 26a5d01ec69203c39008de394e3693acc833d262
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989558"
---
# <a name="iportabledevicevaluessetsignedintegervalue-method"></a><span data-ttu-id="45756-103">IPortableDeviceValues：： SetSignedIntegerValue 方法</span><span class="sxs-lookup"><span data-stu-id="45756-103">IPortableDeviceValues::SetSignedIntegerValue method</span></span>

<span data-ttu-id="45756-104">**SetSignedIntegerValue** 方法會將新的 **LONG** 值新增 (type VT \_ I4) 或覆寫現有的值。</span><span class="sxs-lookup"><span data-stu-id="45756-104">The **SetSignedIntegerValue** method adds a new **LONG** value (type VT\_I4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="45756-105">語法</span><span class="sxs-lookup"><span data-stu-id="45756-105">Syntax</span></span>


```C++
HRESULT SetSignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONG           Value
);
```



## <a name="parameters"></a><span data-ttu-id="45756-106">參數</span><span class="sxs-lookup"><span data-stu-id="45756-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45756-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45756-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45756-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="45756-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="45756-109">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45756-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45756-110">指定新值的 **LONG** 。</span><span class="sxs-lookup"><span data-stu-id="45756-110">A **LONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45756-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="45756-111">Return value</span></span>

<span data-ttu-id="45756-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="45756-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="45756-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="45756-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="45756-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="45756-114">Return code</span></span>                                                                          | <span data-ttu-id="45756-115">Description</span><span class="sxs-lookup"><span data-stu-id="45756-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="45756-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="45756-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="45756-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="45756-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="45756-118">備註</span><span class="sxs-lookup"><span data-stu-id="45756-118">Remarks</span></span>

<span data-ttu-id="45756-119">如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="45756-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="45756-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="45756-120">Requirements</span></span>



| <span data-ttu-id="45756-121">需求</span><span class="sxs-lookup"><span data-stu-id="45756-121">Requirement</span></span> | <span data-ttu-id="45756-122">值</span><span class="sxs-lookup"><span data-stu-id="45756-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45756-123">標頭</span><span class="sxs-lookup"><span data-stu-id="45756-123">Header</span></span><br/>  | <dl> <span data-ttu-id="45756-124"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="45756-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="45756-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="45756-125">Library</span></span><br/> | <dl> <span data-ttu-id="45756-126"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="45756-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45756-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45756-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45756-128">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="45756-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="45756-129">**IPortableDeviceValues::GetSignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="45756-129">**IPortableDeviceValues::GetSignedIntegerValue**</span></span>](iportabledevicevalues-getsignedintegervalue.md)
</dt> </dl>

 

 




