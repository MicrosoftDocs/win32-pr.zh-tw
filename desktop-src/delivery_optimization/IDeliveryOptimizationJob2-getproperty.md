---
title: IDeliveryOptimizationJob2：： GetProperty 方法
description: 傳回 DO 作業的單一屬性。
keywords:
- GetProperty 方法
- GetProperty 方法，IDeliveryOptimizationJob2 介面
- IDeliveryOptimizationJob2 介面，GetProperty 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464785"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a><span data-ttu-id="09347-106">IDeliveryOptimizationJob2：： GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="09347-106">IDeliveryOptimizationJob2::GetProperty method</span></span>

<span data-ttu-id="09347-107">這個方法會傳回 DO 作業的單一屬性。</span><span class="sxs-lookup"><span data-stu-id="09347-107">This method returns a single property of the DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="09347-108">語法</span><span class="sxs-lookup"><span data-stu-id="09347-108">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="09347-109">參數</span><span class="sxs-lookup"><span data-stu-id="09347-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09347-110">*propId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09347-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09347-111">要取得的必要屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="09347-111">The required property ID to get.</span></span> <span data-ttu-id="09347-112">只支援 VT_BSTR 類型的 **DOJobPropertyId_ExtendedErrorInfo** 。</span><span class="sxs-lookup"><span data-stu-id="09347-112">Only **DOJobPropertyId_ExtendedErrorInfo** of type VT_BSTR is supported.</span></span>

</dd> <dt>

<span data-ttu-id="09347-113">*propValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="09347-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09347-114">結果屬性值，儲存在 VARIANT 型別中。</span><span class="sxs-lookup"><span data-stu-id="09347-114">The resultant property value, stored in a VARIANT type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09347-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="09347-115">Return value</span></span>

<span data-ttu-id="09347-116">這個方法會傳回下列 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="09347-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="09347-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="09347-117">Return code</span></span>                  | <span data-ttu-id="09347-118">Description</span><span class="sxs-lookup"><span data-stu-id="09347-118">Description</span></span>          |
|------------------------------|----------------------|
| <span data-ttu-id="09347-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="09347-119">**S_OK**</span></span>                     | <span data-ttu-id="09347-120">Success</span><span class="sxs-lookup"><span data-stu-id="09347-120">Success</span></span>              |
| <span data-ttu-id="09347-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="09347-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="09347-122">未知的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="09347-122">Unknown property ID.</span></span> |

## <a name="requirements"></a><span data-ttu-id="09347-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="09347-123">Requirements</span></span>

| <span data-ttu-id="09347-124">需求</span><span class="sxs-lookup"><span data-stu-id="09347-124">Requirement</span></span> | <span data-ttu-id="09347-125">值</span><span class="sxs-lookup"><span data-stu-id="09347-125">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="09347-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09347-126">Minimum supported client</span></span>  | <span data-ttu-id="09347-127">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09347-127">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="09347-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09347-128">Minimum supported server</span></span>  | <span data-ttu-id="09347-129">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09347-129">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="09347-130">標頭</span><span class="sxs-lookup"><span data-stu-id="09347-130">Header</span></span>                    | <span data-ttu-id="09347-131">>deliveryoptimization。h</span><span class="sxs-lookup"><span data-stu-id="09347-131">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="09347-132">Idl</span><span class="sxs-lookup"><span data-stu-id="09347-132">IDL</span></span>                       | <span data-ttu-id="09347-133">>deliveryoptimization .idl</span><span class="sxs-lookup"><span data-stu-id="09347-133">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="09347-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="09347-134">Library</span></span>                   | <span data-ttu-id="09347-135">Dosvc .lib</span><span class="sxs-lookup"><span data-stu-id="09347-135">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="09347-136">DLL</span><span class="sxs-lookup"><span data-stu-id="09347-136">DLL</span></span>                       | <span data-ttu-id="09347-137">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="09347-137">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="09347-138">IID</span><span class="sxs-lookup"><span data-stu-id="09347-138">IID</span></span>                       | <span data-ttu-id="09347-139">IID_IDeliveryOptimizationJob2 定義為18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="09347-139">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="09347-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09347-140">See also</span></span>

[<span data-ttu-id="09347-141">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="09347-141">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
