---
title: 'UDM_SETACCEL 訊息 (Commctrl .h) '
description: 設定上下按鈕控制項的加速。
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025493"
---
# <a name="udm_setaccel-message"></a>UDM \_ SETACCEL 訊息

設定上下按鈕控制項的加速。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*AAccels* 所指定的 [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)結構數目。

</dd> <dt>

*lParam* 
</dt> <dd>

[**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)結構陣列的指標，其中包含加速資訊。 元素應以每個 **nSec** 成員的遞增順序排序。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**UDM \_ GETACCEL**](udm-getaccel.md)
</dt> </dl>

 

 





