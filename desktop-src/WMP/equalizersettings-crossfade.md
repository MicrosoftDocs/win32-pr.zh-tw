---
title: EQUALIZERSETTINGS.crossFade
description: CrossFade 屬性會指定或抓取值，指出是否已啟用交叉淡化。
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS. crossFade Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996494"
---
# <a name="equalizersettingscrossfade"></a>EQUALIZERSETTINGS.crossFade

**CrossFade** 屬性會指定或抓取值，指出是否已啟用交叉淡化。

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                      |
|-------|----------------------------------|
| true  | 啟用交叉淡化。           |
| false | 預設值。 停用交叉淡化已停用。 |



 

## <a name="remarks"></a>備註

交叉淡化是一種音訊處理功能，它會逐漸減少播放媒體專案結束時的音量，同時在最小磁片區上同時開始播放下一個媒體專案，並逐漸將它逐漸增加到一般磁片區。 第二個媒體專案開始與第一個媒體專案的結尾之間的重迭，是由 **crossFadeWindow** 屬性所指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EQUALIZERSETTINGS 元素**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





