---
title: 'TBM_SETBUDDY 訊息 (Commctrl .h) '
description: 將視窗指派為 [查看] 控制項的合作者視窗。 [並排顯示] 視窗會自動顯示在相對於控制項方向 (水準或垂直) 的位置。
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- TBM_SETBUDDY 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f2586c84740cb2d5e8b1f1aadfb910cd241270d3e18363accf1f166c3c35ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167184"
---
# <a name="tbm_setbuddy-message"></a>TBM \_ SETBUDDY 訊息

將視窗指派為 [查看] 控制項的合作者視窗。 [並排顯示] 視窗會自動顯示在相對於控制項方向 (水準或垂直) 的位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，指定要顯示好友視窗的位置。 這個值可以是下列其中一個值：



| 值                                                                                                                                | 意義                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**真**</dt> </dl>    | 如果 [對齊程式] 控制項使用 [ [**tb] \_ HORZ**](trackbar-control-styles.md) 樣式，則會在 [顯示] 的左邊顯示好友。 如果使用 [Tb] [**\_ 垂直**](trackbar-control-styles.md) 樣式，則會在 [顯示] 控制項上方顯示好友。<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**假**</dt> </dl> | 如果 [HORZ] 控制項使用 [ [**tb] \_**](trackbar-control-styles.md) 樣式，則會在 [顯示] 右邊顯示好友。 如果使用 [Tb] [**\_ 垂直**](trackbar-control-styles.md) 樣式，則會在 [顯示] 控制項下方顯示好友。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

將設定為 [處理常式] 控制項的合作者的視窗控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前指派給該位置之控制項的視窗控制碼。

## <a name="remarks"></a>備註

> [!Note]  
> 追蹤控制項最多可支援兩個好友視窗。 當您必須在控制項的每一端顯示文字或影像時，這項功能就很有用。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





