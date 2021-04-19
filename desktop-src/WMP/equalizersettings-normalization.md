---
title: EQUALIZERSETTINGS 正規化
description: 正規化屬性會指定或抓取值，指出是否已啟用正規化。
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS 正規化 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990146"
---
# <a name="equalizersettingsnormalization"></a>EQUALIZERSETTINGS 正規化

正規化 **屬性會** 指定或抓取值，指出是否已啟用正規化。

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                         |
|-------|-------------------------------------|
| true  | 已啟用正規化。           |
| false | 預設值。 正規化已停用。 |



 

## <a name="remarks"></a>備註

啟用正規化時，會將整個數位媒體檔案的音訊信號向上調整為最大值。 這可讓多個檔案在大約相同的磁片區上播放，而不需要進行磁片區調整。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EQUALIZERSETTINGS 元素**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationAverage**](equalizersettings-normalizationaverage.md)
</dt> <dt>

[**EQUALIZERSETTINGS.normalizationPeak**](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





