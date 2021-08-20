---
title: 'SB_SETTEXT 訊息 (Commctrl .h) '
description: 在狀態視窗的指定部分中設定文字。
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- SB_SETTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fcf0a7928e87cbc614a59dc64b433223afa97bbdac3f45f1635cb8cfe7b34a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408881"
---
# <a name="sb_settext-message"></a>SB \_ SETTEXT 訊息

在狀態視窗的指定部分中設定文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

低序位單字的 [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) 會指定要設定之元件的以零為起始的索引。 如果 **LOBYTE** 設定為 SB \_ SIMPLEID，則狀態視窗會假設為簡單模式狀態列，也就是只有一個部分的狀態列。

低序位字組的 [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) 會指定繪圖作業的型別。 此參數可以是下列其中一個值。

*WParam* 的高序位單字會被忽略。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <dt><strong>0</strong></dt> </dl></td>
<td>文字會以框線繪製，並顯示為低於視窗的平面。<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <dt><strong>SBT_NOBORDERS</strong></dt> </dl></td>
<td>不以框線繪製文字。<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <dt><strong>SBT_OWNERDRAW</strong></dt> </dl></td>
<td>文字是由父視窗繪製。 <br/>
<blockquote>
[!Note]<br />
簡單模式的狀態列不支援「擁有者繪圖」。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <dt><strong>SBT_POPOUT</strong></dt> </dl></td>
<td>文字會以框線繪製，並顯示在視窗的平面的上方。<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <dt><strong>SBT_RTLREADING</strong></dt> </dl></td>
<td>文字將會以相反方向顯示在父視窗中的文字。<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <dt><strong>SBT_NOTABPARSING</strong></dt> </dl></td>
<td>略過 Tab 字元。<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

指標，指向以 null 終止的字串，指定要設定的文字。 如果 *wParam* 是 SBT \_ OWNERDRAW，此參數代表32位的資料。 父視窗必須解讀資料，並在收到 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息時繪製文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

此訊息會使已變更視窗的部分失效，使其在視窗下一次收到 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息時顯示新的文字。

一般視窗會將文字從左至右顯示 (LTR) 。 Windows 可以進行 *鏡像*，以顯示如希伯來文或阿拉伯文等語言，由右至左 (RTL) 。 如果 \_ 設定了 SBT RTLREADING，則會從父視窗中的文字，以相反的方向讀取 *lParam* 字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **SB \_SETTEXTW** (Unicode) 和 **SB \_ SETTEXTA** (ANSI) <br/>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SB \_ GETTEXT**](sb-gettext.md)
</dt> </dl>

 

