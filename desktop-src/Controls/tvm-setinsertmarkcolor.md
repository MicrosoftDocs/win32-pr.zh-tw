---
title: 'TVM_SETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 設定用來繪製樹狀檢視之插入標記的色彩。 您可以使用 TreeView SetInsertMarkColor 宏明確地傳送此訊息 \_ 。
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- TVM_SETINSERTMARKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d5fd9984b77c99a13e1c7eab24c231e0ce7f601ecb79f8747cdf7ea3011327
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636758"
---
# <a name="tvm_setinsertmarkcolor-message"></a>TVM \_ SETINSERTMARKCOLOR 訊息

設定用來繪製樹狀檢視之插入標記的色彩。 您可以使用 [**TreeView \_ SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) 值，其中包含新的插入標記色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含先前插入標記色彩的 **COLORREF** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ GETINSERTMARKCOLOR**](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

