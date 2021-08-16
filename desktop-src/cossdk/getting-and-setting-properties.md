---
description: 取得和設定屬性
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: '取得和設定 (元件服務的屬性) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805d98463e1f9b8f08c1018b49554c95e2735bfa7ea6dca21d90243eb324df49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306753"
---
# <a name="getting-and-setting-properties-component-services"></a>取得和設定 (元件服務的屬性) 

您必須執行下列步驟，才能讀取或寫入集合中的專案所公開的特定屬性：

1.  取得集合。
2.  從 COM + 類別目錄填入集合，以讀取資料。
3.  取出集合中的特定專案，並以 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別中的物件來表示。

如需說明這些步驟的範例，請參閱 [流覽 COM + 集合](navigating-the-com--collection-hierarchy.md)階層。

因為公開的特定屬性會根據專案代表的專案而有所不同;也就是說，代表元件的專案具有不同于一個代表 COM + 應用程式的屬性。 在 [**COMAdminCatalogObject**](comadmincatalogobject.md)上使用單一泛型屬性（Value 屬性）設定這些屬性的任何一個。

Value 屬性可讓您取得或設定專案所公開的任何特定命名屬性，取得時傳回的命名屬性值，並在設定時使用名稱和值。

在使用 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件上的 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)方法明確儲存變更之前，不會實際將任何變更記錄至 com + 類別目錄。 指定集合中所有專案上所有屬性的暫止變更都會一次儲存。 如需詳細資訊，請參閱 [儲存或捨棄變更](saving-or-discarding-changes.md)。

並非您所做的所有變更都將被接受。 COM + 類別目錄會強制執行一些一致性邏輯，以確保您以合理的方式設定專案。 此外，當您變更某些屬性時，其他屬性可能會由相同的一致性邏輯自動變更。 當您嘗試儲存變更時，就會顯示這些效果。

> [!Note]  
> 您可能會與另一個寫入器對 COM + 類別目錄進行競爭。 在對指定集合進行 [**擴展和**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 的呼叫之間，不會鎖定目錄中的任何資料。 多個合作物件可以同時設定指定集合中的專案，而且可能會在儲存變更時進行爭用。 這表示，其他人可能會在您執行程式之前或之後變更物件的設定，不論是在本機或遠端使用 COMAdmin 物件或使用「元件服務」系統管理工具來執行。 在目錄上撰寫物件的一般規則是，物件上的所有屬性都會一次寫入。 也就是最後一個寫入器獲勝—物件會精確地儲存在目錄中，如同最後一個寫入器設定的一樣。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[屬性之間的相互相關性](interdependencies-between-properties.md)
</dt> <dt>

[查詢可用的屬性](querying-for-available-properties.md)
</dt> <dt>

[儲存或捨棄變更](saving-or-discarding-changes.md)
</dt> </dl>

 

 



