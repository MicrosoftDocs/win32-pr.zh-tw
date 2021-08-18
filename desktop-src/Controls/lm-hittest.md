---
title: 'LM_HITTEST 訊息 (Commctrl .h) '
description: 判斷使用者是否按一下指定的連結。
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- LM_HITTEST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 559ea1500c7270ece1785391777133bdaaeb1e95e5b01fa5ca7d4bb76e40f1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958370"
---
# <a name="lm_hittest-message"></a>LM \_ system.windows.media.visualtreehelper.hittest 訊息

判斷使用者是否按一下指定的連結。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須是 **Null**。</dd> <dt>

*lParam* 
</dt> <dd><a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a>結構的指標，要填入使用者所按下的連結相關資訊（如果有的話）。 </dd> </dl>

## <a name="return-value"></a>傳回值

如果使用者按一下連結， **則傳回 TRUE** ，否則傳回 **FALSE**。

## <a name="remarks"></a>備註

如果 **LM \_ system.windows.media.visualtreehelper.hittest** 訊息成功，系統會填入 [**LITEM. Ashraf**](/windows/win32/api/commctrl/ns-commctrl-litem) 和 **LITEM. szID**。 如果 **LM \_ system.windows.media.visualtreehelper.hittest** 訊息失敗，請勿假設 **LITEM** 中的任何資訊都有效。

> [!Note]  
> 若要使用此 API，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





