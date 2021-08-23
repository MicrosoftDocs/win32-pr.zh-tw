---
title: 'TB_SETDRAWTEXTFLAGS 訊息 (Commctrl .h) '
description: 設定工具列的文字繪圖旗標。
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- TB_SETDRAWTEXTFLAGS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 849bbb0e661c9e8afe246894d2d2f59d99d15a3f096ad2295a7018cf3df26ca4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119543878"
---
# <a name="tb_setdrawtextflags-message"></a>TB \_ SETDRAWTEXTFLAGS 訊息

設定工具列的文字繪圖旗標。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

在 DrawText 中指定的一或多個 DT \_ 旗標，表示在繪製 [](/windows/desktop/api/winuser/nf-winuser-drawtext)文字時，將使用 *lParam* 中的哪個位。

</dd> <dt>

*lParam* 
</dt> <dd>

在 DrawText 中指定的一或多個 DT \_ 旗標，指出按鈕文字的繪製方式。 [](/windows/desktop/api/winuser/nf-winuser-drawtext) 此值會在繪製按鈕文字時傳遞至 **DrawText** 函式。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的文字繪圖旗標。

## <a name="remarks"></a>備註

*WParam* 參數可讓您指定在繪製文字時要使用的旗標，即使這些旗標已關閉也是一樣。 例如，如果您不想要在 \_ 繪製文字時使用 dt center 旗標，您可以將 dt \_ center 旗標新增至 *wParam* ，而不要 \_ 在 *lParam* 中指定 dt center 旗標。 這可防止控制項將 DT \_ CENTER 旗標傳遞給 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

