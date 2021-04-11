---
description: 產品代碼是 GUID，也就是應用程式或產品的主體識別。 請參閱產品代碼。
ms.assetid: 4de84885-587d-405f-ba85-d62e09e8ba92
title: 變更產品代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0272f1901ef60342f01f4db091e7a4e62b28e30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026640"
---
# <a name="changing-the-product-code"></a>變更產品代碼

產品代碼是 GUID，也就是應用程式或產品的主體識別。 請參閱 [產品代碼](product-codes.md)。

符合下列指導方針的更新通常不需要變更產品程式碼，而且可以當作 [小型更新](small-updates.md)來處理，或是在版本變更時，做為 [次要升級](minor-upgrades.md)：

-   更新可以放大或縮小功能元件樹狀結構，但不能重新組織 [功能](feature-table.md) 和 [FeatureComponents](featurecomponents-table.md) 資料表所描述的現有功能和元件階層。 它可以將新功能加入至現有的功能元件樹狀結構。 如果移除父功能，它也必須移除已移除功能的所有子功能。
-   更新可將新的元件新增至新的或現有的功能。
-   更新不得變更任何元件的元件代碼。 因此，小型更新或次要升級絕不能變更元件的金鑰檔名稱，因為這需要變更元件的程式碼。
-   更新不能變更安裝封裝之 .msi 檔案的名稱。 相反地，因為它會修改套件，所以它應該會變更封裝程式碼。 請注意，這表示更新可以變更 .msi 檔案中的資料表、自訂動作和對話，而不需要變更檔案的名稱。
-   更新可以新增、移除或修改兩個或多個功能不共用的檔案、登錄機碼或元件的快捷方式。 如果更新修改了已建立版本的檔案，該檔案的版本必須在檔案 [資料表](file-table.md)中遞增。 如果更新移除資源，它也應該更新 [RemoveFile](removefile-table.md) 和 [RemoveRegistry](removeregistry-table.md) 資料表，以移除任何未使用的檔案、登錄機碼或已安裝的快捷方式。
-   由兩個或多個功能共用的元件更新必須與使用該元件的所有應用程式和功能回溯相容。 只要變更可回溯相容，更新就可以修改共用元件的資源，例如檔案、登錄專案和快捷方式。 建議您不要更新新增或移除共用元件中的檔案、登錄專案或快捷方式。
-   小型更新隨附于 Windows Installer [修補套件](patch-packages.md)。  (完整的產品光碟通常不提供小型更新。 ) 

如果更新有下列任何一項，則必須變更產品代碼：

-   在相同系統上並存安裝原始和更新的產品必須是可行的。
-   .Msi 檔案的名稱已經變更。
-   現有元件的元件程式碼已變更。
-   元件會從現有的功能中移除。
-   現有功能的子系已成為現有功能的子系。
-   現有的子功能已從其父項功能中移除。

請注意，將新的子功能（由全新元件組成）新增至現有的功能，並不需要變更產品代碼。

您可以在 [功能資料表](feature-table.md)的 [屬性] 欄位中包含 MsidbFeatureAttributesFollowParent 和 msidbFeatureAttributesUIDisallowAbsent，以撰寫新的子功能。 如果次要升級只加入新的子功能，請重新安裝 = 全部都足以強制安裝新的子功能。 如需詳細資訊，請參閱 [控制特徵選取狀態](controlling-feature-selection-states.md)。

使用者可能會隱藏新的子功能。 若要同步處理新子功能與其父功能的安裝狀態，請設定子功能的 msidbFeatureAttributesFollowParent 和 msidbFeatureAttributesUIDisallowAbsent 位。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於屬性](about-properties.md)
</dt> <dt>

[使用屬性](using-properties.md)
</dt> <dt>

[屬性參考](property-reference.md)
</dt> </dl>

 

 



