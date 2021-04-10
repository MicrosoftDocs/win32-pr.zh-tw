---
title: 'TB_COMMANDTOINDEX 訊息 (Commctrl .h) '
description: 針對與指定的命令識別碼相關聯的按鈕，取得以零為基底的索引。
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- TB_COMMANDTOINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0257f55e01db59f1d23d59583f1ef78f44b1dac1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106607"
---
# <a name="tb_commandtoindex-message"></a>TB \_ COMMANDTOINDEX 訊息

針對與指定的命令識別碼相關聯的按鈕，取得以零為基底的索引。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

與按鈕相關聯的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回按鈕的以零為基底的索引，如果指定的命令識別碼無效，則為-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





