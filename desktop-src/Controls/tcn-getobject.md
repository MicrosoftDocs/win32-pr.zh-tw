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
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965691"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





