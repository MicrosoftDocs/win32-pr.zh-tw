---
title: 'LVN_COLUMNOVERFLOWCLICK (Commctrl 的通知碼) '
description: 當按一下其溢位按鈕時，由清單視圖控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 3d3bb7be-b598-450a-b829-a5aa5b1a0c5d
keywords:
- LVN_COLUMNOVERFLOWCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_COLUMNOVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb28deb3dd98542791b4c8daf350e618e43db57d5090a93d49af5e55e8b39ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077118"
---
# <a name="lvn_columnoverflowclick-notification-code"></a>LVN \_ COLUMNOVERFLOWCLICK 通知碼

當按一下其溢位按鈕時，由清單視圖控制項所傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_COLUMNOVERFLOWCLICK
     
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* \[在\]
</dt> <dd>

描述通知碼的 [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) 結構指標。 呼叫端負責配置此結構，包括包含的 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構。 設定 **NMHDR** 結構的成員。 程式 **代碼** 成員必須設定為 LVN \_ COLUMNOVERFLOWCLICK。

將 [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的 **iItem** 成員設定為-1。 將 **iSubItem** 成員設定為子集合的索引。 將 **uNewState**、 **uOldState** 和 **lParam** 成員設定為零。 不會使用 **NMLISTVIEW** 結構的其餘成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

通知接收者會轉換 *lParam* 來取出 [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) 結構。 *WParam* 參數包含傳送通知碼之控制項的識別碼。

如果標題控制項是 listview 的子系，標題控制項應該會在標題控制項收到 [HDN \_ OVERFLOWCLICK](hdn-overflowclick.md) 通知程式碼時，將此通知碼傳送至 listview 控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





