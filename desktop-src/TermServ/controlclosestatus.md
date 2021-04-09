---
title: ControlCloseStatus 列舉
description: 指出包含控制項的應用程式是否可以立即關閉控制項。
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- ControlCloseStatus 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934009"
---
# <a name="controlclosestatus-enumeration"></a>ControlCloseStatus 列舉

指出包含控制項的應用程式是否可以立即關閉控制項。

## <a name="syntax"></a>Syntax


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**
</dt> <dd>

容器可以立即關閉。 如果控制項未連接，就會發生這種情況。

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**
</dt> <dd>

容器應等候事件 [**IMsTscAxEvents：： OnDisconnected**](imstscaxevents-ondisconnected.md) 或 [**IMsTscAxEvents：： OnConfirmClose**](imstscaxevents-onconfirmclose.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                      |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





