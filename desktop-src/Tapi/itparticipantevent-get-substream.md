---
description: 取得子串流會取得 \_ ITSubStream 介面陣列的指標，代表牽涉到事件的子串流。
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'ITParticipantEvent：： get_SubStream 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258f68815a5bc7cd201d94ab55199d59ebe6759eb2e279a1c80add91ea6c3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774658"
---
# <a name="itparticipanteventget_substream-method"></a>ITParticipantEvent：：取得子 \_ 流方法

\[**取得 \_** 在 Windows Vista、Windows Server 2008 及後續版本的作業系統中，無法使用子串流。 RTC 用戶端 API 提供類似的功能。\]

取得子串流會 **取得 \_** [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) 介面陣列的指標，代表牽涉到事件的子串流。

## <a name="syntax"></a>語法


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppSubStream* \[擴展\]
</dt> <dd>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)指標陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                           | 意義                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>            | 方法成功。<br/>                                    |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | 沒有與此事件相關聯的子串流。<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 指標**</dt> </dl>       | *PpSubStream* 參數不是有效的指標。<br/>  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

