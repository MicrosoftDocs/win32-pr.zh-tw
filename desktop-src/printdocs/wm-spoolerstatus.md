---
description: 只要在 \_ 列印管理員佇列中加入或移除工作，就會從列印管理員傳送 WM SPOOLERSTATUS 訊息。
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: 'WM_SPOOLERSTATUS 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115685"
---
# <a name="wm_spoolerstatus-message"></a>WM \_ SPOOLERSTATUS 訊息

只要在列印管理員佇列中加入或移除工作，就會從列印管理員傳送 **WM \_ SPOOLERSTATUS** 訊息。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

PR \_ JOBSTATUS 旗標。

</dd> <dt>

*lParam* 
</dt> <dd>

低序位字組指定列印管理員佇列中剩餘的工作數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

此訊息僅供參考之用。 這則訊息是建議的訊息，並不保證傳遞的語法。 應用程式不應假設它們會 \_ 在每次變更多工緩衝處理器狀態時收到 WM SPOOLERSTATUS 訊息。

在 \_ WINDOWS XP 之後，不支援 WM SPOOLERSTATUS 訊息。 若要在列印佇列狀態變更時收到通知，您可以使用 [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) 和 [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 訊息](printing-and-print-spooler-messages.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

