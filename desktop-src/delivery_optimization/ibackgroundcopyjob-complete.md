---
title: 'IBackgroundCopyJob Complete 方法 (>deliveryoptimization. h) '
description: 結束作業，並將傳輸的檔案儲存在用戶端上。
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Complete 方法
- Complete 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，Complete 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103656"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>IBackgroundCopyJob：： Complete 方法

結束作業，並將傳輸的檔案儲存在用戶端上。

## <a name="syntax"></a>語法


```C++
HRESULT Complete();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值。 方法也可能會傳回與將已傳送檔案的暫存複本重新命名為其指定名稱相關的錯誤。



| 傳回碼                                                                                          | Description                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | 所有檔案都已成功傳輸。<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | 若為下載，無法 BG_JOB_STATE_CANCELLED 或 BG_JOB_STATE_ACKNOWLEDGED 工作的狀態。 <br/> 針對上傳，必須 BG_JOB_STATE_TRANSFERRED 工作的狀態。<br/> |



 

## <a name="remarks"></a>備註

如果工作的狀態為 **BG_JOB_STATE_TRANSFERRED**，則所有檔案都已成功傳輸。 若要檢查作業的狀態，請呼叫 [**IBackgroundCopyJob：： >getstate**](ibackgroundcopyjob-getstate.md) 方法。 當所有檔案都已傳送至用戶端時，您也可以執行 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面來接收通知。

確實會保留少於30天的工作。 將會移除所有較舊的作業。 不支援 [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) 群組原則。

針對下載作業，您可以在傳輸程式期間隨時呼叫 **Complete** 方法;不過，只有在呼叫這個方法之前成功傳送至用戶端的檔案才會儲存。 例如，如果您在處理五個檔案的第三個檔案時呼叫 **Complete** 方法，則只會儲存前兩個檔案。 若要判斷已傳送的檔案，請呼叫 [**IBackgroundCopyFile：： GetProgress**](ibackgroundcopyfile-getprogress-method.md)方法，並將 **BytesTransferred** 成員與 [**BG_FILE_PROGRESS**](bg-file-progress.md)結構的 **BytesTotal** 成員進行比較。

針對上傳作業，只有在作業的狀態為 **BG_JOB_STATE_TRANSFERRED** 時，您才能呼叫 **Complete** 方法。

檔案的擁有者是進行呼叫的使用者。 例如，如果系統管理員完成他人的工作，系統管理員不會擁有該檔案的擁有者。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
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

[**IBackgroundCopyJob：： >getstate**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





