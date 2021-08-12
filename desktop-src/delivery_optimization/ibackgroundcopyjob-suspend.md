---
title: 'IBackgroundCopyJob 暫止方法 (>deliveryoptimization) '
description: 暫停作業。 新的工作、發生錯誤的作業，以及已完成傳輸檔案的作業會自動暫停。
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Suspend 方法
- 暫止方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，暫止方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9458347c8f09a2f04c4e2800a0f2f747571f5519b322133ef4b874b15cf77a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542807"
---
# <a name="ibackgroundcopyjobsuspend-method"></a>IBackgroundCopyJob：：暫止方法

暫停作業。 新的工作、發生錯誤的作業，以及已完成傳輸檔案的作業會自動暫停。

## <a name="syntax"></a>語法


```C++
HRESULT Suspend();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                                          | 描述                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | 已成功暫止作業。<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | 無法 BG_JOB_STATE_CANCELLED 或 BG_JOB_STATE_ACKNOWLEDGED 作業的狀態。<br/> |



 

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

[**IBackgroundCopyJob：： Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





