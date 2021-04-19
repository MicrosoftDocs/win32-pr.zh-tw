---
description: 如果已在核取方塊或選項按鈕群組上設定此位，則會使用 [按下] 按鈕的外觀來繪製按鈕，但其邏輯會維持不變。 如果未設定位，則會以其一般樣式來繪製控制項。
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: PushLike 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839adfceb0484bc908b8c8c6d14616cfd03acdb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974441"
---
# <a name="pushlike-control-attribute"></a>PushLike 控制項屬性

如果已在核取方塊或選項按鈕群組上設定此位，則會使用 [按下] 按鈕的外觀來繪製按鈕，但其邏輯會維持不變。 如果未設定位，則會以其一般樣式來繪製控制項。

## <a name="valid-controls"></a>有效的控制項

[CheckBox](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                           |
|---------|-------------|------------------------------------|
| 131072  | 0x00020000  | **msidbControlAttributesPushLike** |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 PushLike 位。

請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



