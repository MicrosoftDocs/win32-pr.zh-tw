---
title: 'EM_SETSCROLLPOS 訊息 (Richedit .h) '
description: 將 rich edit 控制項的內容滾動至指定的點。
ms.assetid: 9ec514a4-97b1-44ab-b2ca-973b1f6fc404
keywords:
- EM_SETSCROLLPOS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d86609c1b3f4b04ade24e5ea2f3343c367bbad0a52b8e07be7c18b2282536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412333"
---
# <a name="em_setscrollpos-message"></a>EM \_ SETSCROLLPOS 訊息

將 rich edit 控制項的內容滾動至指定的點。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，指定檔之虛擬文字空間中的點（以圖元為單位）。 檔將會被滾動，直到這個點位於 [編輯] 控制項視窗的左上角。 如果您想要變更視圖，讓視圖的左上角是兩行向下，而左邊緣有一個字元。 您會傳遞 (7，22) 的點。

Rich edit 控制項會檢查 x 和 y 座標，並視需要進行調整，以便在頂端顯示完整的行。 它也可確保文字永遠不會從 view 矩形中完整地滾動。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息一律會傳回1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> </dl>

 

