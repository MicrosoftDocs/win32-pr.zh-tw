---
title: 'TB_SETHOTITEM 訊息 (Commctrl .h) '
description: TB_SETHOTITEM 訊息：設定工具列中的熱專案。
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90e5b38675d33a361857c4303fa2a89f22cff29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104176"
---
# <a name="tb_sethotitem-message"></a>TB \_ SETHOTITEM 訊息

設定工具列中的熱專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

將設為經常性存取之專案的索引。 如果這個值是-1，則沒有任何專案會是經常性的。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前熱專案的索引，如果沒有熱專案，則傳回-1。

## <a name="remarks"></a>備註

未針對沒有 [**TBSTYLE \_ 平面**](toolbar-control-and-button-styles.md) 樣式的工具列定義此訊息的行為。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





