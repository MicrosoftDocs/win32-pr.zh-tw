---
description: SwitchTerminalToSubStream 方法會將終端機設定為參與者子流。
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'ITParticipantSubStreamControl：： SwitchTerminalToSubStream 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f211d4f3ff0f01801fb5497d36d81fa46e43397d8b69227180b022c9e74a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774648"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a>ITParticipantSubStreamControl：： SwitchTerminalToSubStream 方法

\[**SwitchTerminalToSubStream** 無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**SwitchTerminalToSubStream** 方法會將終端機設定為參與者子流。

## <a name="syntax"></a>語法


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pITTerminal* \[在\]
</dt> <dd>

[**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)介面的指標。

</dd> <dt>

*pITSubStream* \[在\]
</dt> <dd>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                     | 描述                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>            | 方法成功。<br/>                                                                       |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>    | 無法存取資料流程的參與者資訊。<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | *PParticipant* 或 *pITSubStream* 參數未指向有效的介面。<br/> |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | 子流未就緒。<br/>                                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | 記憶體不足，無法執行操作。<br/>                                    |



 

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
</dt> <dt>

[**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

