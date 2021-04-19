---
description: 使用一組受限制的查詢來起始與事件提供者的通訊。
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: 'IWbemEventSink 介面 (Wbemprov .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 22a3a15920d26f482cedfa3a596fd439ea70c2f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996886"
---
# <a name="iwbemeventsink-interface"></a>IWbemEventSink 介面

**IWbemEventSink** 介面會使用一組受限制的查詢來起始與事件提供者的通訊。 這個介面會擴充 [**IWbemObjectSink**](iwbemobjectsink.md)，提供處理安全性和效能的新方法。 如需使用此介面的詳細資訊，請參閱 [撰寫事件提供者](writing-an-event-provider.md) 和 [保護 WMI 事件](securing-wmi-events.md)。

## <a name="members"></a>成員

**IWbemEventSink** 介面具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWbemEventSink** 介面具有這些方法。



| 方法                                                                | 描述                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | 由取用者呼叫以設定受限制的事件查詢。<br/> |
| [**IsActive**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | 檢查事件接收的狀態。<br/>                               |
| [**SetBatchingParameters**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | 由取用者呼叫以設定批次參數。<br/>         |
| [**SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | 用來更新事件接收上的安全描述項。<br/>   |



 

## <a name="remarks"></a>備註

當 ([**IWbemObjectSink**](iwbemobjectsink.md) 或 **IWbemEventSink**) 執行事件訂閱接收時，請勿從接收器物件的方法內呼叫 WMI。 例如，呼叫 [**IWbemServices：： CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) ，以在 [**IWbemEventSink：： SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) 的實中取消接收，可能會干擾 WMI 狀態。 若要取消事件訂閱，請設定旗標，並從另一個執行緒或物件呼叫 **IWbemServices：： CancelAsyncCall** 。 對於與事件接收無關的執行（例如物件、列舉和查詢查詢），您可以回呼 WMI。

接收程式應在100毫秒內處理事件通知，因為傳遞事件通知的 WMI 執行緒無法執行其他工作，直到接收物件處理完成為止。 如果通知需要大量處理，接收端可以使用另一個執行緒的內部佇列來處理處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                            |
| 標頭<br/>                   | <dl> <dt>Wbemprov (包含 Wbemidl) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Wbemuuid .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Wbemsvc.dll</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[適用于 WMI 的 COM API](com-api-for-wmi.md)
</dt> </dl>

 

 




