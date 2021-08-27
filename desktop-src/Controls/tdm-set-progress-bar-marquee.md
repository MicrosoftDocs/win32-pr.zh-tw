---
title: 'TDM_SET_PROGRESS_BAR_MARQUEE 訊息 (Commctrl .h) '
description: 在 [工作] 對話方塊中啟動和停止捲軸顯示進度列，並設定字幕的速度。
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- TDM_SET_PROGRESS_BAR_MARQUEE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b92816b70e683b9f58e0de2247b2710da38bee891caa39d9026fc342168c6be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060648"
---
# <a name="tdm_set_progress_bar_marquee-message"></a>TDM \_ 設定 \_ 進度 \_ 列 \_ 捲軸訊息

在 [工作] 對話方塊中啟動和停止捲軸顯示進度列，並設定字幕的速度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

**布林** 值，指出是否要開啟或關閉字幕。 使用 **TRUE** 來開啟字幕顯示，或使用 **FALSE** 關閉。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

指定字幕動畫更新之間時間（以毫秒為單位）的 **UINT** 。 如果此參數為零，則會每隔30毫秒更新字幕動畫。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

如需捲軸模式的詳細資訊，請參閱 [進度列控制項](progress-bar-control.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





