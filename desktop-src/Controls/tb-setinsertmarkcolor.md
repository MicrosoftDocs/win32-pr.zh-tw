---
title: 'TB_SETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 設定用來繪製工具列之插入標記的色彩。
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- TB_SETINSERTMARKCOLOR message Windows 控制項
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
ms.openlocfilehash: 954654d71a3e3b7bba9af287d3e92fb2362e8711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093815"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ GETINSERTMARKCOLOR**](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





