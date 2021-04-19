---
description: Put \_ FormatCodes 方法會設定媒體裝載格式的程式代碼清單。 Variant 包含 Bstr 的 SAFEARRAY。 該陣列中的每個 BSTR 都是格式的程式碼字串。
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: 'ITMedia：:p ut_FormatCodes 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988235"
---
# <a name="itmediaput_formatcodes-method"></a>ITMedia：:p 的 \_ FormatCodes 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Put \_ FormatCodes** 方法會設定媒體裝載格式的程式代碼清單。 變數包含 **BSTR** s 的 SAFEARRAY。 該陣列中的每個 **BSTR** 都是格式的程式碼字串。

## <a name="syntax"></a>語法


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewVal* \[在\]
</dt> <dd>

媒體承載格式代碼的清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *NewVal* 參數無效。<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

當提供承載格式的清單時，這表示這些格式可能會在會話中使用，但這些格式的第一種是會話的預設格式。 當傳輸通訊協定為 RTP 時，格式代碼為 RTP 承載類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia：： get \_ FormatCodes**](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




