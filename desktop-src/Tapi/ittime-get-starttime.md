---
description: 取得 \_ StartTime 方法會取得32位 NTP (網路時間通訊協定) 開始時間值。 會話會在這段時間被視為有效。
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: 'ITTime：： get_StartTime 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2fcc7aedf94d65f828714a7ebe5e6bbbfd760514654b2b634b479f2fd4802b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060756"
---
# <a name="ittimeget_starttime-method"></a>ITTime：： get \_ StartTime 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**取得 \_ StartTime** 方法會取得32位 NTP (網路時間通訊協定) 開始時間值。 會話會在這段時間被視為有效。

## <a name="syntax"></a>語法


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTime* \[擴展\]
</dt> <dd>

會話開始時間的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PTime* 參數不是有效的指標。<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime：:p 的時間 \_ StartTime StartTime**](ittime-put-starttime.md)
</dt> </dl>

 

 




