---
title: 'EM_SETUNDOLIMIT 訊息 (Richedit .h) '
description: 設定可在 rich edit 控制項的復原佇列中儲存的動作數目上限。
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- EM_SETUNDOLIMIT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771e339e38437ea0299e5da6120fa555fd26148f72ff7da4e0287ed46cc4ad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697518"
---
# <a name="em_setundolimit-message"></a>EM \_ SETUNDOLIMIT 訊息

設定可在 rich edit 控制項的復原佇列中儲存的動作數目上限。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定可儲存在復原佇列中的動作數目上限。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 rich edit 控制項的新復原動作最大數目。 如果記憶體有限，則這個值可能小於 *wParam* 。

## <a name="remarks"></a>備註

根據預設，復原佇列中的動作數目上限為100。 如果您增加此數目，則必須有足夠的可用記憶體來容納新的數位。 為了達到較佳的效能，請將限制設定為最小的可能值。

將 [限制] 設定為 [零] 會停用 **復原** 功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ CANREDO**](em-canredo.md)
</dt> <dt>

[**EM \_ GETREDONAME**](em-getredoname.md)
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ 重做**](em-redo.md)
</dt> <dt>

[**EM \_ 復原**](em-undo.md)
</dt> </dl>

 

 





