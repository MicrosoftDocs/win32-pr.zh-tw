---
title: 'TB_SETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 設定用來繪製工具列之插入標記的色彩。
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- TB_SETINSERTMARKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 466c9bfe27462b11cc0c6cf3a183328ddedb1b422b4d0c07b4496c7a90f83890
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540038"
---
# <a name="tb_setinsertmarkcolor-message"></a>TB \_ SETINSERTMARKCOLOR 訊息

設定用來繪製工具列之插入標記的色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

**COLORREF** 值，其中包含新的插入標記色彩。

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

[**TB \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





