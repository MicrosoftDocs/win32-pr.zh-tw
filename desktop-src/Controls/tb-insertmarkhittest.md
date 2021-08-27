---
title: 'TB_INSERTMARKHITTEST 訊息 (Commctrl .h) '
description: 抓取工具列中某個點的插入標記資訊。
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- TB_INSERTMARKHITTEST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc231b915d6d71cc22ee3cd98b1c6dd602451cc3c70d2153ba1bee8a0d55657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061358"
---
# <a name="tb_insertmarkhittest-message"></a>TB \_ INSERTMARKHITTEST 訊息

抓取工具列中某個點的插入標記資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，其中包含點擊測試座標（相對於工具列的工作區）。

</dd> <dt>

*lParam* 
</dt> <dd>

[**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark)結構的指標，此結構會接收插入標記資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果點是插入號，則會傳回非零，否則會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

