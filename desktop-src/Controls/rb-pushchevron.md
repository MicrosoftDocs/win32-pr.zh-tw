---
title: 'RB_PUSHCHEVRON 訊息 (Commctrl .h) '
description: 傳送至 Rebar 控制項以程式設計方式推送燕形。
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON message Windows 控制項
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09e558d5574d4fd28cf01e9794657556dda4ae8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508907"
---
# <a name="rb_pushchevron-message"></a>RB \_ PUSHCHEVRON 訊息

傳送至 Rebar 控制項以程式設計方式推送燕形。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的範圍索引，其中的上推線會被推送。

</dd> <dt>

*lParam* 
</dt> <dd>

應用程式定義的32位值。 它會傳回給應用程式，做為與 [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md)通知一起傳遞之 [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron)結構的 **lParamNM** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="remarks"></a>備註

傳送此訊息時，Rebar 控制項會將 [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) 通知碼傳送給應用程式，提示它顯示箭號功能表。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





