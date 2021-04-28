---
title: 'TB_SETHOTITEM2 訊息 (Commctrl .h) '
description: TB_SETHOTITEM2 訊息：設定工具列中的熱專案。
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7daf67839837adccfbec99bf03fc4dfff97738db
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104136"
---
# <a name="tb_sethotitem2-message"></a>TB \_ SETHOTITEM2 訊息

設定工具列中的熱專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

將設為經常性存取之專案的索引。 如果這個值是-1，則沒有任何專案會是經常性的。

</dd> <dt>

*lParam* 
</dt> <dd>HICF \_ xxx 旗標的組合。 請參閱 <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>。</dd> </dl>

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



 

 





