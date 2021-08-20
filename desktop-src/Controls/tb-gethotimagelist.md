---
title: 'TB_GETHOTIMAGELIST 訊息 (Commctrl .h) '
description: 抓取工具列控制項用來顯示熱按鈕的影像清單。
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69d1c77377553ae19a008f80e692e3c87487bc9874593d5f3d1e692658c4ad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168511"
---
# <a name="tb_gethotimagelist-message"></a>TB \_ GETHOTIMAGELIST 訊息

抓取工具列控制項用來顯示熱按鈕的影像清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回影像清單的控制碼，控制項會使用此控制碼來顯示熱按鈕; 如果未設定任何熱影像清單，則傳回 **Null** 。

## <a name="remarks"></a>備註

當游標停留在按鈕上時，按鈕會是經常性的。 Toolbar 控制項必須具有 [**TBSTYLE 的 \_**](toolbar-control-and-button-styles.md) 一般或 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式，才能有熱專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





