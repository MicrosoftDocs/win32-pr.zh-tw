---
title: 'IBackgroundCopyCallback JobTransferred 方法 (>deliveryoptimization .h) '
description: 當作業中的所有檔案都已成功傳輸時，傳遞最佳化 () 會呼叫 JobTransferred 方法的執行。
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- JobTransferred 方法
- JobTransferred 方法，IBackgroundCopyCallback 介面
- IBackgroundCopyCallback 介面，JobTransferred 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69cf1a739e15bc7341769bdc01549ad439a1c93877f653f0689e686eb8bac1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047096"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a>IBackgroundCopyCallback：： JobTransferred 方法

當作業中的所有檔案都已成功傳輸時，傳遞最佳化 () 會呼叫 **JobTransferred** 方法的執行。

## <a name="syntax"></a>語法


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pJob* \[在\]
</dt> <dd>

包含作業的相關資訊，例如工作完成時間、傳輸的位元組數，以及傳輸的檔案數目。 請勿發行 *pJob*;當方法傳回時，請釋放介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法應該會傳回 S_OK。

## <a name="remarks"></a>備註

一般而言，您的執行應該呼叫 [**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md) 方法，以確認已成功傳輸檔案。 除非您呼叫 **Complete** 方法，否則不會在用戶端上提供下載檔案和回復檔案。

如果您未呼叫 [**Complete**](ibackgroundcopyjob-complete.md) 方法，或 [**IBackgroundCopyJob：： Cancel**](ibackgroundcopyjob-cancel.md) 方法在30天后取消作業，並刪除不完整的檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback 定義為97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**IBackgroundCopyJob：： Cancel**](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





