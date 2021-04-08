---
title: 'TB_GETIMAGELIST 訊息 (Commctrl .h) '
description: 抓取工具列控制項用來顯示其預設狀態之按鈕的影像清單。 當按鈕未熱或停用時，工具列控制項會使用此影像清單來顯示按鈕。
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- TB_GETIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685601"
---
# <a name="tb_getimagelist-message"></a>TB \_ GETIMAGELIST 訊息

抓取工具列控制項用來顯示其預設狀態之按鈕的影像清單。 當按鈕未熱或停用時，工具列控制項會使用此影像清單來顯示按鈕。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回影像清單的控制碼，如果未設定影像清單，則傳回 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





