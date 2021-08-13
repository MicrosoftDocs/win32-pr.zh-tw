---
description: 如果設定點陣圖控制項位，則會以點陣圖影像取代控制項中的文字。 控制資料表中的文字資料行是二進位資料表中的外鍵。
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Bitmap 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2cd7ea8186d1ed16de71ae9974bb67a082142ed3e921d023ad905d4f47bbc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638737"
---
# <a name="bitmap-control-attribute"></a>Bitmap 控制項屬性

如果設定點陣圖控制項位，則會以點陣圖影像取代控制項中的文字。 [控制資料表](control-table.md)中的文字資料行是[二進位資料表](binary-table.md)中的外鍵。

如果未設定此位，則會在 [控制資料表](control-table.md)的文字資料行中指定控制項中的文字。

## <a name="valid-controls"></a>有效的控制項

[CheckBox](checkbox-control.md)

 

[按鈕](pushbutton-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesBitmap** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制 [資料表](control-table.md)中，于控制項記錄的 [屬性] 資料行中包含點陣圖位。

控制資料表中的文字資料行是用來當做 [二進位資料表](binary-table.md)的外鍵，因此控制項不能同時包含圖示影像和文字。

請勿同時設定 [圖示](icon-control-attribute.md) 和點陣圖位。

請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。

 

 



