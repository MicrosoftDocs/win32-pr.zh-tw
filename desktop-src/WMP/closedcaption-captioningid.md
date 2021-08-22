---
title: ClosedCaption.captioningID
description: CaptioningID 屬性會指定或抓取顯示字幕的元素名稱。
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- ClosedCaption. captioningID Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da667e5479cc33312375920c1d573f0e2c19607b2399ff6f4fe34b130ca61e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580986"
---
# <a name="closedcaptioncaptioningid"></a>ClosedCaption.captioningID

**CaptioningID** 屬性會指定或抓取顯示字幕的元素名稱。

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

指定的元素名稱可以是網頁中的任何 HTML 專案，只要它支援 innerHTML 屬性即可。 如果網頁包含多個框架，元素名稱只能參考與播放機控制項相同框架中的元素。

**Windows Media Player 10** 行動裝置版：這個屬性是唯讀的，而且一律會傳回空字串。

## <a name="examples"></a>範例

下列 Microsoft JScript 範例使用 *ClosedCaption*。**captioningID** ，選擇用來顯示標題的網頁區域。 已建立兩個 HTML DIV 元素，分別具有 ID = CC1 和 ID = CC2。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption 物件**](closedcaption-object.md)
</dt> </dl>

 

 





