---
title: 'TDM_ENABLE_BUTTON 訊息 (Commctrl .h) '
description: 啟用或停用工作對話方塊中的 [推送] 按鈕。
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- TDM_ENABLE_BUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106997046"
---
# <a name="tdm_enable_button-message"></a>TDM \_ 啟用 \_ 按鈕訊息

啟用或停用工作對話方塊中的 [推送] 按鈕。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

**Int** 值，指定要啟用或停用之推送按鈕的識別碼。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

指定按鈕狀態。 設定為0以停用按鈕;設定為非零以啟用按鈕。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





