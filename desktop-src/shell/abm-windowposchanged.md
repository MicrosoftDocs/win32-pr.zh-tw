---
description: 在 appbar 的位置變更時通知系統。 Appbar 應該呼叫此訊息以回應 WM \_ WINDOWPOSCHANGED 訊息。
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: 'ABM_WINDOWPOSCHANGED 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d770d50629342095308376856b98e6250adc1f9a1f2559da8509d685995428ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057808"
---
# <a name="abm_windowposchanged-message"></a>ABM \_ WINDOWPOSCHANGED 訊息

在 appbar 的位置變更時通知系統。 Appbar 應該呼叫此訊息以回應 [**WM \_ WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) 訊息。


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
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

如果 *pabd* 所指向之結構的 **hWnd** 成員識別自動隱藏 appbar，則會忽略此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

