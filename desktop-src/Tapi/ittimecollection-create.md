---
description: Create 方法會建立新的 ITTime 元件。
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: 'ITTimeCollection：： Create 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a65949d0584f6ed41d3e1611c790b6b94dfa88a4e11ba18818974af5d38cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762370"
---
# <a name="ittimecollectioncreate-method"></a>ITTimeCollection：： Create 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Create** 方法會建立新的 [**ITTime**](ittime.md)元件。

## <a name="syntax"></a>語法


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要建立之專案的索引。  (索引陣列是以一為基礎的 ) 。

</dd> <dt>

*ppTime* \[擴展\]
</dt> <dd>

所建立 b 元件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PpTime* 參數不是有效的指標。<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *索引* 參數無效。<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

TAPI 會在 **ITTimeCollection：： Create** 所傳回的 [**ITTime**](ittime.md)介面上呼叫 **AddRef** 方法。 應用程式必須在 v 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

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

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 




