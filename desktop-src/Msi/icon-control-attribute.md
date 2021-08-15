---
description: 如果設定此位，則會將文字取代為圖示影像，而控制資料表中的文字資料行則是二進位資料表中的外鍵。
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Icon 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2caeb407b86b888a5dd3b1c08f16d0893233f82cec29b92519c267b286ea121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315118"
---
# <a name="icon-control-attribute"></a>Icon 控制項屬性

如果設定此位，則會將文字取代為圖示影像，而 [控制資料表](control-table.md) 中的文字資料行則是 [二進位資料表](binary-table.md)中的外鍵。

如果未設定此位，則會在 [控制資料表](control-table.md)的文字資料行中指定控制項中的文字。

## <a name="valid-controls"></a>有效的控制項

[CheckBox](checkbox-control.md)

[按鈕](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                       |
|---------|-------------|--------------------------------|
| 5242288 | 0x00080000  | **msidbControlAttributesIcon** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制 [資料表](control-table.md)中，于控制項記錄的 [屬性] 資料行中包含圖示位。

控制資料表中的文字資料行是用來當做 [二進位資料表](binary-table.md)的外鍵，因此控制項不能同時包含圖示影像和文字。

請勿同時設定圖示和 [點陣圖](bitmap-control-attribute.md) 位。

請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。

 

 



