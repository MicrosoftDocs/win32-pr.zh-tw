---
description: 抓取 Windows 工作列的周框。
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: 'ABM_GETTASKBARPOS 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511072"
---
# <a name="abm_gettaskbarpos-message"></a>ABM \_ GETTASKBARPOS 訊息

抓取 Windows 工作列的周框。


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標，其 **rc** 成員會收到工作列的周框（以螢幕座標為單位）。 傳送此訊息時，您必須指定 **cbSize** ;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ;否則 **為 FALSE**。

## <a name="remarks"></a>備註

請注意，這只適用于系統工作列。 其他物件（特別是協力廠商軟體提供的工具列）也可以存在。 如此一來，使用者就看不到 Windows 工作列所涵蓋的某些螢幕區域。 若要取出工作列和其他應用程式橫條未涵蓋的畫面區域，可供您的應用程式使用的工作區，請使用 [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

