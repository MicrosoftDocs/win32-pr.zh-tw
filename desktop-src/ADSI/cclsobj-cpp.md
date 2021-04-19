---
title: CCLSOBJ.Cpp
description: 在範例提供者元件中，架構類別物件的函式包含在 cclsobj 中。
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- CSampleDSClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968410"
---
# <a name="cclsobjcpp"></a>CCLSOBJ.Cpp

在範例提供者元件中，架構類別物件的函式包含在 cclsobj 中。

**CSampleDSClass** 類別是在這個檔案中定義的。 **CSampleDSClass** 是使用下表所列的方法和屬性來定義的。



| 方法                      | 描述                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSClass**          | 標準的函式。                                                                                                                                                                                      |
| **~ CSampleDSClass**         | 標準的函式。                                                                                                                                                                                       |
| **CreateClass**             | 建立 ADs 架構類別物件。 藉由呼叫 **SampleDSGetClassDefinition** 來查閱屬性定義。                                                                                                 |
| **CreateClass**             | 建立架構類別物件，指定屬性定義，設定已知的屬性，例如 [**得到 iadsclass：： MandatoryAttributes**](iadsclass-property-methods.md)中所列的屬性。                     |
| **AllocateClassObject**     | 建立架構類別物件，並載入其類型資料。                                                                                                                                                       |
| **QueryInterface**          | 傳回要求的介面指標（如果有的話）。                                                                                                                                                      |
| 標準 IADs 方法。      | 此檔案中包含的標準 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面方法。                                                                                                                                     |
| 標準得到 iadsclass 方法。 | 此檔案中包含的標準 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 介面方法。                                                                                                                           |
| **CreatePropertyList**      | 藉由呼叫 **CreatePropertyEntry**，建立與此架構類別相關聯的屬性清單。                                                                                                          |
| **CreatePropertyEntry**     | 在此架構類別中建立一個屬性物件。                                                                                                                                                           |
| **FreePropertyEntry**       | 釋放在 **CreatePropertyEntry** 中所做的專案。                                                                                                                                                            |
| **MakeVariantFromPropList** | 從 **CreatePropertyList** 所建立的屬性清單建立變體陣列。 可以用於 [**得到 iadsclass：： MandatoryAttributes**](iadsclass-property-methods.md) 的實，依此類推。 |



 

 

 




