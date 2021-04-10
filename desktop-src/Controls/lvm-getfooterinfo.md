---
title: 'LVM_GETFOOTERINFO 訊息 (Commctrl .h) '
description: 取得清單視圖控制項頁尾的相關資訊。 明確地傳送此訊息，或使用 ListView \_ GetFooterInfo 宏。
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- LVM_GETFOOTERINFO message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933923"
---
# <a name="lvm_getfooterinfo-message"></a>LVM \_ GETFOOTERINFO 訊息

取得清單視圖控制項頁尾的相關資訊。 明確地傳送此訊息，或使用 [**ListView \_ GetFooterInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用。 必須是 0。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

[**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo)結構的指標，用來接收資訊，視 **遮罩** 成員的值而定。 呼叫進程負責配置此結構及設定 **遮罩** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





