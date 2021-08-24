---
title: 'LVM_SETTEXTBKCOLOR 訊息 (Commctrl .h) '
description: 設定清單視圖控制項中文字的背景色彩。 您可以明確地傳送此訊息，或使用 ListView \_ SetTextBkColor 宏來傳送。
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- LVM_SETTEXTBKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d9acdc193609f39fb81aa88263724a507695f15dcb8ba0c789df5c2a4f4d128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656228"
---
# <a name="lvm_settextbkcolor-message"></a>LVM \_ SETTEXTBKCOLOR 訊息

設定清單視圖控制項中文字的背景色彩。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

新的文字背景色彩。 這可以是 \_ 無背景色彩的 CLR 無。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





