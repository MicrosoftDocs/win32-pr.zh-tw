---
title: 'LVM_GETBKIMAGE 訊息 (Commctrl .h) '
description: 取得清單視圖控制項中的背景影像。 您可以明確地傳送此訊息，或使用 ListView \_ GetBkImage 宏來傳送。
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- LVM_GETBKIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685522"
---
# <a name="lvm_getbkimage-message"></a>LVM \_ GETBKIMAGE 訊息

取得清單視圖控制項中的背景影像。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea)結構的指標，此結構會接收背景影像資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_GETBKIMAGEW** (Unicode) 和 **LVM \_ GETBKIMAGEA** (ANSI) <br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVM \_ SETBKIMAGE**](lvm-setbkimage.md)
</dt> </dl>

 

 





