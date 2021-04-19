---
description: 定義回呼函式&\# 郵件; 您可以在應用程式中執行此函式，&\# 郵件; 也就是指定給 WFDStartDisplaySink 函式的應用程式。
ms.assetid: 0D4C00FD-4ED6-4F0F-BB72-0A1FCC05DB37
title: 'WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK 回呼函數 (Wfdsink) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK
api_type:
- UserDefined
api_location:
- wfdsink.h
ms.openlocfilehash: c576f88a5b7f97484647c4c06f44522a5c3c379f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980832"
---
# <a name="wfd_display_sink_notification_callback-callback-function"></a>WFD \_ 顯示 \_ 接收 \_ 通知 \_ 回呼回呼函式

[ **WFD \_ 顯示 \_ 接收 \_ 通知 \_ 回檔** 函式] 會定義回呼函式（您在應用程式中所執行），此函式是指定給 [**WFDStartDisplaySink**](wfdstartdisplaysink.md) 函式的函數。

## <a name="syntax"></a>語法


```C++
DWORD CALLBACK WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK(
  _In_opt_          PVOID                                 pvContext,
  _In_        const PWFD_DISPLAY_SINK_NOTIFICATION        pNotification,
  _Inout_opt_       PWFD_DISPLAY_SINK_NOTIFICATION_RESULT pNotificationResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pvCoNtext* \[在中，選擇性\]
</dt> <dd>

傳遞給回呼函式的選擇性內容指標。

</dd> <dt>

*pNotification* \[在\]
</dt> <dd>

結構的指標，其中包含有關顯示接收通知的資料。

</dd> <dt>

*pNotificationResult* \[in、out、optional\]
</dt> <dd>

結構的指標，其中包含您的應用程式可以選擇性地設定的資料，以表示處理顯示接收通知的結果。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wfdsink。h</dt> </dl> |



 

 




