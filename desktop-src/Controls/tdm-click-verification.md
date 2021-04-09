---
title: 'TDM_CLICK_VERIFICATION 訊息 (Commctrl .h) '
description: 模擬工作對話方塊的 [驗證] 核取方塊（如果有的話）。
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093800"
---
# <a name="tdm_click_verification-message"></a>TDM \_ CLICK \_ 驗證訊息

模擬工作對話方塊的 [驗證] 核取方塊（如果有的話）。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

**TRUE** 表示設定要檢查之核取方塊的狀態。 **FALSE** 表示將它設定為未核取。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

**TRUE** 表示將鍵盤焦點設定為核取方塊;否則 **為 FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





