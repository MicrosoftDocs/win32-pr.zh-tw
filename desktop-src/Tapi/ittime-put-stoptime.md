---
description: Put \_ StopTime 方法會將 NTP (網路時間通訊協定) 結束時間值。 如果結束時間為零，則不會限制會話。
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: 'ITTime：:p ut_StopTime 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53446ea1d7ee93589987c42b005d7a84e7e728ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978660"
---
# <a name="ittimeput_stoptime-method"></a>ITTime：:p 的 \_ StopTime 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Put \_ StopTime** 方法會將 NTP (網路時間通訊協定) 結束時間值。 如果結束時間為零，則不會限制會話。

## <a name="syntax"></a>語法


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*時間* \[在\]
</dt> <dd>

會話的停止時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *Time* 參數無效。<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。 使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。

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

[**ITTime：： get \_ StopTime**](ittime-get-stoptime.md)
</dt> </dl>

 

 




