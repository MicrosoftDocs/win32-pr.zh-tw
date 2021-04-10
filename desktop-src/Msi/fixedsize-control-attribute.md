---
description: 如果設定了 FixedSize 控制項位，則圖片會在控制項中裁剪或置中，而不會變更其形狀或大小。
ms.assetid: fb1ef0ba-5183-4708-a47d-26c83584df6c
title: FixedSize 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee044860b79e56998da68dc6ddf4926e9115ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690248"
---
# <a name="fixedsize-control-attribute"></a>FixedSize 控制項屬性

如果設定了 FixedSize 控制項位，則圖片會在控制項中裁剪或置中，而不會變更其形狀或大小。

如果未設定此位，則會將圖片伸展以符合控制項。

## <a name="valid-controls"></a>有效的控制項

[點陣圖](bitmap-control.md)

[CheckBox](checkbox-control.md)

[圖示](icon-control.md)

[按鈕](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                            |
|---------|-------------|-------------------------------------|
| 1048576 | 0x00100000  | **msidbControlAttributesFixedSize** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 FixedSize 位。

如果沒有設定[點陣圖](bitmap-control-attribute.md)或[圖示](icon-control-attribute.md)，則設定 FixedSize 位不會影響[核取方塊](checkbox-control.md)、[按鈕](pushbutton-control.md)或[RadioButtonGroup](radiobuttongroup-control.md) 。

如果未設定 [IconSize](iconsize-control-attribute.md) 位，則設定 FixedSize 位不會影響圖示控制項或與圖示相關聯的按鍵。

請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。

 

 



