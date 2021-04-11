---
title: 'ADSI 列印工作狀態常數 (Adssts .h) '
description: 下列常數是與 IADsPrintJobOperations. Status 屬性搭配使用，以指出列印工作的狀態。
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934822"
---
# <a name="adsi-print-job-status-constants"></a>ADSI 列印工作狀態常數

下列常數是與 [**IADsPrintJobOperations. Status**](iadsprintjoboperations-property-methods.md) 屬性搭配使用，以指出列印工作的狀態。

<dl> <dt>

<span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**ADS \_ 作業已 \_ 暫停**
</dt> <dd> <dl> <dt>

1 (0x1) 
</dt> <dt>



列印工作已暫停。


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ADS \_ 作業 \_ 錯誤**
</dt> <dd> <dl> <dt>

2 (0x2) 
</dt> <dt>



發生錯誤。


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**廣告 \_ 作業 \_ 刪除**
</dt> <dd> <dl> <dt>

4 (0x4) 
</dt> <dt>



正在刪除列印工作。


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**ADS \_ 作業 \_ 幕後處理**
</dt> <dd> <dl> <dt>

8 (0x8) 
</dt> <dt>



列印工作正在進行多工緩衝處理。


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**ADS \_ 工作 \_ 列印**
</dt> <dd> <dl> <dt>

16 (0x10) 
</dt> <dt>



列印工作正在列印中。


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**ADS \_ 工作 \_ 離線**
</dt> <dd> <dl> <dt>

32 (0x20) 
</dt> <dt>



印表機為離線。


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**ADS \_ 作業 \_ PAPEROUT**
</dt> <dd> <dl> <dt>

64 (0x40) 
</dt> <dt>



印表機紙張用完。


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**廣告 \_ 作業 \_ 列印**
</dt> <dd> <dl> <dt>

128 (0x80) 
</dt> <dt>



列印工作已列印。


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**\_ \_ 已刪除 ADS 作業**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



已刪除列印工作。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Adssts。h</dt> </dl> |



 

 





