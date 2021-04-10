---
title: 'EM_SETMODIFY 訊息 (Winuser .h) '
description: 設定或清除編輯控制項的修改旗標。 修改旗標會指出是否已修改編輯控制項內的文字。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_SETMODIFY message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843808"
---
# <a name="em_setmodify-message"></a>EM \_ SETMODIFY 訊息

設定或清除編輯控制項的修改旗標。 修改旗標會指出是否已修改編輯控制項內的文字。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

修改旗標的新值。 值為 **TRUE** 表示文字已經過修改，而值為 **FALSE** 表示未修改。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

建立控制項時，系統會自動將修改旗標清除為零。 如果使用者變更控制項的文字，系統會將旗標設定為非零。 您可以將 [**EM \_ GETMODIFY**](em-getmodify.md) 訊息傳送至編輯控制項，以取得旗標的目前狀態。

**Rich Edit 1.0：** 當修改旗標設為 **FALSE** 時，不含 **REO \_ DYNAMICSIZE** 旗標的建立物件將會鎖定其範圍。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

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

[**EM \_ GETMODIFY**](em-getmodify.md)
</dt> <dt>

[**REOBJECT**](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





