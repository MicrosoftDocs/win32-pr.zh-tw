---
title: 'EM_GETRECT 訊息 (Winuser .h) '
description: 取得編輯控制項的格式化矩形。
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- EM_GETRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d4ad7dbab40a8d294d814e3524b54c5b11206c91608e9293bdf88df2a63f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541038"
---
# <a name="em_getrect-message"></a>EM \_ GETRECT 訊息

取得編輯控制項的 [格式化矩形](about-edit-controls.md) 。 格式化矩形是控制項用來繪製文字的限制矩形。 限制矩形與編輯控制項視窗的大小無關。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收格式化矩形。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值沒有意義。

## <a name="remarks"></a>備註

您可以使用 [**em \_ SETRECT**](em-setrect.md) 和 [**em \_ SETRECTNP**](em-setrectnp.md) 訊息來修改多行編輯控制項的格式化矩形。

在某些情況下， **em \_ GETRECT** 可能不會傳回 [**em \_ SETRECT**](em-setrect.md) 或 [**em \_ SETRECTNP**](em-setrectnp.md) 所設定的確切值，但它可以是由幾個圖元來關閉。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 格式化矩形不包含選取範圍列，也就是每個段落左方未標記的區域。 按一下時，選取列會選取該行。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ SETRECT**](em-setrect.md)
</dt> <dt>

[**EM \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**矩形**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

