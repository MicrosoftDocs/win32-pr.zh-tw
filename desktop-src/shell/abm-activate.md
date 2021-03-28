---
description: 通知系統 appbar 已啟用。 Appbar 應該呼叫此訊息以回應 WM \_ 啟動訊息。
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: 'ABM_ACTI加值稅E 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112365"
---
# <a name="abm_activate-message"></a>ABM \_ 啟動訊息

通知系統 appbar 已啟用。 Appbar 應該呼叫此訊息以回應 [**WM \_ 啟動**](/windows/desktop/inputdev/wm-activate) 訊息。


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標，此結構識別要啟用的 appbar。 傳送此訊息時，您必須指定 **cbSize** 和 **hWnd** 成員;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

一律傳回 **TRUE**。

## <a name="remarks"></a>備註

如果 *pabd* 所指向之結構的 **hWnd** 成員識別自動隱藏 appbar，則會忽略此訊息。 系統會自動設定自動隱藏透過像 appbars 的迭置順序。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

