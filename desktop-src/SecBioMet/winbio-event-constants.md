---
title: 'WINBIO_EVENT 常數 (Winbio \_ 類型 .h) '
description: 指定要監視的服務提供者事件通知類型。
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a871022c51a906bd078125ae6aa6aa30c2e97024279f3309ca4ece58c00a88f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910656"
---
# <a name="winbio_event-constants"></a>WINBIO \_ 事件常數

下列常數可以用在 [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) 函式中，以指定要監視的服務提供者事件通知類型。



| 常數                                                                                                                                                                                                                        | 描述                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <dt>**WINBIO \_ 事件 \_ FP \_ 取消認領**</dt> </dl>                             | 感應器偵測到沒有應用程式要求的手指，或是目前有焦點的視窗。 Windows 生物特徵辨識架構會呼叫您的回呼函式，以表示已發生手指刷，但不會嘗試識別指紋。<br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <dt>**WINBIO \_ 事件 \_ FP \_ 取消認領 \_ 識別**</dt> </dl> | 感應器偵測到沒有應用程式要求的手指，或是目前有焦點的視窗。 Windows 生物特徵辨識架構會嘗試識別指紋，並將該進程的結果傳遞給您的回呼函式。<br/>                        |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> </dl>

 

 





