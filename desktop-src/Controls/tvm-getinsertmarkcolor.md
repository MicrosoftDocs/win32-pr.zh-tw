---
title: 'TVM_GETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 抓取用來繪製樹狀檢視之插入標記的色彩。 您可以使用 TreeView GetInsertMarkColor 宏明確地傳送此訊息 \_ 。
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- TVM_GETINSERTMARKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38c784f6b3c363d68472270f0f52cb97cea7c13b6eb709d1aba4975d3cd97bca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834148"
---
# <a name="tvm_getinsertmarkcolor-message"></a>TVM \_ GETINSERTMARKCOLOR 訊息

抓取用來繪製樹狀檢視之插入標記的色彩。 您可以使用 [**TreeView \_ GetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含目前插入標記色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ SETINSERTMARKCOLOR**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

