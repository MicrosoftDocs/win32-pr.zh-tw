---
title: 'PGM_SETSCROLLINFO 訊息 (Commctrl .h) '
description: 設定分頁控制項的滾動參數，包括超時值、每個超時的行數，以及每行的圖元。 您可以明確地傳送此訊息，或使用 [呼叫器 \_ SetScrollInfo 宏]。
ms.assetid: e02450b8-f2b5-45b2-9395-d7412119849c
keywords:
- PGM_SETSCROLLINFO message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8fc230e1a12968d0eb29f8ba512848df42b64b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843427"
---
# <a name="pgm_setscrollinfo-message"></a>PGM \_ SETSCROLLINFO 訊息

\[適用于內部用途;不建議在應用程式中使用。 未來的 Windows 版本可能不支援此訊息。\]

設定分頁控制項的滾動參數，包括超時值、每個超時的行數，以及每行的圖元。 您可以明確地傳送此訊息，或使用 [ [**呼叫器 \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo) 宏]。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定捲軸之超時值的 **UINT** （以毫秒為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是一種 **UINT** ，可指定每個 timeout 所要滾動的行數。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是一種 **UINT** ，可指定每行的圖元數。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="security-considerations"></a>安全性考量

使用此訊息可能會危害程式的安全性。

## <a name="remarks"></a>備註

*WParam* timeout 值會控制當控制項已捕捉到滑鼠輸入並按下滑鼠左鍵時，分頁控制項產生滾動事件的速率。 較小的值會導致滾動更快;較大的值會導致捲動速度較慢。 預設值為按兩下時間的一到八。 如需詳細資訊，請參閱 [**GetDoubleClickTime**](/windows/desktop/api/winuser/nf-winuser-getdoubleclicktime)。

根據預設，每個滾動事件的分頁控制項會根據呼機控制項的水準或垂直方向，將等於控制項整體寬度或高度的金額滾動。 *LParam* 中的值可用來覆寫預設的滾動量。 如果未提供非零值，則滾動量就是兩個值的乘積 (LOWORD (*lParam*) \* HIWORD (*lParam*) ) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**呼機 \_ SetScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setscrollinfo)
</dt> </dl>

 

