---
title: 預設類別和關聯
description: 針對特定類別，單一類別可以關聯為預設類別。
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371862"
---
# <a name="default-classes-and-associations"></a>預設類別和關聯

針對特定類別，單一類別可以關聯為預設類別。 每當需要物件的特定類別時，就會選取預設的類別。 雖然這對所有元件類別都沒有説明，但在不需要使用者介入的情況下，當特定類別必須從可能的類別清單中載入時，建立預設類別會很有説明。 系統管理員可以藉由操作登錄來定義可使用的類別。

若要建立預設類別與類別之間的關聯，請引入 CLSID 索引鍵，其 CLSID 與選擇作為預設的元件類別的 CATID 相同。 然後使用類別的預設類別 CLSID 的值，將 TreatAs 索引鍵新增至此索引鍵。 若要使用元件類別的預設類別，請使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 或 [**COGETCLASSOBJECT**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)，指定 CLSID 參數的 CATID。 這會自動重新導向至建立為此分類預設值的 CLSID。 登錄專案如下所示：

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

在安裝期間，元件可以檢查其類別目錄的任何預設類別機碼是否存在，並為使用者提供覆寫目前設定的選項。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將圖示與類別產生關聯](associating-icons-with-a-category.md)
</dt> <dt>

[依元件功能分類](categorizing-by-component-capabilities.md)
</dt> <dt>

[依容器功能分類](categorizing-by-container-capabilities.md)
</dt> <dt>

[定義元件類別](defining-component-categories.md)
</dt> <dt>

[元件類別管理員](the-component-categories-manager.md)
</dt> </dl>

 

 




