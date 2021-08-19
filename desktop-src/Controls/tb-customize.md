---
title: 'TB_CUSTOMIZE 訊息 (Commctrl .h) '
description: 顯示 [自訂工具列] 對話方塊。
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- TB_CUSTOMIZE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c4fe1cba535903ff1e60804ee6d4ec5743f5d3726212f9aca16742a40913b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957927"
---
# <a name="tb_customize-message"></a>TB \_ 自訂訊息

顯示 [ **自訂工具列** ] 對話方塊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 工具列必須處理 [TBN \_ QUERYINSERT](tbn-queryinsert.md) 和 [TBN \_ QUERYDELETE](tbn-querydelete.md) 通知，才能顯示 [ **自訂工具列** ] 對話方塊。 如果工具列沒有處理這些通知，則 **TB \_ 自訂** 不會有任何作用。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





