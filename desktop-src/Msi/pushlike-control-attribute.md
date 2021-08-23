---
description: 如果已在核取方塊或選項按鈕群組上設定此位，則會使用 [按下] 按鈕的外觀來繪製按鈕，但其邏輯會維持不變。 如果未設定位，則會以其一般樣式來繪製控制項。
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: PushLike 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab516038538849ac97d273d5fb3ede2be5be17417c48cf9a5624af98789867c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692477"
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

 

 



