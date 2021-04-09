---
title: 'EM_SETPALETTE 訊息 (Richedit .h) '
description: 變更 rich edit 控制項用於顯示視窗的調色板。
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- EM_SETPALETTE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026a0a85001818b6f69366e8dba80ef56a7a8f20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024996"
---
# <a name="em_setpalette-message"></a>EM \_ SETPALETTE 訊息

變更 rich edit 控制項用於顯示視窗的調色板。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

Rich edit 控制項所使用之新調色板的控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

Rich edit 控制項不會檢查新的調色板是否有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





