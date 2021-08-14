---
title: 'TB_GETITEMRECT 訊息 (Commctrl .h) '
description: 抓取工具列中按鈕的周框。
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- TB_GETITEMRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6dbfa4c7e305c4e2dfe53b45edaac1d6601631c920fa266c64292fd7e6d97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829703"
---
# <a name="tb_getitemrect-message"></a>TB \_ GETITEMRECT 訊息

抓取工具列中按鈕的周框。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的按鈕索引，用來取得資訊。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收周框矩形的用戶端座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息不會針對其狀態設定為 [**TBSTATE \_ 隱藏**](toolbar-button-states.md) 值的按鈕，取得周框矩形。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

