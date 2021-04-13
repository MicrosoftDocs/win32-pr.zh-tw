---
title: 'LVM_SETBKIMAGE 訊息 (Commctrl .h) '
description: 在清單視圖控制項中設定背景影像。 您可以明確地傳送此訊息，或使用 ListView \_ SetBkImage 宏來傳送。
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- LVM_SETBKIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465873"
---
# <a name="lvm_setbkimage-message"></a>LVM \_ SETBKIMAGE 訊息

在清單視圖控制項中設定背景影像。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea)結構的指標，其中包含新的背景影像資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。 如果 [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea)結構的 **UlFlags** 成員是 **LVBKIF \_ 來源 \_ NONE**，則傳回零。

## <a name="remarks"></a>備註

由於清單視圖控制項會使用 OLE COM 來操作背景影像，因此呼叫端應用程式必須呼叫 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 或 [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ，才能傳送此訊息。 最好是在應用程式初始化時呼叫其中一個函式，並在應用程式終止時呼叫 [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) 或 [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_SETBKIMAGEW** (Unicode) 和 **LVM \_ SETBKIMAGEA** (ANSI) <br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVM \_ GETBKIMAGE**](lvm-getbkimage.md)
</dt> </dl>

 

