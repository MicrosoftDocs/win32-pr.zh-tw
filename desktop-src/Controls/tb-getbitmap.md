---
title: 'TB_GETBITMAP 訊息 (Commctrl .h) '
description: 抓取與工具列中的按鈕相關聯的點陣圖索引。
ms.assetid: 64878cca-7d71-48ad-b2ed-d2bdc3067592
keywords:
- TB_GETBITMAP message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771073b67b1421a5d9bda9d162bc234400c85885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935158"
---
# <a name="tb_getbitmap-message"></a>TB \_ GETBITMAP 訊息

抓取與工具列中的按鈕相關聯的點陣圖索引。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取出其點陣圖索引之按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回點陣圖的索引，否則為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





