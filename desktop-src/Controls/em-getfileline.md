---
title: 'EM_GETFILELINE 訊息 (CommCtrl .h) '
description: 從編輯控制項複製一行文字，與螢幕上顯示線條的方式無關，然後將它放在指定的緩衝區中。
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- EM_GETFILELINE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466109"
---
# <a name="em_getfileline-message-commctrlh"></a>EM_GETFILELINE 訊息 (CommCtrl .h) 

從編輯控制項複製一行文字，與螢幕上顯示線條的方式無關，然後將它放在指定的緩衝區中。

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

複製的行不包含終止的 null 字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限 1809 desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2019 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ FILELINELENGTH**](em-filelinelength.md)
</dt> <dt>

[**編輯 \_ GetFileLine**](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

**其他資源**
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

