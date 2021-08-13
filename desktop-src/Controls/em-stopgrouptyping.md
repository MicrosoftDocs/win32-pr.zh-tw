---
title: 'EM_STOPGROUPTYPING 訊息 (Richedit .h) '
description: 停止 rich edit 控制項，使其無法將其他輸入動作收集到目前的復原動作。 控制項會將下一個輸入動作（如果有的話）儲存至復原佇列中的新動作。
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- EM_STOPGROUPTYPING 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e62a5d652218b24240ce612851c4c08e335b31230532bc778bb44c5d7e74854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672276"
---
# <a name="em_stopgrouptyping-message"></a>EM \_ STOPGROUPTYPING 訊息

停止 rich edit 控制項，使其無法將其他輸入動作收集到目前的復原動作。 控制項會將下一個輸入動作（如果有的話）儲存至復原佇列中的新動作。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值為零。 此訊息無法失敗。

## <a name="remarks"></a>備註

Rich edit 控制項會將連續的輸入動作（包括使用 **倒退鍵** 刪除的字元）分組成單一復原動作，直到發生下列其中一個事件為止：

-   控制項收到 **EM \_ STOPGROUPTYPING** 訊息。
-   控制項失去焦點。
-   使用者可以使用方向鍵或按一下滑鼠來移動目前的選取範圍。
-   使用者按下 **Delete** 鍵。
-   使用者執行任何其他動作，例如 **不包含輸入** 的貼上作業。

您可以傳送 **EM \_ STOPGROUPTYPING** 訊息，將連續的輸入動作分成較小的復原群組。 例如，您可以在每個字元之後或每個斷字字元之後傳送 **EM \_ STOPGROUPTYPING** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ 復原**](em-undo.md)
</dt> </dl>

 

 





