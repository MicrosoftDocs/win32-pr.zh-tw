---
title: 'TDM_SET_PROGRESS_BAR_STATE 訊息 (Commctrl .h) '
description: 在工作對話方塊中設定進度列的狀態。
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- TDM_SET_PROGRESS_BAR_STATE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3be7432ac3a93af4f27fe9b06dced50fc6c77c0176c3bff7419cf15f2c73ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104528"
---
# <a name="tdm_set_progress_bar_state-message"></a>TDM \_ 設定 \_ 進度 \_ 列 \_ 狀態訊息

在工作對話方塊中設定進度列的狀態。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

指定進度列狀態的 **int** 。 此參數可以是下列其中一個值。



| 值                                                                                                                                                   | 意義                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ 正常**</dt> </dl> | 將進度列設定為正常狀態。<br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST 已 \_ 暫停**</dt> </dl>    | 將進度列設定為暫停狀態。<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**PBST \_ 錯誤**</dt> </dl>    | 將進度列設定為錯誤狀態。<br/>   |



 

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零。

如果此函式失敗，則傳回值為零。 若要取得擴充的錯誤資訊，請呼叫 GetLastError。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





