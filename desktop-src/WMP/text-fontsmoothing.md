---
title: FontSmoothing
description: FontSmoothing 屬性會指定或抓取值，指出是否已啟用字型平滑處理。
ms.assetid: bd6f0468-285e-44b3-a5e8-361744c5ce4a
keywords:
- FontSmoothing Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.fontSmoothing
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcdf285572b4edda0f514cb3519b6953f9e94677
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977616"
---
# <a name="textfontsmoothing"></a>FontSmoothing

**FontSmoothing** 屬性會指定或抓取值，指出是否已啟用字型平滑處理。

``` syntax
        elementID.fontSmoothing
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                          |
|-------|--------------------------------------|
| true  | 啟用字型凹凸貼圖。           |
| false | 預設值。 字型平滑處理已停用。 |



 

## <a name="remarks"></a>備註

字型平滑處理會使用作業系統的消除鋸齒功能。 如果已啟用字型凹凸貼圖，而且作業系統支援消除鋸齒，Windows Media Player 會嘗試將文字平滑。 並非所有字型都支援消除鋸齒。 Windows Media Player 10 使用 Windows XP ClearType 消除鋸齒方法。

-   **警告** 透明色彩的字型平滑化可能會導致透明色彩混合成字元。 如果文字會顯示在透明上，則不建議使用 **fontSmoothing** 。

如需說明如何使用 **TEXT** 元素屬性的範例，請參閱 [value](text-value.md)屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TEXT 元素**](text-element.md)
</dt> </dl>

 

 





