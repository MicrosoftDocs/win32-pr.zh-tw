---
title: IDeliveryOptimizationFile2：： SetProperty 方法
description: 這個方法會傳回 DO 檔案的單一屬性。 |IDeliveryOptimizationFile2：： SetProperty 方法
keywords:
- SetProperty 方法
- SetProperty 方法，IDeliveryOptimizationFile2 介面
- IDeliveryOptimizationFile2 介面，SetProperty 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106986058"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a><span data-ttu-id="45fd9-107">IDeliveryOptimizationFile2：： SetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="45fd9-107">IDeliveryOptimizationFile2::SetProperty method</span></span>

<span data-ttu-id="45fd9-108">這個方法會傳回 DO 檔案的單一屬性。</span><span class="sxs-lookup"><span data-stu-id="45fd9-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="45fd9-109">語法</span><span class="sxs-lookup"><span data-stu-id="45fd9-109">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="45fd9-110">參數</span><span class="sxs-lookup"><span data-stu-id="45fd9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45fd9-111">*propId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45fd9-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45fd9-112">要設定 DOFilePropertyId 類型的必要屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="45fd9-112">The required property ID to set of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="45fd9-113">*propValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45fd9-113">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45fd9-114">要設定的屬性值，屬於 VARIANT 類型。</span><span class="sxs-lookup"><span data-stu-id="45fd9-114">The property value to set, of type VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45fd9-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="45fd9-115">Return value</span></span>

<span data-ttu-id="45fd9-116">這個方法會傳回下列 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="45fd9-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="45fd9-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="45fd9-117">Return code</span></span>                  | <span data-ttu-id="45fd9-118">Description</span><span class="sxs-lookup"><span data-stu-id="45fd9-118">Description</span></span>                                                        |
|------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="45fd9-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="45fd9-119">**S_OK**</span></span>                     | <span data-ttu-id="45fd9-120">Success</span><span class="sxs-lookup"><span data-stu-id="45fd9-120">Success</span></span>                                                            |
| <span data-ttu-id="45fd9-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="45fd9-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="45fd9-122">未知的屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="45fd9-122">Unknown property ID</span></span>                                                |
| <span data-ttu-id="45fd9-123">**DO_E_INVALID_STATE**</span><span class="sxs-lookup"><span data-stu-id="45fd9-123">**DO_E_INVALID_STATE**</span></span>       | <span data-ttu-id="45fd9-124">作業目前不在允許屬性設定的狀態</span><span class="sxs-lookup"><span data-stu-id="45fd9-124">The job is not currently in a state that allows a property setting</span></span> |

## <a name="requirements"></a><span data-ttu-id="45fd9-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="45fd9-125">Requirements</span></span>

| <span data-ttu-id="45fd9-126">需求</span><span class="sxs-lookup"><span data-stu-id="45fd9-126">Requirement</span></span> | <span data-ttu-id="45fd9-127">值</span><span class="sxs-lookup"><span data-stu-id="45fd9-127">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="45fd9-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45fd9-128">Minimum supported client</span></span>  | <span data-ttu-id="45fd9-129">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45fd9-129">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="45fd9-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45fd9-130">Minimum supported server</span></span>  | <span data-ttu-id="45fd9-131">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45fd9-131">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="45fd9-132">標頭</span><span class="sxs-lookup"><span data-stu-id="45fd9-132">Header</span></span>                    | <span data-ttu-id="45fd9-133">>deliveryoptimization。h</span><span class="sxs-lookup"><span data-stu-id="45fd9-133">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="45fd9-134">Idl</span><span class="sxs-lookup"><span data-stu-id="45fd9-134">IDL</span></span>                       | <span data-ttu-id="45fd9-135">>deliveryoptimization .idl</span><span class="sxs-lookup"><span data-stu-id="45fd9-135">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="45fd9-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="45fd9-136">Library</span></span>                   | <span data-ttu-id="45fd9-137">Dosvc .lib</span><span class="sxs-lookup"><span data-stu-id="45fd9-137">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="45fd9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="45fd9-138">DLL</span></span>                       | <span data-ttu-id="45fd9-139">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="45fd9-139">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="45fd9-140">IID</span><span class="sxs-lookup"><span data-stu-id="45fd9-140">IID</span></span>                       | <span data-ttu-id="45fd9-141">IID_IDeliveryOptimizationJob2 定義為18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="45fd9-141">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="45fd9-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45fd9-142">See also</span></span>

[<span data-ttu-id="45fd9-143">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="45fd9-143">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
