---
title: 'IBackgroundCopyJob SetNoProgressTimeout 方法 (>deliveryoptimization .h) '
description: 設定在發生暫時性錯誤狀況時，) 嘗試傳送檔案的時間長度傳遞最佳化 (。 如果有進度，則會重設計時器。
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- SetNoProgressTimeout 方法
- SetNoProgressTimeout 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，SetNoProgressTimeout 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcf6905388d54103aaac34ae934c89e2fd8ccc16ce32a384eb730376606351b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542925"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a>IBackgroundCopyJob：： SetNoProgressTimeout 方法

設定在發生暫時性錯誤狀況時，) 嘗試傳送檔案的時間長度傳遞最佳化 (。 如果有進度，則會重設計時器。

## <a name="syntax"></a>語法


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RetryPeriod* \[在\]
</dt> <dd>

未進行任何進度之後，嘗試傳輸檔案的時間長度（以秒為單位）。 高優先順序作業的預設重試期間為3600秒 (1 小時) ，而低優先順序作業為86400秒 (24 小時) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                                          | 描述                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | 已成功設定重試期限。<br/>                                                            |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | 無法 BG_JOB_STATE_CANCELLED 或 BG_JOB_STATE_ACKNOWLEDGED 作業的狀態。<br/> |



 

## <a name="remarks"></a>備註

如果在重試期間未進行任何進度，則會將工作的狀態從 BG_JOB_STATE_TRANSIENT_ERROR 移至 BG_JOB_STATE_ERROR。 如果您要求錯誤通知，則會呼叫您的 [**JobError**](https://www.bing.com/search?q=**JobError**) 回呼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





