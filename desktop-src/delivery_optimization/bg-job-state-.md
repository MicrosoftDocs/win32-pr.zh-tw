---
title: 'BG_JOB_STATE 列舉 (>deliveryoptimization .h) '
description: BG_JOB_STATE 列舉會針對作業的不同狀態定義常數值。
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- BG_JOB_STATE 列舉
- BG_JOB_STATE 列舉
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968741"
---
# <a name="bg_job_state-enumeration"></a>BG_JOB_STATE 列舉

**BG_JOB_STATE** 列舉會針對作業的不同狀態定義常數值。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**
</dt> <dd>

指定作業在佇列中並等候執行。 如果使用者在工作傳輸時登出，則作業會轉換成已排入佇列的狀態。

</dd> <dt>

<span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**
</dt> <dd>

不支援。

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**
</dt> <dd>

指定要傳送作業的資料。

</dd> <dt>

<span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**
</dt> <dd>

指定將工作暫停 (暫停) 。 若要暫停工作，請呼叫 [**IBackgroundCopyJob：：暫**](ibackgroundcopyjob-suspend.md) 止方法。 作業會保持暫止，直到您呼叫 [**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md)、 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md)或 [**IBackgroundCopyJob：： Cancel**](ibackgroundcopyjob-cancel.md) 方法。

</dd> <dt>

<span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**
</dt> <dd>

指定 (服務無法) 傳送檔案時，發生無法恢復的錯誤。 如果您可以更正錯誤，例如拒絕存取的錯誤，請在錯誤修正之後呼叫 [**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md) 方法。 但是，如果無法修正錯誤，請呼叫 [**IBackgroundCopyJob：： cancel**](ibackgroundcopyjob-cancel.md) 方法來取消作業，或呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法，以接受成功傳輸的下載作業部分。

</dd> <dt>

<span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**
</dt> <dd>

指定發生可復原的錯誤。 確實會根據內部重試設定重試暫時性錯誤狀態中的工作。 如果作業無法進行進度，作業的狀態會變更為 **BG_JOB_STATE_ERROR** (請參閱 [**IBackgroundCopyJob：： SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)) 。

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**
</dt> <dd>

指定已成功處理您的作業。 您必須呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法來確認作業已完成，並將檔案提供給用戶端。

</dd> <dt>

<span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**
</dt> <dd>

指定您呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法，以確認您的作業已順利完成。

</dd> <dt>

<span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**
</dt> <dd>

指定您呼叫 [**IBackgroundCopyJob：： cancel**](ibackgroundcopyjob-cancel.md) 方法來取消作業 (從傳送佇列) 移除作業。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob：： >getstate**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





