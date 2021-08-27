---
title: 'IBackgroundCopyJob Resume 方法 (>deliveryoptimization .h) '
description: 啟用新的作業，或重新開機已暫停的工作。
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Resume 方法
- Resume 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，Resume 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa4bd9a98626b7f26fc4ac9968d27d54604b5db56539eb383bb8aff696b2a561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543004"
---
# <a name="ibackgroundcopyjobresume-method"></a>IBackgroundCopyJob：： Resume 方法

啟用新的作業，或重新開機已暫停的工作。

## <a name="syntax"></a>語法


```C++
HRESULT Resume();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                                          | Description                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | 已成功重新開機作業。<br/>                                                           |
| <dl> <dt>**DO_E_EMPTY**</dt> </dl>          | 沒有要傳送的檔案。<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | 無法 BG_JOB_STATE_CANCELLED 或 BG_JOB_STATE_ACKNOWLEDGED 作業的狀態。<br/> |



 

## <a name="remarks"></a>備註

當您建立作業時，會一開始就暫停作業。 呼叫 **Resume** 會將作業移至傳輸狀態。 請注意，作業必須包含一或多個檔案，才能呼叫這個方法。

如果處於 BG_JOB_STATE_TRANSIENT_ERROR 或 BG_JOB_STATE_ERROR 狀態的作業，請在修正錯誤之後，呼叫 **Resume** 方法以重新開機作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob：： Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob：：暫止**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





