---
title: 'IBackgroundCopyJob GetNoProgressTimeout 方法 (>deliveryoptimization .h) '
description: 抓取在暫時性錯誤狀況發生之後，服務嘗試傳送檔案的時間長度。 如果有進度，則會重設計時器。
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- GetNoProgressTimeout 方法
- GetNoProgressTimeout 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetNoProgressTimeout 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a80e4d89c510885372a92d2c373d5fb73e9bd8375dd712ec07c5f98be51f791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755428"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a>IBackgroundCopyJob：： GetNoProgressTimeout 方法

抓取在暫時性錯誤狀況發生之後，服務嘗試傳送檔案的時間長度。 如果有進度，則會重設計時器。

## <a name="syntax"></a>語法


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRetryPeriod* \[在\]
</dt> <dd>

發生暫時性錯誤之後，服務嘗試傳送檔案的時間長度（以秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                              | 描述                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | 已成功取出超時時間。<br/> |



 

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

[**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





