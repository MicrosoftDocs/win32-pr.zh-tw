---
title: IDeliveryOptimizationFile2：： GetProperty 方法
description: 這個方法會傳回 DO 檔案的單一屬性。 |IDeliveryOptimizationFile2：： GetProperty 方法
keywords:
- GetProperty 方法
- GetProperty 方法，IDeliveryOptimizationFile2 介面
- IDeliveryOptimizationFile2 介面，GetProperty 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322467"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a><span data-ttu-id="c2846-107">IDeliveryOptimizationFile2：： GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="c2846-107">IDeliveryOptimizationFile2::GetProperty method</span></span>

<span data-ttu-id="c2846-108">這個方法會傳回 DO 檔案的單一屬性。</span><span class="sxs-lookup"><span data-stu-id="c2846-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2846-109">語法</span><span class="sxs-lookup"><span data-stu-id="c2846-109">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="c2846-110">參數</span><span class="sxs-lookup"><span data-stu-id="c2846-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2846-111">*propId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2846-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2846-112">要取得類型 DOFilePropertyId 的必要屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2846-112">The required property ID to get of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="c2846-113">*propValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c2846-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2846-114">儲存在變數中的屬性值。</span><span class="sxs-lookup"><span data-stu-id="c2846-114">The property value stored in a VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2846-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2846-115">Return value</span></span>

<span data-ttu-id="c2846-116">這個方法會傳回下列 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="c2846-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="c2846-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c2846-117">Return code</span></span>                  | <span data-ttu-id="c2846-118">Description</span><span class="sxs-lookup"><span data-stu-id="c2846-118">Description</span></span>                                         |
|------------------------------|-----------------------------------------------------|
| <span data-ttu-id="c2846-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="c2846-119">**S_OK**</span></span>                     | <span data-ttu-id="c2846-120">Success</span><span class="sxs-lookup"><span data-stu-id="c2846-120">Success</span></span>                                             |
| <span data-ttu-id="c2846-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="c2846-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="c2846-122">未知的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="c2846-122">Unknown property ID.</span></span>                                |
| <span data-ttu-id="c2846-123">**DO_E_WRITE_ONLY_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="c2846-123">**DO_E_WRITE_ONLY_PROPERTY**</span></span> | <span data-ttu-id="c2846-124">屬性為僅限寫入，無法讀取。</span><span class="sxs-lookup"><span data-stu-id="c2846-124">The property is Write only and cannot be read.</span></span>      |
| <span data-ttu-id="c2846-125">**E_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="c2846-125">**E_NOT_SET**</span></span>                | <span data-ttu-id="c2846-126">未透過 SetProperty 方法設定任何屬性。</span><span class="sxs-lookup"><span data-stu-id="c2846-126">No property was set through the SetProperty method.</span></span> |
| <span data-ttu-id="c2846-127">**E_OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="c2846-127">**E_OUTOFMEMORY**</span></span>            |  <span data-ttu-id="c2846-128">記憶體配置失敗</span><span class="sxs-lookup"><span data-stu-id="c2846-128">Memory allocation failure</span></span>                          |

## <a name="requirements"></a><span data-ttu-id="c2846-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2846-129">Requirements</span></span>

| <span data-ttu-id="c2846-130">需求</span><span class="sxs-lookup"><span data-stu-id="c2846-130">Requirement</span></span> | <span data-ttu-id="c2846-131">值</span><span class="sxs-lookup"><span data-stu-id="c2846-131">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c2846-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2846-132">Minimum supported client</span></span>  | <span data-ttu-id="c2846-133">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2846-133">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="c2846-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2846-134">Minimum supported server</span></span>  | <span data-ttu-id="c2846-135">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2846-135">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="c2846-136">標頭</span><span class="sxs-lookup"><span data-stu-id="c2846-136">Header</span></span>                    | <span data-ttu-id="c2846-137">>deliveryoptimization。h</span><span class="sxs-lookup"><span data-stu-id="c2846-137">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="c2846-138">Idl</span><span class="sxs-lookup"><span data-stu-id="c2846-138">IDL</span></span>                       | <span data-ttu-id="c2846-139">>deliveryoptimization .idl</span><span class="sxs-lookup"><span data-stu-id="c2846-139">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="c2846-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2846-140">Library</span></span>                   | <span data-ttu-id="c2846-141">Dosvc .lib</span><span class="sxs-lookup"><span data-stu-id="c2846-141">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="c2846-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c2846-142">DLL</span></span>                       | <span data-ttu-id="c2846-143">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="c2846-143">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="c2846-144">IID</span><span class="sxs-lookup"><span data-stu-id="c2846-144">IID</span></span>                       | <span data-ttu-id="c2846-145">IID_IDeliveryOptimizationJob2 定義為18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="c2846-145">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="c2846-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2846-146">See also</span></span>

[<span data-ttu-id="c2846-147">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="c2846-147">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
