---
title: 'IBackgroundCopyJob5 SetProperty 方法 (>deliveryoptimization .h) '
description: 設定傳遞最佳化 (的泛型方法會) 作業屬性。
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty 方法
- SetProperty 方法，IBackgroundCopyJob5 介面
- IBackgroundCopyJob5 介面，SetProperty 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686247"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a><span data-ttu-id="caacc-106">IBackgroundCopyJob5：： SetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="caacc-106">IBackgroundCopyJob5::SetProperty method</span></span>

<span data-ttu-id="caacc-107">設定傳遞最佳化 (的泛型方法會) 作業屬性。</span><span class="sxs-lookup"><span data-stu-id="caacc-107">A generic method for setting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="caacc-108">語法</span><span class="sxs-lookup"><span data-stu-id="caacc-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="caacc-109">參數</span><span class="sxs-lookup"><span data-stu-id="caacc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caacc-110">*PropertyId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caacc-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caacc-111">要設定為 [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) 列舉值之屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="caacc-111">The ID of the property that is being set specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="caacc-112">*PropertyValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="caacc-112">*PropertyValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caacc-113">正在設定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="caacc-113">The value of the property that is being set.</span></span> <span data-ttu-id="caacc-114">為了保留型別適合屬性的值，這個值是透過由所有已知屬性型別所組成的 [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) 聯集來指定。</span><span class="sxs-lookup"><span data-stu-id="caacc-114">In order to hold a value whose type is appropriate to the property, this value is specified via the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union that is composed of all the known property types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caacc-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="caacc-115">Return value</span></span>

<span data-ttu-id="caacc-116">方法會傳回下列傳回值。</span><span class="sxs-lookup"><span data-stu-id="caacc-116">The method returns the following return values.</span></span>



| <span data-ttu-id="caacc-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="caacc-117">Return code</span></span>                                                                          | <span data-ttu-id="caacc-118">Description</span><span class="sxs-lookup"><span data-stu-id="caacc-118">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="caacc-119"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="caacc-119"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="caacc-120">Success</span><span class="sxs-lookup"><span data-stu-id="caacc-120">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="caacc-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="caacc-121">Requirements</span></span>



| <span data-ttu-id="caacc-122">需求</span><span class="sxs-lookup"><span data-stu-id="caacc-122">Requirement</span></span> | <span data-ttu-id="caacc-123">值</span><span class="sxs-lookup"><span data-stu-id="caacc-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caacc-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="caacc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="caacc-125">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="caacc-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="caacc-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="caacc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="caacc-127">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="caacc-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="caacc-128">標頭</span><span class="sxs-lookup"><span data-stu-id="caacc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="caacc-129"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="caacc-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="caacc-130">Idl</span><span class="sxs-lookup"><span data-stu-id="caacc-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="caacc-131"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="caacc-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="caacc-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="caacc-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="caacc-133"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="caacc-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="caacc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="caacc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caacc-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caacc-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="caacc-136">IID</span><span class="sxs-lookup"><span data-stu-id="caacc-136">IID</span></span><br/>                      | <span data-ttu-id="caacc-137">IID_IBackgroundCopyJob5 定義為 E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="caacc-137">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="caacc-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="caacc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caacc-139">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="caacc-139">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="caacc-140">**IBackgroundCopyJob5：： GetProperty**</span><span class="sxs-lookup"><span data-stu-id="caacc-140">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





