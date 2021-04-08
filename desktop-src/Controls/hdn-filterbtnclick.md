---
title: 'HDN_FILTERBTNCLICK (Commctrl 的通知碼) '
description: 當按一下 [篩選] 按鈕或回應 HDM SETITEM 訊息時，通知標題控制項的父視窗 \_ 。 此通知碼以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843151"
---
# <a name="hdn_filterbtnclick-notification-code"></a>HDN \_ FILTERBTNCLICK 通知碼

當按一下 [篩選] 按鈕或回應 [**HDM \_ SETITEM**](hdm-setitem.md) 訊息時，通知標題控制項的父視窗。 此通知碼以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)結構的指標，其中包含標題控制項和標頭篩選按鈕的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果您傳回 **TRUE**， [HDN \_ FILTERCHANGE](hdn-filterchange.md) 通知碼將會傳送至標題控制項的父視窗。 此通知碼可讓父視窗有機會同步處理其使用者介面元素。 如果您不想傳送通知，則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





