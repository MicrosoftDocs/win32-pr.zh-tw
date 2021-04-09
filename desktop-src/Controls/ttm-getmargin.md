---
title: 'TTM_GETMARGIN 訊息 (Commctrl .h) '
description: 抓取工具提示視窗的頂端、左方、底端和右邊界設定。 邊界是工具提示視窗框線和工具提示視窗內所含文字之間的距離（以圖元為單位）。
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- TTM_GETMARGIN message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934397"
---
# <a name="ttm_getmargin-message"></a>TTM \_ GETMARGIN 訊息

抓取工具提示視窗的頂端、左方、底端和右邊界設定。 邊界是工具提示視窗框線和工具提示視窗內所含文字之間的距離（以圖元為單位）。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收邊界資訊。 **矩形** 結構的成員不會定義周框。 針對此訊息的目的，結構成員會以下面方式解讀：



| 值                                                                                                                                   | 意義                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**top**</dt> </dl>          | 上方框線和工具提示文字頂端之間的距離（以圖元為單位）。<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**離開**</dt> </dl>       | 工具提示文字的左邊框線和左邊緣之間的距離（以圖元為單位）。<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**底部**</dt> </dl> | 下方框線和工具提示文字底端之間的距離（以圖元為單位）。<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**對**</dt> </dl>    | 工具提示文字右框線和右端之間的距離（以圖元為單位）。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="remarks"></a>備註

當您建立工具提示控制項時，四個邊界都會預設為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TTM \_ SETMARGIN**](ttm-setmargin.md)
</dt> </dl>

 

