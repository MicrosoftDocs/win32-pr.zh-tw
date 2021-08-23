---
title: 'TCN_GETOBJECT (Commctrl 的通知碼) '
description: 當索引標籤控制項具有 TCS \_ EX \_ REGISTERDROP 擴充樣式，且將物件拖曳至控制項中的索引標籤專案上方時，便會傳送此控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf5ec3a314a7380ccff5f8613145c890f8f304d73289ad5354b8668a09070b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166901"
---
# <a name="tcn_getobject-notification-code"></a>TCN \_ GETOBJECT 通知碼

當索引標籤控制項具有 [**TCS \_ EX \_ REGISTERDROP**](tab-control-extended-styles.md) 擴充樣式，且將物件拖曳至控制項中的索引標籤專案上方時，便會傳送此控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的指標，其中包含物件拖曳到的索引標籤專案的相關資訊，並接收應用程式傳回的資料以回應此訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

處理此通知程式碼的應用程式必須傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





