---
description: Get \_ SubStreamFromParticipant 方法可讓應用程式探索哪些子串流與指定的參與者相關聯。
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'ITParticipantSubStreamControl：： get_SubStreamFromParticipant 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae40487bbef7e678722a2710d99bce9ed1ebe2f5192705f0a7dc03f86e10e421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621528"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a>ITParticipantSubStreamControl：： get \_ SubStreamFromParticipant 方法

\[**取得 \_SubStreamFromParticipant** 無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ SubStreamFromParticipant** 方法可讓應用程式探索哪些子串流與指定的參與者相關聯。

## <a name="syntax"></a>語法


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pParticipant* \[在\]
</dt> <dd>

[**ITParticipant**](itparticipant.md)介面的指標。

</dd> <dt>

*ppITSubStream* \[擴展\]
</dt> <dd>

[**ITParticipant**](itparticipant.md)介面指標的陣列指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                                 |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PpITSubStream* 參數不是有效的指標。<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PParticipant* 參數未指向有效的介面。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>  | 無法存取資料流程的參與者資訊。<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipantSubStreamControl**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

