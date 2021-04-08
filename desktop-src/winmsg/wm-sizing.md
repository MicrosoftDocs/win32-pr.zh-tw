---
description: 傳送至使用者正在調整大小的視窗。 藉由處理此訊息，應用程式可以監視拖曳矩形的大小和位置，並視需要變更其大小或位置。
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: 'WM_SIZING 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693063"
---
# <a name="wm_sizing-message"></a>WM 重設 \_ 大小訊息

傳送至使用者正在調整大小的視窗。 藉由處理此訊息，應用程式可以監視拖曳矩形的大小和位置，並視需要變更其大小或位置。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要調整大小之視窗的邊緣。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                                                         | 意義                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <dt>**WMSZ \_底部**</dt> <dt>6</dt> </dl>                | 下邊緣<br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <dt>**WMSZ \_BOTTOMLEFT**</dt> <dt>7</dt> </dl>    | 左下角<br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <dt>**WMSZ \_BOTTOMRIGHT**</dt> <dt>8</dt> </dl> | 右下角<br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <dt>**WMSZ \_左方**</dt> <dt>1</dt> </dl>                      | 左邊緣<br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <dt>**WMSZ \_右**</dt> <dt>2</dt> </dl>                   | 右邊緣<br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <dt>**WMSZ \_前**</dt> <dt>3</dt>名 </dl>                         | 上邊緣<br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <dt>**WMSZ \_下拉式功能表**</dt> <dt>4</dt> </dl>             | 左上角<br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <dt>**WMSZ \_右上**</dt> <dt>5</dt> </dl>          | 右上角<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含拖曳矩形的螢幕座標。 若要變更拖曳矩形的大小或位置，應用程式必須變更此結構的成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LRESULT**

如果應用程式處理此訊息，則應該傳回 **TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**WM \_ 移動**](wm-moving.md)
</dt> <dt>

[**WM \_ 大小**](wm-size.md)
</dt> <dt>

**概念**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**矩形**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
