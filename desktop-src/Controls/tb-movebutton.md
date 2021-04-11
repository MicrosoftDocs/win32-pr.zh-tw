---
title: 'TB_MOVEBUTTON 訊息 (Commctrl .h) '
description: 將按鈕從一個索引移至另一個索引。
ms.assetid: 030aedc5-2de5-4751-90b2-63794322f503
keywords:
- TB_MOVEBUTTON message Windows 控制項
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
ms.openlocfilehash: 8dac4cd303e895998b12e710910432ba2c38b230
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105047"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TB \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)
</dt> </dl>

 

 





