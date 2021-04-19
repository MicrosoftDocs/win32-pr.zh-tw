---
description: 如果已在下拉式方塊上設定 ComboList 控制項位，則會以靜態文字欄位取代編輯欄位。 這可防止使用者輸入新的值，而且需要使用者只選擇其中一個預先定義的值。
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: ComboList 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990357"
---
# <a name="combolist-control-attribute"></a>ComboList 控制項屬性

如果已在下拉式方塊上設定 ComboList 控制項位，則會以靜態文字欄位取代編輯欄位。 這可防止使用者輸入新的值，而且需要使用者只選擇其中一個預先定義的值。

如果未設定此位，下拉式方塊就會有編輯欄位。

## <a name="valid-controls"></a>有效的控制項

[ComboBox](combobox-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | Description                     |
|---------|-------------|---------------------------------|
| 131072  | 0x00020000  | msidbControlAttributesComboList |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 ComboList 位。

請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。

 

 



