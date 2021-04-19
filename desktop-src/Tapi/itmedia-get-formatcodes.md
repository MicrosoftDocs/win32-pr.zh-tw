---
description: Get FormatCodes 方法會取得媒體裝載格式的程式 \_ 代碼清單。 Variant 會傳回 Bstr 的 SAFEARRAY。 該陣列中的每個 BSTR 都是格式的程式碼字串。
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'ITMedia：： get_FormatCodes 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985580"
---
# <a name="itmediaget_formatcodes-method"></a>ITMedia：： get \_ FormatCodes 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ FormatCodes** 方法會取得媒體裝載格式的程式代碼清單。 Variant 會傳回 **BSTR** 的 SAFEARRAY。 該陣列中的每個 **BSTR** 都是格式的程式碼字串。

## <a name="syntax"></a>語法


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[擴展\]
</dt> <dd>

媒體承載格式代碼的陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PVal* 參數不是有效的指標。<br/>         |
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

[**ITMedia：:p 的 \_ FormatCodes**](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




