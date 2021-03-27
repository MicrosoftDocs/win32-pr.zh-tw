---
description: 設定 Windows 工作列的自動隱藏和 alwayson 最上層狀態。
title: 'ABM_SETSTATE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972093"
---
# <a name="abm_setstate-message"></a>ABM \_ SETSTATE 訊息

設定 Windows 工作列的自動隱藏和 alwayson 最上層狀態。


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。 傳送此訊息時，您必須指定 **cbSize** 和 **hWnd** 成員。 您可以使用下列其中一個值，在 **lParam** 成員中傳送所需狀態的資料。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

自動隱藏和永遠開啟-頂端

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS \_ ALWAYSONTOP**


</dt> <dd>

Always on-頂端開啟，自動隱藏

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS 自動 \_ 隱藏**


</dt> <dd>

自動隱藏開啟、永遠開啟

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS 自動 \_ 隱藏 \| ABS \_ ALWAYSONTOP**


</dt> <dd>

自動隱藏和隨時開啟

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

一律傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

 




