---
title: 動態輔助類別
description: 類似于結構化和抽象物件類別，輔助類別是由 Active Directory 架構中的 classSchema 物件所定義。
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- 動態輔助類別 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce88f525b5d72a271aab1746a0ce0d0b308cb7022c4702433b82038c101435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429898"
---
# <a name="dynamic-auxiliary-classes"></a>動態輔助類別

類似于結構化和抽象物件類別，輔助類別是由 Active Directory 架構中的 [**classSchema**](/windows/desktop/ADSchema/c-classschema) 物件所定義。 如需詳細資訊，請參閱 [結構化、抽象概念和輔助類別](structural-abstract-and-auxiliary-classes.md)。 此架構定義會指定類別的各種特性，包括與類別相關聯的屬性。

不同于結構化類別，您無法建立輔助類別的實例，就像您可以使用結構化類別一樣。 相反地，您可以使用輔助類別來擴充與另一個結構化、抽象或輔助物件類別相關聯的屬性清單。

在 Windows 2000 的初始版本中，Active Directory Domain Services 提供將輔助類別靜態連結至另一個物件類別 [**classSchema**](/windows/desktop/ADSchema/c-classschema)定義的支援。 以這種方式使用輔助類別時，物件類別的每個實例都支援輔助類別的屬性。

**Windows 2000 Server 及更早版本：** Active Directory Domain Services 不會提供將輔助類別動態連結至個別物件的支援，而不是只支援整個物件類別。 此外，附加至物件實例的輔助類別，之後無法從實例中移除。

**Windows Server 2003：** 當樹系中的所有網域控制站都執行 Windows server 2003 且樹系功能模式 Windows server 2003 時，即支援動態輔助類別。

如需輔助類別的詳細資訊，請參閱：

-   [動態連結的輔助類別](dynamically-linked-auxiliary-classes.md)
-   [靜態連結的輔助類別](statically-linked-auxiliary-classes.md)
-   [判斷與物件實例相關聯的類別](determining-the-classes-associated-with-an-object-instance.md)
-   [將輔助類別加入至物件實例](adding-an-auxiliary-class-to-an-object-instance.md)

For more information about forest functional levels, see "How to raise Active Directory domain and forest functional levels" in the Help and Support Knowledge Base at [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692).

 

 