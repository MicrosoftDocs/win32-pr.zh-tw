---
title: 'LVM_HITTEST 訊息 (Commctrl .h) '
description: 判斷哪一個清單視圖專案（如果有的話）位於指定的位置。 您可以明確地傳送此訊息，或使用 ListView \_ system.windows.media.visualtreehelper.hittest 宏來傳送。
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- LVM_HITTEST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81308249992b134dd3fa2bd0bc43ff0074bc3bae7048072ada7d68b0a867a979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958167"
---
# <a name="lvm_hittest-message"></a>LVM \_ system.windows.media.visualtreehelper.hittest 訊息

判斷哪一個清單視圖專案（如果有的話）位於指定的位置。 您可以明確地傳送此訊息，或使用 [**ListView \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須是 0。 **WindowsVista。** 如果要取出 *lParam* 結構的 **iGroup** 和 **iSubItem** 成員，則應該是-1。</dd> <dt>

*lParam* 
</dt> <dd>

[**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo)結構的指標，其中包含要點擊測試的位置，並接收點擊測試結果的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回位於指定位置之專案的索引（如果有的話），否則傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





