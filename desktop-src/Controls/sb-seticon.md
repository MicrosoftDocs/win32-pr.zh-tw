---
title: 'SB_SETICON 訊息 (Commctrl .h) '
description: 設定狀態列中元件的圖示。
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- SB_SETICON message Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843996"
---
# <a name="sb_seticon-message"></a>SB \_ SETICON 訊息

設定狀態列中元件的圖示。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

將接收圖示之元件以零為起始的索引。 如果此參數為-1，則會假設狀態列為簡單的狀態列。

</dd> <dt>

*lParam* 
</dt> <dd>

要設定之圖示的控制碼。 如果這個值為 **Null**，則會從元件中移除圖示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

狀態列不會摧毀圖示。 呼叫應用程式負責追蹤和終結任何圖示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





