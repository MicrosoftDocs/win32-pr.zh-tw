---
title: 'DTM_GETIDEALSIZE 訊息 (Commctrl .h) '
description: 取得在不剪切的情況下顯示控制項所需的大小。 請明確地傳送此訊息，或使用 DateTime \_ GetIdealSize 宏。
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- DTM_GETIDEALSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a979883f431fea4627f52fe19c3716341e3f2328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187277"
---
# <a name="dtm_getidealsize-message"></a>DTM \_ GETIDEALSIZE 訊息

取得在不剪切的情況下顯示控制項所需的大小。 請明確地傳送此訊息，或使用 [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用。 必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

要接收理想大小的 [**大小**](/previous-versions//dd145106(v=vs.85)) 結構指標。 呼叫應用程式負責配置此結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

