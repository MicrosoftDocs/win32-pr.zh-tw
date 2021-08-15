---
title: 畫筆旗標
description: 可以出現在 POINTER_PEN_INFO 結構的 penFlags 欄位中的值。
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: acc1afb1d490a1831fdb1ecd5a090e457bae77ae2f08a1b94cabc81d12dbde9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482403"
---
# <a name="pen-flags"></a>畫筆旗標

可以出現在 [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)結構的 **penFlags** 欄位中的值。

<dl> <dt>

<span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



沒有畫筆旗標。 此為預設值。


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



已按下 [圓筒] 按鈕。


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



畫筆已反轉。


</dt> </dl> </dd> <dt>

<span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



已按下橡皮擦按鈕。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[常數](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





