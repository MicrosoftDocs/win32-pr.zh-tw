---
title: 'LVM_SCROLL 訊息 (Commctrl .h) '
description: 滾動清單視圖控制項的內容。 您可以明確地傳送此訊息，或使用 ListView \_ 滾動宏來傳送。
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- LVM_SCROLL message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465869"
---
# <a name="lvm_scroll-message"></a>LVM \_ 捲軸訊息

滾動清單視圖控制項的內容。 您可以明確地傳送此訊息，或使用 [**ListView \_ 滾動**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**Int** 類型的值，指定相對於清單視圖內容目前位置的水準滾動量（以圖元為單位）。 如果清單視圖控制項在清單視圖中，此值會無條件進位到構成整個資料行之最接近的圖元數目。

</dd> <dt>

*lParam* 
</dt> <dd>

**Int** 類型的值，指定垂直捲動的數量（以圖元為單位），相對於清單視圖內容的目前位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ;否則 **為 FALSE**。

## <a name="remarks"></a>備註

當清單視圖控制項位於報表檢視時，控制項只能以整行遞增的方式垂直捲動。 因此， *lParam* 參數將會舍入形成整行增量的最接近圖元數目。 例如，如果線條的高度為16圖元，而針對 *lParam* 傳遞的是8，則清單會以16圖元滾動 (1 行) 。 如果針對 *lParam* 傳遞7，此清單將會滾動 (0 行) 的0圖元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





