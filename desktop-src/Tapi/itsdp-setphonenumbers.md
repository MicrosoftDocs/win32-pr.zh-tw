---
description: SetPhoneNumbers 方法會設定與會議 blob 相關聯的電話號碼陣列。
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'ITSdp：： SetPhoneNumbers 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733dfbe4752281abf4063f308a05aec73203d361e3c9c5dcebf413eb4ba2af72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140211"
---
# <a name="itsdpsetphonenumbers-method"></a>ITSdp：： SetPhoneNumbers 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**SetPhoneNumbers** 方法會設定與會議 blob 相關聯的電話號碼陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*數位* \[在\]
</dt> <dd>

列出電話號碼之 **BSTR** 的 SAFEARRAY。

</dd> <dt>

*名稱* \[在\]
</dt> <dd>

**BSTR** 清單名稱的 SAFEARRAY。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *數位* 或 *名稱* 參數無效。<br/>     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

清單中的 *數位* 和 *名稱* 會指向相同的長度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




