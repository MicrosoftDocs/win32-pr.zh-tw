---
title: 'MCM_GETMINREQRECT 訊息 (Commctrl .h) '
description: 抓取在月曆控制項中顯示全月所需的最小大小。 您可以使用 MonthCal GetMinReqRect 宏明確地傳送此訊息 \_ 。
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- MCM_GETMINREQRECT message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464877"
---
# <a name="mcm_getminreqrect-message"></a>MCM \_ GETMINREQRECT 訊息

抓取在月曆控制項中顯示全月所需的最小大小。 您可以使用 [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收周框的資訊。 此參數必須是有效的位址，而且不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零和 *lParam* 接收適用的界限資訊。 否則，訊息會傳回零。

## <a name="remarks"></a>備註

月曆控制項的最小必要視窗大小取決於目前選取的字型、控制項樣式、系統計量和地區設定。 當應用程式變更任何會影響最小視窗大小的任何值，或處理 [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) 訊息時，它應該傳送 **MCM \_ GETMINREQRECT** 來判斷新的最小大小。

> [!Note]  
> **MCM \_ GETMINREQRECT** 所傳回的矩形不包含 "Today" 字串的寬度（如果有的話）。 如果未設定 [**MCS \_ NOTODAY**](month-calendar-control-styles.md) 樣式，您的應用程式也應該藉由傳送 [**MCM \_ GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) 訊息，來取得定義 "Today" 字串寬度的矩形。 使用兩個矩形中較大的，以確保不會裁剪 "Today" 字串。

 

*LParam* 所指向之結構的 **top** 和 **left** 成員永遠為零。 **右邊** 和 **底部** 的成員代表控制項所需的最小 *cx* 和 *cy* 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

