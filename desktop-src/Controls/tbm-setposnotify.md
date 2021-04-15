---
title: 'TBM_SETPOSNOTIFY 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的目前邏輯位置。
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636a2add9f13470a89b312450f1a3dcbc185be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464772"
---
# <a name="tbm_setposnotify-message"></a>TBM \_ SETPOSNOTIFY 訊息

設定捲軸中滑杆的目前邏輯位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

wParam 未使用。

</dd> <dt>

*lParam* 
</dt> <dd>

滑杆的新邏輯位置。 有效的邏輯位置是在最小至最大滑杆位置的最小值範圍中的整數值。 如果這個值超出控制項的最大和最小範圍，則會將位置設定為最大值或最小值。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

呼叫 **TBM \_ SETPOSNOTIFY** 將會設定像 [**TBM \_ SETPOS**](tbm-setpos.md) 一樣的 [顯示] 滑杆位置，但它也會導致資訊提示透過 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息來通知其父系移動。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





