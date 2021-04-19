---
title: 'IBackgroundCopyCallback JobModification 方法 (>deliveryoptimization .h) '
description: 傳遞最佳化 (在修改工作時，) 呼叫 JobModification 方法的執行。
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- JobModification 方法
- JobModification 方法，IBackgroundCopyCallback 介面
- IBackgroundCopyCallback 介面，JobModification 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968958"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a>IBackgroundCopyCallback：： JobModification 方法

傳遞最佳化 (在修改工作時，) 呼叫 [**JobModification**](https://www.bing.com/search?q=**JobModification**) 方法的執行。 當傳送位元組、將檔案新增至作業、屬性已修改，或作業狀態已變更時，服務就會產生此事件。

## <a name="syntax"></a>語法


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pJob* \[在\]
</dt> <dd>

包含存取作業之屬性、進度和狀態資訊的方法。 請勿發行 *pJob*;當 [**JobModification**](https://www.bing.com/search?q=**JobModification**) 方法傳回時，請釋放介面。

</dd> <dt>

*>dwreserved* \[在\]
</dt> <dd>

保留供未來使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法應該會傳回 S_OK。

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

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





