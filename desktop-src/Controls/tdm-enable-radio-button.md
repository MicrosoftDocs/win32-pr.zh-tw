---
title: 'TDM_ENABLE_RADIO_BUTTON 訊息 (Commctrl .h) '
description: 啟用或停用工作對話方塊中的選項按鈕。
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- TDM_ENABLE_RADIO_BUTTON message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935006"
---
# <a name="tdm_enable_radio_button-message"></a>TDM \_ 啟用 \_ 單選 \_ 按鈕訊息

啟用或停用工作對話方塊中的選項按鈕。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

**Int** 值，指定要啟用或停用的選項按鈕的識別碼。

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



 

 





