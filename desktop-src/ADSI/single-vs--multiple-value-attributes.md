---
title: Single 與 Multiple Value 屬性
description: 可以存在於目錄中的屬性通常會定義在目錄的架構中。
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- single 與 multiple value 屬性 ADSI
- 屬性 ADSI、single 與 multiple value 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd9442a5365efbe343c2a9af74aa8576928e7a6a383cc131a3384152c2b1c0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262028"
---
# <a name="single-vs-multiple-value-attributes"></a>Single 與 Multiple Value 屬性

可以存在於目錄中的屬性通常會定義在目錄的架構中。 屬性（attribute）的架構定義（attribute）會指定屬性（attribute）的許多特性（attribute），例如資料類型，以及屬性（attribute）的實例是否可以有多個值。

單一值屬性的實例可以包含單一值。 多重值屬性的實例可以包含單一值或多個值。 Active Directory 不會建立具有空白值的屬性，因為屬性包含有效的值，或不存在於物件上。

> [!Note]  
> 在 Active Directory 和大部分其他 LDAP 伺服器中，多重值屬性中的值順序是未定義的。 此外，多重值屬性的每個值都必須是唯一的。

 

如果您的目錄支援架構，則 ADSI 通常會載入架構資料，如同 Active Directory 一樣。 因為 ADSI 知道架構中的屬性語法，所以在存取它時，您不需要指定屬性類型。 ADSI 會將屬性值封送處理至架構中定義的適當資料類型。

如果您的目錄沒有架構，請在存取屬性時提供資料類型。

> [!Note]  
> Active Directory、Exchange、Windows NT 4.0 和網站伺服器都有架構。 此外，Active Directory 具有可延伸的架構。

 

 

 




