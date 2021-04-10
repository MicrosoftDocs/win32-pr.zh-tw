---
description: 如果設定此位，則會以指定的順序顯示控制項中所列的專案。 如果未設定位，專案會依字母順序顯示。
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: 排序的控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026100"
---
# <a name="sorted-control-attribute"></a>排序的控制項屬性

如果設定此位，則會以指定的順序顯示控制項中所列的專案。 如果未設定位，專案會依字母順序顯示。

## <a name="valid-controls"></a>有效的控制項

[ComboBox](combobox-control.md)

 

[ListBox](listbox-control.md)

 

[ListView 控制項](listview-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                         |
|---------|-------------|----------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesSorted** |



 

## <a name="remarks"></a>備註

若要排序下拉式 [方塊中的專案，請](combobox-control.md)在 [控制資料表](control-table.md) 的 [屬性] 資料行中包含已排序的位，並在 [ComboBox 資料表](combobox-table.md)的 [順序] 資料行中指定專案順序。

若要排序 [ListBox](listbox-control.md)中的專案，請在 [控制資料表](control-table.md) 的 [屬性] 資料行中包含已排序的位，並在 [ComboBox 資料表](combobox-table.md)的 [順序] 資料行中指定專案順序。

若要排序 [ListView](listview-control.md)中的專案，請在 [控制資料表](control-table.md) 的 [屬性] 資料行中包含已排序的位，並在 [ComboBox 資料表](combobox-table.md)中指定專案的順序。

請參閱 [控制項屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



