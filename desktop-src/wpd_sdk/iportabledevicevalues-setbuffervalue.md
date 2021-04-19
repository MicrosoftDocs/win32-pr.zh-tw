---
description: SetBufferValue 方法會將新的位元組 \* 值新增 (類型 VT \_ 向量 \| VT \_ UI1) 或覆寫現有的位元組值。
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: 'IPortableDeviceValues：： SetBufferValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e04b41fdd397d8d03e7e0576d2ba8fb3b6ad1401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995000"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a><span data-ttu-id="cb7eb-103">IPortableDeviceValues：： SetBufferValue 方法</span><span class="sxs-lookup"><span data-stu-id="cb7eb-103">IPortableDeviceValues::SetBufferValue method</span></span>

<span data-ttu-id="cb7eb-104">**SetBufferValue** 方法會將新的 **位元組** \* 值新增 (類型 VT \_ 向量 \| VT \_ UI1) 或覆寫現有的位元組值。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-104">The **SetBufferValue** method adds a new **BYTE**\* value (type VT\_VECTOR \| VT\_UI1) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb7eb-105">語法</span><span class="sxs-lookup"><span data-stu-id="cb7eb-105">Syntax</span></span>


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
);
```



## <a name="parameters"></a><span data-ttu-id="cb7eb-106">參數</span><span class="sxs-lookup"><span data-stu-id="cb7eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb7eb-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb7eb-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb7eb-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="cb7eb-109">*pValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb7eb-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb7eb-110">**位元組 \*** ，其中包含要寫入至專案的資料。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-110">A **BYTE\*** that contains the data to write to the item.</span></span> <span data-ttu-id="cb7eb-111">提交的緩衝區資料會複製到介面，因此呼叫者可以在進行此呼叫之後釋放此緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-111">The submitted buffer data is copied to the interface, so the caller can free this buffer after making this call.</span></span>

</dd> <dt>

<span data-ttu-id="cb7eb-112">*cbValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cb7eb-112">*cbValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb7eb-113">*PValue* 所指向的值大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-113">The size of the value pointed to by *pValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb7eb-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb7eb-114">Return value</span></span>

<span data-ttu-id="cb7eb-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cb7eb-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cb7eb-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cb7eb-117">Return code</span></span>                                                                          | <span data-ttu-id="cb7eb-118">Description</span><span class="sxs-lookup"><span data-stu-id="cb7eb-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cb7eb-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cb7eb-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cb7eb-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb7eb-121">備註</span><span class="sxs-lookup"><span data-stu-id="cb7eb-121">Remarks</span></span>

<span data-ttu-id="cb7eb-122">如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-122">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="cb7eb-123">會適當地釋放現有的金鑰記憶體。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-123">The existing key memory is released appropriately.</span></span>

<span data-ttu-id="cb7eb-124">不支援設定 **Null** 或零大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cb7eb-124">Setting a **NULL** or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb7eb-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb7eb-125">Requirements</span></span>



| <span data-ttu-id="cb7eb-126">需求</span><span class="sxs-lookup"><span data-stu-id="cb7eb-126">Requirement</span></span> | <span data-ttu-id="cb7eb-127">值</span><span class="sxs-lookup"><span data-stu-id="cb7eb-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb7eb-128">標頭</span><span class="sxs-lookup"><span data-stu-id="cb7eb-128">Header</span></span><br/>  | <dl> <span data-ttu-id="cb7eb-129"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="cb7eb-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb7eb-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="cb7eb-130">Library</span></span><br/> | <dl> <span data-ttu-id="cb7eb-131"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb7eb-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb7eb-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb7eb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb7eb-133">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="cb7eb-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="cb7eb-134">**IPortableDeviceValues::GetBufferValue**</span><span class="sxs-lookup"><span data-stu-id="cb7eb-134">**IPortableDeviceValues::GetBufferValue**</span></span>](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




