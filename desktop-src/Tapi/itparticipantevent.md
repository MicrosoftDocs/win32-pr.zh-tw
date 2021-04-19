---
description: ITParticipantEvent 介面包含可取得參與者事件描述的方法。
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: 'ITParticipantEvent 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000828"
---
# <a name="itparticipantevent-interface"></a>ITParticipantEvent 介面

\[**ITParticipantEvent** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**ITParticipantEvent** 介面包含可取得參與者事件描述的方法。 當應用程式的 [**ITTAPIEventNotification：： Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)方法的實，指出 [**TAPI \_ 事件**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)等於 **TE \_ 私** 用時，方法的 *pEvent* 參數就是 **ITParticipantEvent** 介面的 **IDispatch** 指標。 這個介面的方法可以用來取得發生之參與者變更的相關資訊。

> [!Note]  
> 您必須呼叫 [**ITTAPI：:p 的 \_ >eventfilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) 方法，並設定包含 **TE \_ 私** 用事件的事件篩選遮罩，以啟用參與者事件的接收。 如果您未呼叫 **ITTAPI：:p] \_ >eventfilter**，您的應用程式將不會收到任何事件。 如需詳細資訊，請參閱 [事件](events.md) 總覽。

 

## <a name="members"></a>成員

**ITParticipantEvent** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITParticipantEvent** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITParticipantEvent** 介面具有這些方法。



| 方法                                                         | 描述                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**取得 \_ 事件**](itparticipantevent-get-event.md)             | 取得事件的 [**參與者 \_ 事件**](participant-event.md) 描述元。<br/>                                                    |
| [**取得 \_ 參與者**](itparticipantevent-get-participant.md) | 取得 [**ITParticipant**](itparticipant.md) 介面陣列的指標，代表牽涉到事件的參與者。<br/> |
| [**取得子 \_ 流**](itparticipantevent-get-substream.md)     | 取得 [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) 介面陣列的指標，代表涉及事件的子串流。<br/>       |



 

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
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**參與者 \_ 活動**](participant-event.md)
</dt> <dt>

[**ITTAPIEventNotification：： Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**TAPI \_ 事件**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[註冊事件程式碼片段](register-events.md)
</dt> </dl>

 

