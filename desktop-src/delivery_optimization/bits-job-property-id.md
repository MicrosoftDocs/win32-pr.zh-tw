---
title: 'BITS_JOB_PROPERTY_ID 列舉 (>deliveryoptimization .h) '
description: BITS_JOB_PROPERTY_ID 列舉會指定 DO 作業的屬性識別碼。 此列舉會在 BITS_JOB_PROPERTY_VALUE 聯集內使用，以決定包含在聯集內的數值型別。
ms.assetid: B0F3C6C2-474F-4FD8-990A-770FAA993550
keywords:
- BITS_JOB_PROPERTY_ID 列舉
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1d00d4dc12b27c1c80b0e18bb095641a56e322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685612"
---
# <a name="bits_job_property_id-enumeration"></a><span data-ttu-id="d4ea0-105">BITS_JOB_PROPERTY_ID 列舉</span><span class="sxs-lookup"><span data-stu-id="d4ea0-105">BITS_JOB_PROPERTY_ID enumeration</span></span>

<span data-ttu-id="d4ea0-106">**BITS_JOB_PROPERTY_ID** 列舉會指定 DO 作業的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-106">The **BITS_JOB_PROPERTY_ID** enumeration specifies the ID of the property for the DO job.</span></span> <span data-ttu-id="d4ea0-107">此列舉會在 [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) 聯集內使用，以決定包含在聯集內的數值型別。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-107">This enumeration is used in the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union to determine the type of value contained in the union.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ea0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4ea0-108">Syntax</span></span>


```C++
typedef enum  { 
  BITS_JOB_PROPERTY_ID_COST_FLAGS                     = 1,
  BITS_JOB_PROPERTY_NOTIFICATION_CLSID                = 2,
  BITS_JOB_PROPERTY_DYNAMIC_CONTENT                   = 3,
  BITS_JOB_PROPERTY_HIGH_PERFORMANCE                  = 4,
  BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE                 = 5,
  BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS            = 7,
  BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS  = 9,
  BITS_JOB_PROPERTY_ON_DEMAND_MODE                    = 10
} BITS_JOB_PROPERTY_ID;
```



## <a name="constants"></a><span data-ttu-id="d4ea0-109">常數</span><span class="sxs-lookup"><span data-stu-id="d4ea0-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d4ea0-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="d4ea0-111">用來控制透過行動電話和/或類似網路之 [傳輸行為](https://www.bing.com/search?q=control+transfer+behavior) 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-111">The ID that is used to [control transfer behavior](https://www.bing.com/search?q=control+transfer+behavior) over cellular and/or similar networks.</span></span> <span data-ttu-id="d4ea0-112">當傳輸進行中時，可能會變更這個屬性，新的成本旗標會立即生效。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-112">This property may be changed while a transfer is ongoing   the new cost flags will take effect immediately.</span></span>

<span data-ttu-id="d4ea0-113">這個屬性會使用 **BITS_JOB_PROPERTY_VALUE** s **Dword** 欄位。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-113">This property uses the **BITS_JOB_PROPERTY_VALUE** s **Dword** field.</span></span>

</dd> <dt>

<span data-ttu-id="d4ea0-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="d4ea0-115">用來依照 CLSID [註冊 COM 回呼](https://www.bing.com/search?q=register+a+COM+callback) 的識別碼，以接收有關進度和完成作業的通知。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-115">The ID that is used to [register a COM callback](https://www.bing.com/search?q=register+a+COM+callback) by CLSID to receive notifications about the progress and completion of a DO job.</span></span> <span data-ttu-id="d4ea0-116">CLSID 必須參考與已註冊的跨進程 COM 伺服器相關聯的類別。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-116">The CLSID must refer to a class associated with a registered out-of-process COM server.</span></span> <span data-ttu-id="d4ea0-117">您也可以將它設定為 **GUID_Null** ，以清除先前設定的通知 CLSID。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-117">It may also be set to **GUID_NULL** to clear a previously set notification CLSID.</span></span>

<span data-ttu-id="d4ea0-118">這個屬性會使用 **BITS_JOB_PROPERTY_VALUE** 的 **CLsID** 欄位。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-118">This property uses the **BITS_JOB_PROPERTY_VALUE** s **CLsID** field.</span></span>

</dd> <dt>

<span data-ttu-id="d4ea0-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="d4ea0-120">不支援。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-120">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d4ea0-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span></span>
</dt> <dd>

<span data-ttu-id="d4ea0-122">不支援。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d4ea0-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="d4ea0-124">不支援。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-124">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d4ea0-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="d4ea0-126">不支援。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-126">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d4ea0-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span></span>
</dt> <dd>

<span data-ttu-id="d4ea0-128">不支援。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-128">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d4ea0-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="d4ea0-130">不支援。</span><span class="sxs-lookup"><span data-stu-id="d4ea0-130">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4ea0-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4ea0-131">Requirements</span></span>



| <span data-ttu-id="d4ea0-132">需求</span><span class="sxs-lookup"><span data-stu-id="d4ea0-132">Requirement</span></span> | <span data-ttu-id="d4ea0-133">值</span><span class="sxs-lookup"><span data-stu-id="d4ea0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ea0-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4ea0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ea0-135">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4ea0-135">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d4ea0-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4ea0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ea0-137">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4ea0-137">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d4ea0-138">標頭</span><span class="sxs-lookup"><span data-stu-id="d4ea0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4ea0-139"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ea0-139"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ea0-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4ea0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ea0-141">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-141">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="d4ea0-142">**BITS_JOB_PROPERTY_VALUE**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-142">**BITS_JOB_PROPERTY_VALUE**</span></span>](bits-job-property-value-.md)
</dt> <dt>

[<span data-ttu-id="d4ea0-143">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-143">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> <dt>

[<span data-ttu-id="d4ea0-144">**IBackgroundCopyJob5：： SetProperty**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-144">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[<span data-ttu-id="d4ea0-145">**IBackgroundCopyJob5：： GetProperty**</span><span class="sxs-lookup"><span data-stu-id="d4ea0-145">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





