---
title: 'BM_SETDONTCLICK 訊息 (Winuser .h) '
description: 設定選項按鈕上的旗標，此旗標會在 \_ 按鈕取得焦點時，控制 BN 按一下訊息的產生。
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- BM_SETDONTCLICK message Windows 控制項
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969959"
---
# <a name="bm_setdontclick-message"></a>BM \_ SETDONTCLICK 訊息

設定選項按鈕上的旗標，此旗標會在按鈕取得焦點時，控制 [BN \_ 按一下](bn-clicked.md) 訊息的產生。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

指定狀態的 **布林** 值。 **TRUE** 表示設定旗標，否則為 **FALSE**。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用。 必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



 

 





