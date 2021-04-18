---
title: IDeliveryOptimizationJob2：： SetProperty 方法
description: 未使用這個方法。
keywords:
- SetProperty 方法
- SetProperty 方法，IDeliveryOptimizationJob2 介面
- IDeliveryOptimizationJob2 介面，SetProperty 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384777"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a><span data-ttu-id="8ec78-106">IDeliveryOptimizationJob2：： SetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="8ec78-106">IDeliveryOptimizationJob2::SetProperty method</span></span>

<span data-ttu-id="8ec78-107">未使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="8ec78-107">This method is unused.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec78-108">語法</span><span class="sxs-lookup"><span data-stu-id="8ec78-108">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="8ec78-109">參數</span><span class="sxs-lookup"><span data-stu-id="8ec78-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ec78-110">*propId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ec78-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ec78-111">未使用的。</span><span class="sxs-lookup"><span data-stu-id="8ec78-111">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="8ec78-112">*propValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ec78-112">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ec78-113">未使用的。</span><span class="sxs-lookup"><span data-stu-id="8ec78-113">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ec78-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ec78-114">Return value</span></span>

<span data-ttu-id="8ec78-115">如果 **DOJobPropertyId_ExtendedErrorInfo** propId，則傳回的值會 **DO_E_READ_ONLY_PROPERTY**，否則函數會傳回 **DO_E_UNKNOWN_PROPERTY_ID**。</span><span class="sxs-lookup"><span data-stu-id="8ec78-115">If propId is **DOJobPropertyId_ExtendedErrorInfo**, the returned value is **DO_E_READ_ONLY_PROPERTY**, otherwise the function returns **DO_E_UNKNOWN_PROPERTY_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec78-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ec78-116">Requirements</span></span>

| <span data-ttu-id="8ec78-117">需求</span><span class="sxs-lookup"><span data-stu-id="8ec78-117">Requirement</span></span> | <span data-ttu-id="8ec78-118">值</span><span class="sxs-lookup"><span data-stu-id="8ec78-118">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8ec78-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ec78-119">Minimum supported client</span></span>  | <span data-ttu-id="8ec78-120">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ec78-120">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="8ec78-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ec78-121">Minimum supported server</span></span>  | <span data-ttu-id="8ec78-122">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ec78-122">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="8ec78-123">標頭</span><span class="sxs-lookup"><span data-stu-id="8ec78-123">Header</span></span>                    | <span data-ttu-id="8ec78-124">>deliveryoptimization。h</span><span class="sxs-lookup"><span data-stu-id="8ec78-124">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="8ec78-125">Idl</span><span class="sxs-lookup"><span data-stu-id="8ec78-125">IDL</span></span>                       | <span data-ttu-id="8ec78-126">>deliveryoptimization .idl</span><span class="sxs-lookup"><span data-stu-id="8ec78-126">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="8ec78-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ec78-127">Library</span></span>                   | <span data-ttu-id="8ec78-128">Dosvc .lib</span><span class="sxs-lookup"><span data-stu-id="8ec78-128">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="8ec78-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8ec78-129">DLL</span></span>                       | <span data-ttu-id="8ec78-130">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="8ec78-130">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="8ec78-131">IID</span><span class="sxs-lookup"><span data-stu-id="8ec78-131">IID</span></span>                       | <span data-ttu-id="8ec78-132">IID_IDeliveryOptimizationJob2 定義為18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="8ec78-132">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="8ec78-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ec78-133">See also</span></span>

[<span data-ttu-id="8ec78-134">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="8ec78-134">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
