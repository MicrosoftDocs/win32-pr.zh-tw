---
title: 'TB_GETIDEALSIZE 訊息 (Commctrl .h) '
description: 取得工具列的理想大小。
ms.assetid: d3b5ea4d-fd80-4f07-be4f-89b53a8bdf4d
keywords:
- TB_GETIDEALSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b8701a4f4debcfb8e43f37068e7e7a4ef4f11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024722"
---
# <a name="tb_getidealsize-message"></a>TB \_ GETIDEALSIZE 訊息

取得工具列的理想大小。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>**布林** 值，指出是否要取出工具列的理想高度或寬度。 您可以使用 **TRUE** 來取得理想的高度， **FALSE** 以抓取理想的寬度。</dd> <dt>

*lParam* 
</dt> <dd>

[**大小**](/previous-versions//dd145106(v=vs.85))結構的指標，該結構會接收所有按鈕的顯示高度或寬度。 如果 *wParam* 為 **TRUE**，則只有 **cy** 成員 (height) 有效。 如果 *wParam* 為 **FALSE**，則只有 **cx** 成員 (寬度) 有效。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

