---
description: ITParticipantSubStreamControl 介面是由 IPConf MSP 所執行。
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: 'ITParticipantSubStreamControl 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e910022d45ca9f9516adbe8aeebbdb172d66f28ab1bf8cb23219c2eee80f56cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774598"
---
# <a name="itparticipantsubstreamcontrol-interface"></a>ITParticipantSubStreamControl 介面

\[**ITParticipantSubStreamControl** 無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**ITParticipantSubStreamControl** 介面是由 IPConf MSP 所執行。 此介面會在呼叫物件上公開。 這個介面會提供方法，讓應用程式能夠探索或控制與參與者的子串流相符。 **ITParticipantSubStreamControl** 介面是藉由在 [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)上呼叫 **QueryInterface** 來建立。

## <a name="members"></a>成員

**ITParticipantSubStreamControl** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITParticipantSubStreamControl** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITParticipantSubStreamControl** 介面具有這些方法。



| 方法                                                                                              | 描述                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**取得 \_ ParticipantFromSubStream**](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | 取得與指定子流相關聯的參與者。<br/> |
| [**取得 \_ SubStreamFromParticipant**](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | 取得與指定參與者相關聯的子串流。<br/> |
| [**SwitchTerminalToSubStream**](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | 設定子流上的參與者。<br/>                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

