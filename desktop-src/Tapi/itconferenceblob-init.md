---
description: Init 方法會根據文字字串來初始化會議 blob。 如果 pBlob 為 Null，則會使用預設值。
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'ITConferenceBlob：： Init 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990223"
---
# <a name="itconferenceblobinit-method"></a>ITConferenceBlob：： Init 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Init** 方法會根據文字字串來初始化會議 blob。 如果 *pBlob* 為 **Null**，則會使用預設值。

## <a name="syntax"></a>語法


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

會議名稱之 **BSTR** 表示的指標。

</dd> <dt>

*CharacterSet* \[在\]
</dt> <dd>

[**BLOB \_字元集 \_ 的字元集**](blob-character-set.md) 描述元。

</dd> <dt>

*pBlob* \[在\]
</dt> <dd>

包含會議 blob 之 **BSTR** 的指標。 如果是 **Null**，則會使用預設值來初始化會議 blob。 目前，只有在 *CharacterSet* 參數設定為 [BCS ASCII] 時，才可以使用預設會議值 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PName*、 *CharacterSet* 或 *pBlob* 參數無效。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>            |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                              |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                             |



 

## <a name="remarks"></a>備註

如果 blob 已經初始化， **ITConferenceBlob：： Init** 將會傳回失敗。

應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 來配置 *pName* 和 *pBlob* 參數的記憶體。 當不再需要變數時，應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。

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

 

