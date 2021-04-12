---
description: 屬性之間的相互相關性
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: 屬性之間的相互相關性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936328"
---
# <a name="interdependencies-between-properties"></a>屬性之間的相互相關性

當您設定屬性時，COM + 類別目錄會強制執行一些一致性邏輯，以確保您以合理的方式設定元素。 此邏輯可以用兩種方式來執行，如下所示：

-   **依賴。** 您可能會遭到封鎖而無法進行一些變更，因為另一個屬性相依于您嘗試設定之屬性的特定設定。 例如，如果元件是以所需的屬性交易來設定，而且您接著嘗試將同步處理設定變更為 [無]，當您嘗試呼叫 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 時就會產生錯誤，因為交易相依于同步處理。
-   **副作用。** 如果您沒有明確設定，某些屬性可能會變更。 例如，如果您設定的元件需要屬性交易，則也會將同步處理設定為 [必要]。 這實際上是相依性的翻轉端—一個屬性優先于另一個屬性，而其相依性則是透過第一次設定次要屬性，然後封鎖對其所做的變更來表示。

在集合中的專案所公開的屬性清單中，全都列在 [Com + 系統管理集合](com--administration-collections.md)中，每個屬性都有相關的相依性和副作用。 當您設定 COM + 應用程式和元件時，您應該留意哪些條件約束在設定上有哪些限制。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[取得和設定屬性](getting-and-setting-properties.md)
</dt> <dt>

[查詢可用的屬性](querying-for-available-properties.md)
</dt> <dt>

[儲存或捨棄變更](saving-or-discarding-changes.md)
</dt> </dl>

 

 



