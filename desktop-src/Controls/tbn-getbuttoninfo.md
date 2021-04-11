---
title: 'TBN_GETBUTTONINFO (Commctrl 的通知碼) '
description: 抓取工具列自訂資訊，並通知工具列的父視窗對工具列進行的任何變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934781"
---
# <a name="tbn_getbuttoninfo-notification-code"></a>TBN \_ GETBUTTONINFO 通知碼

抓取工具列自訂資訊，並通知工具列的父視窗對工具列進行的任何變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標。 **IItem** 成員會指定以零為起始的索引，此索引會提供 [自訂工具列] 對話方塊所顯示的按鈕計數，以及工具列上顯示的按鈕。 **PszText** 成員指定目前按鈕文字的位址，而 **cchText** 指定其長度（以字元為單位）。 應用程式應該以按鈕的相關資訊填入結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果按鈕資訊已複製到指定的結構，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

工具列控制項會配置緩衝區，而接收者 (父視窗) 必須將文字複製到該緩衝區。 當 TBN \_ GETBUTTONINFO 傳送至父視窗時，cchText 成員會包含工具列所配置的緩衝區長度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TBN \_GETBUTTONINFOW** (Unicode) 和 **TBN \_ GETBUTTONINFOA** (ANSI) <br/>       |



 

 





