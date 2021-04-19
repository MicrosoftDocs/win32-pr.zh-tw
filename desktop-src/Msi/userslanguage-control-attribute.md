---
description: 如果設定此位旗標，則會使用使用者的預設 UI 字碼頁來建立字型。 如果未設定位旗標，則會使用資料庫字碼頁來建立字型。
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: UsersLanguage 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977285"
---
# <a name="userslanguage-control-attribute"></a>UsersLanguage 控制項屬性

如果設定此位旗標，則會使用使用者的預設 UI 字碼頁來建立字型。 如果未設定位旗標，則會使用資料庫字碼頁來建立字型。

## <a name="valid-controls"></a>有效的控制項

[Text](text-control.md)

 

[ListBox](listbox-control.md)

 

[ComboBox](combobox-control.md)

## <a name="value"></a>值



| Decimal | 十六進位 | 常數                                |
|---------|-------------|-----------------------------------------|
| 1048576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

## <a name="remarks"></a>備註

這個控制項屬性可以用來顯示使用者已在 [編輯](edit-control.md) 或 [PathEdit](pathedit-control.md) 控制項中輸入的文字。

Edit control、PathEdit control、 [DirectoryList control](directorylist-control.md) 和 [DirectoryCombo control](directorycombo-control.md) 一律會使用使用者預設 UI 字碼頁中所建立的字型。 如果作業系統上已安裝其他語言，這可能會造成問題。 在此情況下，電腦上的字型可能無法以新增的語言呈現所有的字元。 若要判斷可以使用的字型，請查閱 **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ FontLink \\ SystemLink** 中的值。

如需詳細資訊，請參閱 [控制屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



