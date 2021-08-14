---
title: 'TB_SETCMDID 訊息 (Commctrl .h) '
description: 設定工具列按鈕的命令識別碼。
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- TB_SETCMDID 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539fb03899a6a763a94a7cd2fd1b7e8be071f04e26e21f19e9ff53640b87be1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167603"
---
# <a name="tb_setcmdid-message"></a>TB \_ SETCMDID 訊息

設定工具列按鈕的命令識別碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要設定其命令識別碼之按鈕的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

命令識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





