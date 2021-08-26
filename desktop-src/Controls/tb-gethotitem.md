---
title: 'TB_GETHOTITEM 訊息 (Commctrl .h) '
description: 抓取工具列中熱專案的索引。
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- TB_GETHOTITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f33566a586ceaa524f720a9d688897f132ee227950f1f786093150955eafa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918828"
---
# <a name="tb_gethotitem-message"></a>TB \_ GETHOTITEM 訊息

抓取工具列中熱專案的索引。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回熱專案的索引，如果沒有設定熱專案，則傳回-1。 沒有 [ [**TBSTYLE] \_ 平面**](toolbar-control-and-button-styles.md) 樣式的工具列控制項沒有熱專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





