---
title: 'TB_SETHOTIMAGELIST 訊息 (Commctrl .h) '
description: 設定工具列控制項將用來顯示熱按鈕的影像清單。
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d07c66add48fa8022f7b8505bee377be184af3ed8195251b3a92b46d0ff58c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318848"
---
# <a name="tb_sethotimagelist-message"></a>TB \_ SETHOTIMAGELIST 訊息

設定工具列控制項將用來顯示熱按鈕的影像清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

將設定之影像清單的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前用來顯示熱按鈕的影像清單控制碼，如果先前未設定任何影像清單，則傳回 **Null** 。

## <a name="remarks"></a>備註

當游標停留在按鈕上時，按鈕會是經常性的。 Toolbar 控制項必須具有 [**TBSTYLE 的 \_**](toolbar-control-and-button-styles.md) 一般或 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式，才能有熱專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





