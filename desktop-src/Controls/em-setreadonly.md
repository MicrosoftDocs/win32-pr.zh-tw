---
title: 'EM_SETREADONLY 訊息 (Winuser .h) '
description: 設定或移除編輯控制項 (ES READONLY) 的唯讀樣式 \_ 。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- EM_SETREADONLY message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094503"
---
# <a name="em_setreadonly-message"></a>EM \_ SETREADONLY 訊息

設定或移除編輯控制項 ([**ES \_ READONLY**](edit-control-styles.md)) 的唯讀樣式。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定是否要設定或移除 [**ES \_ READONLY**](edit-control-styles.md) 樣式。 **TRUE** 值會設定 **es \_ readonly** 樣式; **FALSE** 值會移除 **es \_ readonly** 樣式。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為非零。

如果作業失敗，則傳回值為零。

## <a name="remarks"></a>備註

當編輯控制項具有 [**ES \_ READONLY**](edit-control-styles.md) 樣式時，使用者無法變更編輯控制項內的文字。

若要判斷編輯控制項是否有 [**ES \_ READONLY**](edit-control-styles.md) 樣式，請使用 [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) 函數搭配 GWL \_ 樣式旗標。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

