---
title: 'LVM_SETITEMPOSITION 訊息 (Commctrl .h) '
description: 將專案移至清單視圖控制項中的指定位置 (必須是圖示或小圖示視圖) 。 您可以明確地傳送此訊息，或使用 ListView \_ SetItemPosition 宏來傳送。
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- LVM_SETITEMPOSITION message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843667"
---
# <a name="lvm_setitemposition-message"></a>LVM \_ SETITEMPOSITION 訊息

將專案移至清單視圖控制項中的指定位置 (必須是圖示或小圖示視圖) 。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetItemPosition**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單視圖專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會在 view 座標中指定專案左上角的新 x 位置。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會在 view 座標中指定專案左上角的新 y 位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

如果清單視圖控制項有 [**lvs) \_ AUTOARRANGE**](list-view-window-styles.md) 樣式，則會在設定專案的位置之後排列清單視圖控制項中的專案。

在 Windows Vista 上，將此訊息傳送至具有 [**lvs) \_ AUTOARRANGE**](list-view-window-styles.md) 樣式的清單視圖控制項不會執行任何動作，且傳回值為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

