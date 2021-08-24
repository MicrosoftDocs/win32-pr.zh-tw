---
description: 圖示檔可保存相同圖示影像的數種不同大小。
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: IconSize 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7323d9c3d8dc9bef1bfd4cd275a20dfcadaa3be946bc78fd358a2d6484db53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894198"
---
# <a name="iconsize-control-attribute"></a>IconSize 控制項屬性

圖示檔可保存相同圖示影像的數種不同大小。 這些位指定要載入之圖示影像的大小。 如果未設定任何位，則會載入第一個映射。 如果只設定 **msidbControlAttributesIconSize16** ，則會載入第一個16x16 映射。 如果只設定 **msidbControlAttributesIconSize32** ，則會載入第一個32x32 映射。 如果設定了 **msidbControlAttributesIconSize48** ，則會載入第一個48x48 映射。

## <a name="valid-controls"></a>有效的控制項

[CheckBox](checkbox-control.md)

[圖示](icon-control.md)

[按鈕](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 描述                          |
|---------|-------------|--------------------------------------|
| 2097152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| 4194304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 IconSize 位。

如果未設定 [FixedSize](fixedsize-control-attribute.md) 位，則會壓縮或延展載入的影像以符合圖示控制項。 如果已設定 [FixedSize](fixedsize-control-attribute.md) 位，且載入的影像小於圖示控制項，則圖片會以中央顯示在控制項內。 如果已設定 [FixedSize](fixedsize-control-attribute.md) 位，且載入的影像大於圖示控制項，則圖片會縮小以符合控制項。

請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。

 

 



