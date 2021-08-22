---
description: 集合中的每個專案都會公開屬性。
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: 編輯 COM + 目錄中的屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ace2809fef4510a9c89b5faf31df555cb76426a06dd445aff9438c0d19e887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546226"
---
# <a name="editing-properties-in-the-com-catalog"></a>編輯 COM + 目錄中的屬性

集合中的每個專案都會公開屬性。 這些屬性可保存專案所代表之任何元素的設定資料。 在 [元件服務] 系統管理工具中，這些屬性會出現在您透過以滑鼠右鍵按一下資料夾中的專案來存取的屬性頁面上。

因為指定集合中的專案全都代表相同類型，所以這些專案會公開一組在集合中一致的屬性。 例如， [**應用程式**](applications.md) 集合會公開 Name 屬性、AppID 屬性等等。 這類似于「元件服務」系統管理工具中的每個應用程式如何使用一致的結構化屬性頁面。 如需 **應用程式** 集合可用的屬性清單，請參閱 **應用程式**。 如需 [**元件**](components.md) 集合可用的屬性清單，請參閱 **元件**。

如需每個集合中的專案所公開之屬性的完整清單，請參閱 [Com + 系統管理集合](com--administration-collections.md)。

您可以使用從 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別建立的物件，表示集合中的專案。 這個物件可讓您設定和取得專案所公開的任何屬性。 設定屬性時，您也可能會將其他寫入器與 COM + 類別目錄進行爭用。 如需詳細資訊，請參閱 [取得和設定屬性](getting-and-setting-properties.md)。

設定屬性之後，在您明確儲存變更之前，不會實際認可任何變更。 如需詳細資訊，請參閱 [儲存或捨棄變更](saving-or-discarding-changes.md)。

當您儲存變更時，COM + 類別目錄會強制執行一些設定邏輯，以確保您不會將某些專案設定為不相容的設定。 當您明確變更某些其他屬性時，它也會變更某些屬性。 如需詳細資訊，請參閱 [屬性之間的相互相關性](interdependencies-between-properties.md)。

此外，COM + 也有一項功能，可讓您以動態方式查詢以查看指定集合中的專案可使用哪些屬性。 如需詳細資訊，請參閱 [查詢可用的屬性](querying-for-available-properties.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[交易內的 COM + 管理作業](com--administration-operations-within-transactions.md)
</dt> <dt>

[處理 COM + 管理錯誤](handling-com--administration-errors.md)
</dt> <dt>

[使用 COM + 系統管理目錄的簡介範例](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[COMAdmin 物件的總覽](overview-of-the-comadmin-objects.md)
</dt> <dt>

[在 COM + 類別目錄上取出集合](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



