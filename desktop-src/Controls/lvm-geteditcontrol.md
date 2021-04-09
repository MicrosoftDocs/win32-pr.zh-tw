---
title: 'LVM_GETEDITCONTROL 訊息 (Commctrl .h) '
description: 取得編輯控制項的控制碼，這個控制項是用來編輯清單視圖專案的文字。 您可以明確地傳送此訊息，或使用 ListView \_ GetEditControl 宏來傳送。
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- LVM_GETEDITCONTROL message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024593"
---
# <a name="lvm_geteditcontrol-message"></a>LVM \_ GETEDITCONTROL 訊息

取得編輯控制項的控制碼，這個控制項是用來編輯清單視圖專案的文字。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回編輯控制項的控制碼，否則傳回 **Null** 。

## <a name="remarks"></a>備註

當標籤編輯開始時，會建立、定位和初始化編輯控制項。 在顯示之前，清單視圖控制項會將 [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) 通知程式碼傳送給其父視窗。

若要自訂標籤編輯，請執行 [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) 的處理常式，並讓它將 **LVM \_ GETEDITCONTROL** 訊息傳送至清單視圖控制項。 如果正在編輯標籤，傳回值將會是編輯控制項的控制碼。 您可以使用此控制碼來自訂編輯控制項，方法是傳送一般的 **EM \_ XXX** 訊息。

當使用者完成或取消編輯時，就會終結編輯控制項，而且控制碼不再有效。 您可以子類別化編輯控制項，但您不應該將它終結。 若要取消編輯，請將清單 view 控制項傳送至 [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) 訊息。

正在編輯的清單視圖專案是目前焦點的專案，也就是處於焦點狀態的專案。 若要根據專案的狀態尋找專案，請使用 [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ListView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

