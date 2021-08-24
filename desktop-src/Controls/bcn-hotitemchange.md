---
title: 'BCN_HOTITEMCHANGE (Commctrl 的通知碼) '
description: 通知按鈕控制項擁有者滑鼠正在進入或離開按鈕控制項的工作區。 按鈕控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6966978dc1d1eee1d84a9e5caa51116ccb96e098d2c196ea143051663abbf4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921368"
---
# <a name="bcn_hotitemchange-notification-code"></a>BCN \_ HOTITEMCHANGE 通知碼

通知按鈕控制項擁有者滑鼠正在進入或離開按鈕控制項的工作區。 按鈕控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





