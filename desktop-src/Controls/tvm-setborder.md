---
title: 'TVM_SETBORDER 訊息 (Commctrl .h) '
description: 針對樹狀檢視控制項中的專案，設定框線的大小。 您可以使用 TreeView SetBorder 宏明確地傳送訊息 \_ 。
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- TVM_SETBORDER 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1c8cab133fb654e431638be96301325d68d9743109f84ed8def1ee9cc67c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669653"
---
# <a name="tvm_setborder-message"></a>TVM \_ SETBORDER 訊息

**適用于內部用途;不建議在應用程式中使用。**

針對樹狀檢視控制項中的專案，設定框線的大小。 您可以使用 [**TreeView \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) 宏明確地傳送訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

動作旗標。 這個參數可以是下列其中一個或多個值：



| 值                                                                                                                                                         | 意義                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <dt>**TVSBF \_ XBORDER**</dt> </dl> | 將指定的框線大小套用至樹狀檢視控制項中專案的左邊。 <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <dt>**TVSBF \_ YBORDER**</dt> </dl> | 將指定的框線大小套用至樹狀檢視控制項中的專案頂端。<br/>        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是指定左邊框線大小的 **簡短** 值（以圖元為單位）。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是指定上框線大小的 **簡短** 值（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含先前框線大小的 **長** 數值（以圖元為單位）。 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含水準框線的先前大小，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含垂直框線的先前大小。

## <a name="remarks"></a>備註

**安全性警告：** 使用此訊息可能會危害程式的安全性。

專案框線的設定只是為了間距之用。 成功的設定會觸發捲軸的重新計算。

未來的 Comctl32.dll 版本可能不支援此訊息。 此外，commctrl 中並未定義此訊息。 將下列定義新增至您應用程式的原始程式檔，以使用訊息：

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TreeView \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

