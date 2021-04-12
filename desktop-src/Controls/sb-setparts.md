---
title: 'SB_SETPARTS 訊息 (Commctrl .h) '
description: 設定狀態視窗中的部分數目，以及每個元件右邊緣的座標。
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS message Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509015"
---
# <a name="sb_setparts-message"></a>SB \_ SETPARTS 訊息

設定狀態視窗中的部分數目，以及每個元件右邊緣的座標。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要設定的部分數目 (不能大於 256) 。

</dd> <dt>

*lParam* 
</dt> <dd>

整數陣列的指標。 在 *wParam* 中指定的元素數目。 每個元素會指定相對應元件右邊緣的位置（以客戶座標為單位）。 如果元素為-1，對應元件的右邊緣會延伸至視窗的框線。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





