---
description: SetBoolValue 方法會將新的布林值新增 (型別 VT \_ BOOL) 或覆寫現有的布林值。
ms.assetid: add30665-78f7-4037-801e-af51a4ab2f60
title: 'IPortableDeviceValues：： SetBoolValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7adf311e863c08873aa8300f9e940d4a5b49417f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993261"
---
# <a name="iportabledevicevaluessetboolvalue-method"></a><span data-ttu-id="c9227-103">IPortableDeviceValues：： SetBoolValue 方法</span><span class="sxs-lookup"><span data-stu-id="c9227-103">IPortableDeviceValues::SetBoolValue method</span></span>

<span data-ttu-id="c9227-104">**SetBoolValue** 方法會將新的 **布林** 值新增 (型別 VT \_ BOOL) 或覆寫現有的布林值。</span><span class="sxs-lookup"><span data-stu-id="c9227-104">The **SetBoolValue** method adds a new **Boolean** value (type VT\_BOOL) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9227-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9227-105">Syntax</span></span>


```C++
HRESULT SetBoolValue(
  [in]       REFPROPERTYKEY key,
  [in] const BOOL           Value
);
```



## <a name="parameters"></a><span data-ttu-id="c9227-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9227-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9227-107">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9227-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9227-108">指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。</span><span class="sxs-lookup"><span data-stu-id="c9227-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="c9227-109">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9227-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9227-110">指定新值的 **布林** 值。</span><span class="sxs-lookup"><span data-stu-id="c9227-110">A **BOOL** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9227-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9227-111">Return value</span></span>

<span data-ttu-id="c9227-112">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="c9227-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c9227-113">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="c9227-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c9227-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c9227-114">Return code</span></span>                                                                          | <span data-ttu-id="c9227-115">Description</span><span class="sxs-lookup"><span data-stu-id="c9227-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c9227-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c9227-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c9227-117">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="c9227-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c9227-118">備註</span><span class="sxs-lookup"><span data-stu-id="c9227-118">Remarks</span></span>

<span data-ttu-id="c9227-119">如果現有的值具有 *金鑰* 參數指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。</span><span class="sxs-lookup"><span data-stu-id="c9227-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="c9227-120">會適當地釋放現有的金鑰記憶體。</span><span class="sxs-lookup"><span data-stu-id="c9227-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9227-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9227-121">Requirements</span></span>



| <span data-ttu-id="c9227-122">需求</span><span class="sxs-lookup"><span data-stu-id="c9227-122">Requirement</span></span> | <span data-ttu-id="c9227-123">值</span><span class="sxs-lookup"><span data-stu-id="c9227-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9227-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c9227-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c9227-125"><dt>PortableDeviceTypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9227-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9227-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9227-126">Library</span></span><br/> | <dl> <span data-ttu-id="c9227-127"><dt>PortableDeviceGUIDs .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9227-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9227-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9227-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9227-129">**IPortableDeviceValues 介面**</span><span class="sxs-lookup"><span data-stu-id="c9227-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c9227-130">**IPortableDeviceValues::GetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="c9227-130">**IPortableDeviceValues::GetBoolValue**</span></span>](iportabledevicevalues-getboolvalue.md)
</dt> </dl>

 

 




