---
title: 選取子物件
description: 用戶端會呼叫 IAccessible accSelect 方法，以修改物件中子系之間的選取範圍或鍵盤焦點。 以呼叫指定的 SELFLAG 常數會定義要執行的作業。
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc15ab48a42be44c62c8c7bc2b9151158875509a2e43010c5da70830b2f2973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133681"
---
# <a name="selecting-child-objects"></a>選取子物件

用戶端會呼叫 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) 方法，以修改物件中子系之間的選取範圍或鍵盤焦點。 以呼叫指定的 [SELFLAG 常數](selflag.md) 會定義要執行的作業。

如果以具有 **HWND** 的子物件上的 [**SELFLAG \_ TAKEFOCUS**](selflag.md)旗標呼叫 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) ，只有當物件的父系具有焦點時，此旗標才會生效。

## <a name="performing-complex-selection-operations"></a>執行複雜的選取作業

以下描述呼叫 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) 來執行複雜的選取作業時所要指定的 SELFLAG 值。

**若要模擬按一下**

-   [**SELFLAG \_TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)

**藉由模擬 CTRL + 按一下來選取目標專案**

-   [**SELFLAG \_TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ ADDSELECTION**](selflag.md)

**藉由模擬 CTRL + 按一下，取消選取目標專案**

-   [**SELFLAG \_TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)

**模擬 SHIFT + 按一下**

-   [**SELFLAG \_TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)

**若要選取物件的範圍，並將焦點放在最後一個物件上**

1.  指定起始物件的 [**SELFLAG \_ TAKEFOCUS**](selflag.md) ，以設定選取範圍錨點。
2.  再次呼叫 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) ，並在最後一個物件上指定 [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) 。

**取消選取所有物件**

1.  在任何物件上指定 [**SELFLAG \_ TAKESELECTION**](selflag.md) 。 此旗標會將所有選取的物件（除了剛剛選取的物件之外）取消選取。
2.  再次呼叫 [**IAccessible：： accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) ，並在剩餘的物件上指定 [**SELFLAG \_ REMOVESELECTION**](selflag.md) 。

 

 




