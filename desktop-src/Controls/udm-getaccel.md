---
title: 'UDM_GETACCEL 訊息 (Commctrl .h) '
description: 抓取上下按鈕控制項的加速資訊。
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464653"
---
# <a name="udm_getaccel-message"></a>UDM \_ GETACCEL 訊息

抓取上下按鈕控制項的加速資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*LParam* 所指定陣列中的元素數目。

</dd> <dt>

*lParam* 
</dt> <dd>

接收加速資訊之 [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) 結構陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是目前為控制項設定的快速鍵數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**UDM \_ SETACCEL**](udm-setaccel.md)
</dt> </dl>

 

 





