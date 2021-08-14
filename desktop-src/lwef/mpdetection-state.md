---
title: 'MPDETECTION_STATE 列舉 (MpClient .h) '
description: 目前偵測到之威脅的狀態。
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE 列舉舊版 Windows 環境功能
- PMPDETECTION_STATE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0443e0c47eef4d4943d39bd671c28c19db0ff5e1fbe79e5af8d034603b1ab78d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883515"
---
# <a name="mpdetection_state-enumeration"></a>MPDETECTION \_ 狀態列舉

目前偵測到之威脅的狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**MPDETECTION \_ 狀態 \_ 不明**
</dt> <dd>

處於錯誤狀態。

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION \_ 狀態為 \_ 主動**
</dt> <dd>

作用中的威脅。

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION \_ 狀態 \_ 已完成**
</dt> <dd>

暫止24小時到已清除的移動。

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**MPDETECTION \_ 狀態 \_ 其他 \_ 動作**
</dt> <dd>

需要額外的動作。

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**MPDETECTION \_ 狀態 \_ 失敗**
</dt> <dd>

非重大補救失敗。

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION \_ 狀態 \_ 嚴重 \_ 失敗**
</dt> <dd>

重大補救失敗。

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**已 \_ 清除 MPDETECTION 狀態 \_**
</dt> <dd>

威脅不會顯示在狀態查詢中，只會顯示在歷程記錄中。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





