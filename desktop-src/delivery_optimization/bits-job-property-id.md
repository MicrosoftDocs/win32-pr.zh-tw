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
ms.openlocfilehash: 803e776bd635cd600bf664354dda8703d224dffcd63ea751919875a6ea69233d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047146"
---
# <a name="bits_job_property_id-enumeration"></a>BITS_JOB_PROPERTY_ID 列舉

**BITS_JOB_PROPERTY_ID** 列舉會指定 DO 作業的屬性識別碼。 此列舉會在 [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) 聯集內使用，以決定包含在聯集內的數值型別。

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>常數

<dl> <dt>

<span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**
</dt> <dd>

用來控制透過行動電話和/或類似網路之 [傳輸行為](https://www.bing.com/search?q=control+transfer+behavior) 的識別碼。 當傳輸進行中時，可能會變更這個屬性，新的成本旗標會立即生效。

這個屬性會使用 **BITS_JOB_PROPERTY_VALUE** s **Dword** 欄位。

</dd> <dt>

<span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**
</dt> <dd>

用來依照 CLSID [註冊 COM 回呼](https://www.bing.com/search?q=register+a+COM+callback) 的識別碼，以接收有關進度和完成作業的通知。 CLSID 必須參考與已註冊的跨進程 COM 伺服器相關聯的類別。 您也可以將它設定為 **GUID_Null** ，以清除先前設定的通知 CLSID。

這個屬性會使用 **BITS_JOB_PROPERTY_VALUE** 的 **CLsID** 欄位。

</dd> <dt>

<span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**
</dt> <dd>

不支援。

</dd> <dt>

<span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**
</dt> <dd>

不支援。

</dd> <dt>

<span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**
</dt> <dd>

不支援。

</dd> <dt>

<span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**
</dt> <dd>

不支援。

</dd> <dt>

<span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**
</dt> <dd>

不支援。

</dd> <dt>

<span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**
</dt> <dd>

不支援。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> <dt>

[**IBackgroundCopyJob5：： SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[**IBackgroundCopyJob5：： GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





