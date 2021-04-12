---
title: 'HDM_INSERTITEM 訊息 (Commctrl .h) '
description: 將新的專案插入至標題控制項。 您可以明確地傳送此訊息，或使用標頭 \_ InsertItem 宏。
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- HDM_INSERTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465376"
---
# <a name="hdm_insertitem-message"></a>HDM \_ INSERTITEM 訊息

將新的專案插入至標題控制項。 您可以明確地傳送此訊息，或使用 [**標頭 \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要插入新專案的專案索引。 如果 *wParam* 大於或等於控制項中的專案數，則新專案會插入至標題控制項的結尾。 如果 *wParam* 為零，則會在標題控制項的開頭插入新專案。

</dd> <dt>

*lParam* 
</dt> <dd>

[**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema)結構的指標，其中包含新專案的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回新專案的索引，否則傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDM \_INSERTITEMW** (Unicode) 和 **HDM \_ INSERTITEMA** (ANSI) <br/>             |



 

 





