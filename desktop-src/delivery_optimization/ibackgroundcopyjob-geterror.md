---
title: 'IBackgroundCopyJob GetError 方法 (>deliveryoptimization .h) '
description: 在發生錯誤之後抓取錯誤介面。
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- GetError 方法
- GetError 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetError 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 016f11023d50d7ea1fa9024e270a7ebce0597e07d5c33a915facae47773759c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755508"
---
# <a name="ibackgroundcopyjobgeterror-method"></a>IBackgroundCopyJob：： GetError 方法

在發生錯誤之後抓取錯誤介面。

傳遞最佳化 (當工作的狀態為 BG_JOB_STATE_ERROR 或 BG_JOB_STATE_TRANSIENT_ERROR 時，) 會產生錯誤物件。 **IBackgroundCopyXXXX** 介面方法的呼叫失敗時，此服務不會建立錯誤物件。 在開始將資料傳輸 (工作的狀態變更為 BG_JOB_STATE_TRANSFERRING 的工作) 或應用程式結束之前，會提供錯誤物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppError* \[擴展\]
</dt> <dd>

提供錯誤代碼的錯誤介面、錯誤的描述，以及發生錯誤的內容。 此參數也會識別發生錯誤時所要傳送的檔案。 完成時釋放 *ppError* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                                                           | 描述                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>                              | 已成功產生 error 物件。<br/>                                                                                                                                                       |
| <dl> <dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt> </dl> | 只有在發生錯誤時，才可使用錯誤介面 (BG_JOB_STATE_ERROR 或 BG_JOB_STATE_TRANSIENT_ERROR) ，以及開始傳送資料 (BG_JOB_STATE_TRANSFERRING) 。<br/> |



 

## <a name="remarks"></a>備註

作業在發生嚴重錯誤時，會處於錯誤狀態。 您可以使用下列其中一個選項來判斷作業是否發生錯誤：

-   若要輪詢作業的狀態，請呼叫 [**IBackgroundCopyJob：： >getstate**](ibackgroundcopyjob-getstate.md) 方法。 如果狀態為 BG_JOB_STATE_ERROR，則作業會處於錯誤狀態。
-   若要在發生錯誤時收到通知，請將 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面明確地 (，) 的 [**JobError**](https://www.bing.com/search?q=**JobError**) 方法。 然後，呼叫 [**IBackgroundCopyJob：： SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) 方法來註冊回呼，並呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) 方法來設定 BG_NOTIFY_JOB_ERROR 旗標。

[**IBackgroundCopyError**](ibackgroundcopyerror.md)介面包含您用來判斷錯誤原因的資訊，以及傳輸程式是否可繼續。 判斷錯誤的原因之後，請執行下列其中一個選項：

-   若要取消作業，請呼叫 [**IBackgroundCopyJob：： cancel**](ibackgroundcopyjob-cancel.md) 方法。
-   若要在錯誤發生之前儲存成功傳輸的檔案，請呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法。
-   若要完成處理作業，請修正問題，然後呼叫 [**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md) 方法。

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

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob：： >getstate**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





