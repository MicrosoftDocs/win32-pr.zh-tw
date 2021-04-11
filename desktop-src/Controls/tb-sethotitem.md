---
title: 'TB_SETHOTITEM 訊息 (Commctrl .h) '
description: 設定工具列中的熱專案。
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
ms.openlocfilehash: c477a445cb6aae78dd5d31e8d23b8ec3be8c61ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843980"
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



 

 





