---
title: 'TB_GETINSERTMARKCOLOR 訊息 (Commctrl .h) '
description: 抓取用來繪製工具列之插入標記的色彩。
ms.assetid: 52915dc6-a45c-4f3b-aa9b-99a23d423e59
keywords:
- TB_GETINSERTMARKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd87c27252f9838001d10320b3b9783ef598eea654d384deaa383ad5c5f6cddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918718"
---
# <a name="tb_getinsertmarkcolor-message"></a>TB \_ GETINSERTMARKCOLOR 訊息

抓取用來繪製工具列之插入標記的色彩。

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

[**TB \_ SETINSERTMARKCOLOR**](tb-setinsertmarkcolor.md)
</dt> </dl>

 

