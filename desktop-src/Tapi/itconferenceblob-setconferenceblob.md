---
description: SetConferenceBlob 方法會認可會議 blob 的變更。 若要第一次初始化會議 blob，請改用 Init 方法。
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'ITConferenceBlob：： SetConferenceBlob 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 391a20ade99d3e35da9d4f76eaab13b6ba65b07b5693321c6c3b2bb63f53c2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865422"
---
# <a name="itconferenceblobsetconferenceblob-method"></a>ITConferenceBlob：： SetConferenceBlob 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**SetConferenceBlob** 方法會認可會議 blob 的變更。 若要第一次初始化會議 blob，請改用 [**Init**](itconferenceblob-init.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*CharacterSet* \[在\]
</dt> <dd>

[**BLOB \_會議 \_**](blob-character-set.md) blob 字元集的字元集描述項。

</dd> <dt>

*pBlob* \[在\]
</dt> <dd>

包含會議 blob 之 **BSTR** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *CharacterSet* 或 *pBlob* 參數無效。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>  |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                    |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                   |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pBlob* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。

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

 

