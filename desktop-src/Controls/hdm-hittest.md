---
title: 'HDM_HITTEST 訊息 (Commctrl .h) '
description: 測試點以判斷哪個標頭專案（如果有的話）位於指定的點。
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- HDM_HITTEST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc219640d9dd9d5d9a4c9537169401f681e37660554266b3edd653365cf8cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544768"
---
# <a name="hdm_hittest-message"></a>HDM \_ system.windows.media.visualtreehelper.hittest 訊息

測試點以判斷哪個標頭專案（如果有的話）位於指定的點。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**HDHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo)結構的指標，其中包含要測試的位置，以及接收測試結果的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回位於指定位置之專案的索引（如果有的話），否則傳回1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





