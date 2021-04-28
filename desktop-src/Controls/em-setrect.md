---
title: 'EM_SETRECT 訊息 (Winuser .h) '
description: EM_SETRECT 訊息：設定多行編輯控制項的格式化矩形。
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042428a236b8e9a23f03cdcceaf5d76eb977efd8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085966"
---
# <a name="em_setrect-message"></a>EM \_ SETRECT 訊息

設定多行編輯控制項的 [格式化矩形](about-edit-controls.md) 。 格式化矩形是控制項用來繪製文字的限制矩形。 限制矩形與編輯控制項視窗的大小無關。

此訊息只會由多行編輯控制項處理。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 2.0 和更新版本：** 指出 *lParam* 是否指定絕對或相對座標。 值為零表示絕對座標。 值為1時，表示相對於目前格式化矩形的位移。  (位移可以是正數或負數。 ) 

**編輯控制項和 Rich edit 1.0：** 未使用此參數，且必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形結構的**](/previous-versions//dd162897(v=vs.85))指標，指定矩形的新維度。 如果這個參數為 **Null**，則會將格式化矩形設定為其預設值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

如果已安裝觸控裝置，或從已 (安裝勾點的執行緒傳送 **EM \_ SETRECT** ，則將 *lParam* 設定為 **Null** 沒有任何作用，請參閱 [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)) 。 在這些情況下， *lParam* 應該包含 [**矩形**](/previous-versions//dd162897(v=vs.85)) 結構的有效指標。

**EM \_ SETRECT** 訊息會重新繪製編輯控制項的文字。 若要變更格式化矩形的大小而不重繪文字，請使用 [**EM \_ SETRECTNP**](em-setrectnp.md) 訊息。

當您第一次建立編輯控制項時，格式化矩形會設定為預設大小。 您可以使用 **EM \_ SETRECT** 訊息，將格式化矩形放大或小於編輯控制項視窗。

如果編輯控制項沒有水準捲軸，且格式化矩形設定為大於編輯控制項視窗，則文字行超過編輯控制項視窗的寬度 (但小於格式化矩形) 的寬度，而不是換行。

如果編輯控制項包含框線，則會以框線的大小來縮減格式化矩形。 如果您要調整 [**em \_ GETRECT**](em-getrect.md) 訊息所傳回的矩形，您必須先移除框線的大小，然後才能使用該矩形搭配 **EM \_ SETRECT** 訊息。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 格式化矩形不包含選取範圍列，也就是每個段落左方未標記的區域。 當使用者按一下選取範圍時，就會選取對應的行。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ GETRECT**](em-getrect.md)
</dt> <dt>

[**EM \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**矩形**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

