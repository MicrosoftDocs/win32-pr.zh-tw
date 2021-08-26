---
title: IRDVTaskPluginNotifySink 介面
description: 工作代理程式會使用 IRDVTaskPluginNotifySink 介面來與觸發程式代理程式進行通訊。
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- IRDVTaskPluginNotifySink 介面遠端桌面服務
- IRDVTaskPluginNotifySink 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88692175fedbad4faf5b2755ce92897cff25fe9d588e6fb446d8174407aa6b5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072388"
---
# <a name="irdvtaskpluginnotifysink-interface"></a>IRDVTaskPluginNotifySink 介面

工作代理程式會使用 **IRDVTaskPluginNotifySink** 介面來與觸發程式代理程式進行通訊。 這個介面的指標會傳遞至 [**IRDVTaskPlugin：： Initialize**](irdvtaskplugin-initialize.md) 方法中的工作代理程式。

## <a name="members"></a>成員

**IRDVTaskPluginNotifySink** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IRDVTaskPluginNotifySink** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IRDVTaskPluginNotifySink** 介面具有這些方法。



| 方法                                                                  | 描述                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**DeleteSchedule**](irdvtaskpluginnotifysink-deleteschedule.md)       | 由工作代理程式呼叫以刪除已排程的工作。<br/>                   |
| [**OnTaskStateChange**](irdvtaskpluginnotifysink-ontaskstatechange.md) | 用來通知觸發程式代理程式工作的狀態已變更。<br/> |
| [**OnTerminated**](irdvtaskpluginnotifysink-onterminated.md)           | 由工作代理程式呼叫，以要求關閉工作代理程式。<br/>  |
| [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md)           | 由工作代理程式呼叫以排程工作。<br/>                           |



 

## <a name="remarks"></a>備註

雖然下列需求中所識別的作業系統支援這個介面，但只有在虛擬機器裝載于 Windows Server 2012 時，才會使用此介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------|
| 最低支援的用戶端<br/> | Windows 7 Enterprise<br/>   |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/> |



 

