---
title: 'IBackgroundCopyCallback JobError 方法 (>deliveryoptimization .h) '
description: 傳遞最佳化 (當工作的狀態變更為 BG_JOB_STATE_ERROR 時，) 會呼叫 JobError 方法的執行。
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- JobError 方法
- JobError 方法，IBackgroundCopyCallback 介面
- IBackgroundCopyCallback 介面，JobError 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384517"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>IBackgroundCopyCallback：： JobError 方法

傳遞最佳化 (當工作的狀態變更為 BG_JOB_STATE_ERROR 時，) 會呼叫 [**JobError**](https://www.bing.com/search?q=**JobError**) 方法的執行。

## <a name="syntax"></a>語法


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pJob* \[在\]
</dt> <dd>

包含作業相關的資訊，例如發生錯誤之前所傳輸的位元組數和檔案數目。 它也包含可繼續和取消作業的方法。 請勿發行 *pJob*;當 [**JobError**](https://www.bing.com/search?q=**JobError**) 方法傳回時，請釋放介面。

</dd> <dt>

*pError* \[在\]
</dt> <dd>

包含錯誤資訊，例如發生嚴重錯誤時所處理的檔案，以及錯誤的描述。 請勿發行 *pError*;當 [**JobError**](https://www.bing.com/search?q=**JobError**) 方法傳回時，請釋放介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法應該會傳回 **S_OK**;否則，請繼續呼叫這個方法，直到傳回 **S_OK** 為止。 基於效能的考慮，您應該將傳回不 **S_OK** 值的次數限制為幾次。 除了傳回錯誤碼之外，請考慮一律傳回 **S_OK** ，並在內部處理錯誤。 呼叫這個方法的間隔是任意的。

## <a name="remarks"></a>備註

判斷錯誤的原因之後，請執行下列其中一個選項：

-   若要取消作業，請呼叫 [**IBackgroundCopyJob：： cancel**](ibackgroundcopyjob-cancel.md) 方法。
-   若要在發生錯誤之前，接受成功傳輸的部分作業，請呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法。 此選項不適用於上傳作業;您無法完成上傳工作的一部分。
-   若要完成處理作業，請修正問題，然後呼叫 [**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md) 方法。

暫時性錯誤不會產生對 [**JobError**](https://www.bing.com/search?q=**JobError**) 方法的呼叫。

如果作業遇到 HTTP 403 錯誤，確實會傳回 BG_ERROR_CONTEXT_REMOTE_FILE，否則 BG_ERROR_CONTEXT_NONE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback 定義為97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob：： Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





