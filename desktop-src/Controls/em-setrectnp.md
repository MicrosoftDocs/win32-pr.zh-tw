---
title: 'EM_SETRECTNP 訊息 (Winuser .h) '
description: EM_SETRECTNP 訊息：設定多行編輯控制項的格式化矩形。
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60341a41706f012064d3b7cbc79aa019f1492c3a8d535866fa51fc7ea8dfd437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831129"
---
# <a name="em_setrectnp-message"></a>EM \_ SETRECTNP 訊息

設定多行編輯控制項的 [格式化矩形](about-edit-controls.md) 。 **Em \_ SETRECTNP** 訊息與 [**em \_ SETRECT**](em-setrect.md)訊息相同，不同之處在于 **em \_ SETRECTNP** 不會 *重繪* 編輯控制項視窗。

格式化矩形是控制項用來繪製文字的限制矩形。 限制矩形與編輯控制項視窗的大小無關。

此訊息只會由多行編輯控制項處理。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 3.0 和更新版本：** 指出新的矩形是否包含絕對或相對座標。 值為零表示絕對座標。 值為1時，表示相對於目前格式化矩形的位移。  (位移可以是正數或負數。 ) 

**編輯控制項：** 未使用此參數，且必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形結構的**](/previous-versions//dd162897(v=vs.85))指標，指定矩形的新維度。 如果這個參數為 **Null**，則會將格式化矩形設定為其預設值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

**Rich Edit：** Microsoft Rich Edit 3.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

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

**其他資源**
</dt> <dt>

[**矩形**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

