---
description: Get \_ CharacterSet 方法會取得 \_ \_ 目前會議 blob 中所使用之字元集的 BLOB 字元集描述元。
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'ITConferenceBlob：： get_CharacterSet 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20a9dd719d2ae9742a6ec4b3295e3e22ffe871b4a38c55d07e07a3421271553d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060996"
---
# <a name="itconferenceblobget_characterset-method"></a>ITConferenceBlob：： get \_ CharacterSet 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ CharacterSet** 方法會取得目前會議 blob 中所使用之字元集的 [**BLOB \_ 字元集 \_**](blob-character-set.md)描述元。

## <a name="syntax"></a>語法


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCharacterSet* \[擴展\]
</dt> <dd>

字元集的 [**BLOB \_ 字元集 \_**](blob-character-set.md) 描述元指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                                   | 描述                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                          | 方法成功。<br/>                                     |
| <dl> <dt>**E \_ 指標**</dt> </dl>                     | *PCharacterSet* 參數不是有效的指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                 | 記憶體不足，無法執行操作。<br/>  |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                        | 未指定的錯誤。<br/>                                    |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>                     | 尚未實作這個方法。<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                  | *pCharacterSet* 為 **Null**。<br/>                          |
| <dl> <dt>**(HRESULT) 錯誤 \_ 的 \_ 資料無效**</dt> </dl> | 目前的字元集無效或無法使用。<br/>  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**BLOB \_ 字元集 \_**](blob-character-set.md)
</dt> </dl>

 

 




