---
title: 'LVN_INCREMENTALSEARCH (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，累加式搜尋已開始。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967774"
---
# <a name="lvn_incrementalsearch-notification-code"></a>LVN \_ INCREMENTALSEARCH 通知碼

通知清單視圖控制項的父視窗，累加式搜尋已開始。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* \[在\]
</dt> <dd>

描述通知碼的 [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) 結構指標。 呼叫端負責配置此結構，包括包含的 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 和 [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) 結構。 設定 **NMHDR** 結構的成員。 程式 **代碼** 成員必須設定為 LVN \_ INCREMENTALSEARCH。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

通知接收者會轉換 *lParam* 來取出 [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) 結構。 *WParam* 參數包含傳送此通知碼之控制項的識別碼。

此通知碼會提供應用程式 (或通知接收器) 自訂增量搜尋的機會。 例如，如果搜尋專案是數值，則應用程式可以執行數值搜尋，而不是字串搜尋。

應用程式會將 [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema)結構中所包含之 [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa)結構的 **lParam** 成員設定為搜尋結果，或設定為另一個應用程式定義的值，以使搜尋失敗，並向控制項指出如何繼續進行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl>   |
| Unicode 與 ANSI 名稱<br/>   | **LVN \_INCREMENTALSEARCHW** (Unicode) 和 **LVN \_ INCREMENTALSEARCHA** (ANSI) <br/> |



 

 





