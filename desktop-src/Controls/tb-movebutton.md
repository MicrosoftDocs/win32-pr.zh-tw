---
title: 'TB_MOVEBUTTON 訊息 (Commctrl .h) '
description: 將按鈕從一個索引移至另一個索引。
ms.assetid: 030aedc5-2de5-4751-90b2-63794322f503
keywords:
- TB_MOVEBUTTON 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_MOVEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857592f852b21d656be2a4ad5b59f691db9ac391f66960b98a70db138ea69f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168038"
---
# <a name="tb_movebutton-message"></a>TB \_ MOVEBUTTON 訊息

將按鈕從一個索引移至另一個索引。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要移動之按鈕的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

以零為基底的索引，將會在其中移動按鈕。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)
</dt> </dl>

 

 





