---
title: 'HWINEVENTHOOK (Windef) '
description: 用來宣告視窗事件攔截函式。
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- HWINEVENTHOOK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966313"
---
# <a name="hwineventhook"></a>HWINEVENTHOOK

用來宣告視窗事件攔截函式。


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>備註

這個資料類型會與 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) 回呼函式和 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) 和 [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) 函數搭配使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                                          |
| 可轉散發套件<br/>          | 使用 SP6 和更新版本和 Windows 95 在 Windows NT 4.0 上 Active Accessibility 1.3 的 RDK<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Windef .h (WINVER >= 0x0500)  (包含 Windows .h) </dt> </dl> |



 

 





