---
title: 'TCM_HITTEST 訊息 (Commctrl .h) '
description: 判斷哪一個索引標籤（如果有的話）位於指定的畫面位置上。 您可以使用 TabCtrl System.windows.media.visualtreehelper.hittest 宏明確地傳送此訊息 \_ 。
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- TCM_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970446"
---
# <a name="tcm_hittest-message"></a>TCM \_ system.windows.media.visualtreehelper.hittest 訊息

判斷哪一個索引標籤（如果有的話）位於指定的畫面位置上。 您可以使用 [**TabCtrl \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo)結構的指標，指定要測試的螢幕位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回索引標籤的索引，如果沒有索引標籤位於指定的位置，則為-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





