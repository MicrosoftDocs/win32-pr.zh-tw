---
title: 依元件功能分類
description: 元件類別可以用來顯示所有已安裝元件的子集。
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967609"
---
# <a name="categorizing-by-component-capabilities"></a>依元件功能分類

元件類別可以用來顯示所有已安裝元件的子集。 每個元件類別都是由 GUID 所識別，稱為類別目錄識別碼 (CATID) 。 每個 CATID 都有一份清單，其中列出與地區設定相關的已標記、人們看得懂的名稱。 Catid 清單和人們可讀取的名稱會儲存在登錄的已知位置中。

例如，所有可執行 OLE 檔內嵌功能的元件都可以在元件類別中分類。 在過去，這些物件會由登錄中的「可插入」機碼來識別。 若要改為使用元件類別目錄，將會在登錄中新增下列資訊：

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

每個執行對應至元件類別之功能的類別，會在登錄的 CLSID 機碼中列出該類別的類別識別碼。 由於單一元件可以支援各種功能，因此元件可以屬於多個元件類別。 例如，特定的 OLE 控制項可能會支援參與 OLE 檔內嵌、Microsoft Visual Basic 資料系結和網際網路功能所需的所有功能。 這類控制項會將下列資訊儲存在登錄中的 CLSID 機碼中：

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

利用這項資訊，容器可以列舉系統上所安裝的控制項，並只顯示支援容器所需功能的控制項。 使用元件類別可讓您依元件的實功能來分類元件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將圖示與類別產生關聯](associating-icons-with-a-category.md)
</dt> <dt>

[依容器功能分類](categorizing-by-container-capabilities.md)
</dt> <dt>

[預設類別和關聯](default-classes-and-associations.md)
</dt> <dt>

[定義元件類別](defining-component-categories.md)
</dt> <dt>

[元件類別管理員](the-component-categories-manager.md)
</dt> </dl>

 

 




