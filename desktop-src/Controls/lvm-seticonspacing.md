---
title: 'LVM_SETICONSPACING 訊息 (Commctrl .h) '
description: 在具有 LVS) 圖示樣式的清單視圖控制項中，設定圖示之間的間距 \_ 。 您可以明確地傳送此訊息，或使用 ListView \_ SetIconSpacing 宏來傳送。
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- LVM_SETICONSPACING 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5897b0ca6aec7763cc24a0ea538f336e7a2f737f2ddc0e7cb52a2145e570db47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019171"
---
# <a name="lvm_seticonspacing-message"></a>LVM \_ SETICONSPACING 訊息

在具有 [**lvs) \_ 圖示**](list-view-window-styles.md) 樣式的清單視圖控制項中，設定圖示之間的間距。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定要在 X 軸上的圖示之間設定的距離（以圖元為單位）。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定要在 y 軸上的圖示之間設定的距離（以圖元為單位）。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **DWORD** 值，其中包含低字組中之前的 X 軸距離，以及高單字中先前的 y 軸距離。

## <a name="remarks"></a>備註

*LParam* 的值會相對於圖示點陣圖的左上角。 因此，若要在不重迭的圖示之間設定間距， *lParam* 值必須包含圖示的大小，以及圖示之間所需的空白空間量。 不包含圖示寬度的值會導致重迭。

定義圖示間距時， *lParam* 值必須設定為4或更大。 較小的值不會產生所需的版面配置。 若要將圖示重設為預設間距，請將 *lParam* 值設為-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

