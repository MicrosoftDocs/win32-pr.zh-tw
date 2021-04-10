---
title: 'RB_GETBARINFO 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項及其所使用影像清單的相關資訊。
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- RB_GETBARINFO message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025281"
---
# <a name="rb_getbarinfo-message"></a>RB \_ GETBARINFO 訊息

抓取 Rebar 控制項及其所使用影像清單的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo)結構的指標，此結構會接收 Rebar 控制項資訊。 在傳送此訊息之前，您必須將此結構的 **cbSize** 成員設定為 **sizeof** (REBARINFO) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





