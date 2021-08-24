---
title: 'TTM_ADJUSTRECT 訊息 (Commctrl .h) '
description: 從視窗矩形計算工具提示控制項的文字顯示矩形，或從顯示指定的文字顯示矩形所需的工具提示視窗矩形。
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- TTM_ADJUSTRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba5a6719bcbd820d94b6d736a12644f8b2539cc81064f942616c62bce55823f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769528"
---
# <a name="ttm_adjustrect-message"></a>TTM \_ ADJUSTRECT 訊息

從視窗矩形計算工具提示控制項的文字顯示矩形，或從顯示指定的文字顯示矩形所需的工具提示視窗矩形。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，指定要執行的作業。 若為 **TRUE**，則會使用 *lParam* 來指定文字顯示矩形，並接收對應的視窗矩形。 如果為 **FALSE**，則會使用 *lParam* 來指定視窗矩形，並接收對應的文字顯示矩形。

</dd> <dt>

*lParam* 
</dt> <dd>

**矩形** 結構，用來保存工具提示視窗矩形或文字顯示矩形。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已成功調整矩形，則傳回非零值，如果發生錯誤則傳回零。

## <a name="remarks"></a>備註

當您想要使用工具提示控制項來顯示通常會截斷之字串的完整文字時，此訊息特別有用。 它通常會與 listview 和 treeview 控制項搭配使用。 您通常會傳送此訊息以回應 [TTN \_ 顯示](ttn-show.md) 通知程式碼，讓您可以正確定位工具提示控制項。

工具提示視窗矩形比用來限定工具提示字串的文字顯示矩形稍微大一點。 視窗原點也會從文字顯示矩形的原點位移和左邊。 若要定位文字顯示矩形，您必須計算對應的視窗矩形，然後使用該矩形來定位工具提示。 **TTM \_ADJUSTRECT** 會為您處理此計算。

如果您將 *wParam* 設為 **TRUE**， **TTM \_ ADJUSTRECT** 會採用所需工具提示文字顯示矩形的大小和位置，並傳回在指定的位置中顯示文字所需的工具提示視窗大小和位置。 如果您將 *wParam* 設定為 **FALSE**，您可以指定工具提示視窗矩形， **TTM \_ ADJUSTRECT** 將會傳回其文字矩形的大小和位置。

下列程式碼片段說明如何使用 **TTM \_ ADJUSTRECT** 訊息來定位工具提示控制項，以顯示控制項字串的完整文字來取代截斷的字串。 應用程式定義的 **GetMyItemRect** 函式會傳回在截斷的字串上直接顯示工具提示文字所需的文字矩形。 如何執行此函式的詳細資料將取決於特定的控制項。 **TTM \_ADJUSTRECT** 用來將此文字矩形傳送至工具提示控制項。 它會傳回適當大小和定位的視窗矩形，然後用來定位工具提示視窗。


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





