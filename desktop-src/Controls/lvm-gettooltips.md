---
title: 'LVM_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項用來顯示工具提示的工具提示控制項。 您可以明確地傳送此訊息，或使用 ListView \_ GetToolTips 宏。
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- LVM_GETTOOLTIPS message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466504"
---
# <a name="lvm_gettooltips-message"></a>LVM \_ GETTOOLTIPS 訊息

抓取清單視圖控制項用來顯示工具提示的工具提示控制項。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回工具提示控制項的控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVM \_ SETTOOLTIPS**](lvm-settooltips.md)
</dt> </dl>

 

 





