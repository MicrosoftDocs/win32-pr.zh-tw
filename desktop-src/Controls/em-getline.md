---
title: 'EM_GETLINE 訊息 (Winuser .h) '
description: 從編輯控制項複製一行文字，並將它放在指定的緩衝區中。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETLINE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933993"
---
# <a name="em_getline-message-winuserh"></a>EM_GETLINE 訊息 (Winuser .h) 

從編輯控制項複製一行文字，並將它放在指定的緩衝區中。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的索引，這是從多行編輯控制項取出的行。 值為零會指定最頂端的行。 單行編輯控制項會忽略此參數。

</dd> <dt>

*lParam* 
</dt> <dd>

接收一行複本之緩衝區的指標。 傳送訊息之前，請先將這個緩衝區的第一個字組設為緩衝區的大小（以 **TCHAR** s）。 若為 ANSI 文字，此為位元組數;若為 Unicode 文字，此為字元數。 第一個單字中的大小會被覆制的行覆寫。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是複製的 **TCHAR** 數目。 如果 *wParam* 參數指定的行號大於編輯控制項中的行數，則傳回值為零。

## <a name="remarks"></a>備註

**編輯控制項：** 複製的行不包含終止的 null 字元。

**Rich edit 控制項：** Microsoft Rich Edit 1.0 和更新版本支援。 複製的行不包含結束的 null 字元，除非沒有複製任何文字。 如果未複製任何文字，訊息會在緩衝區的開頭放置一個 null 字元。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

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

[**EM \_ LINELENGTH**](em-linelength.md)
</dt> <dt>

[**編輯 \_ GetLine**](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

