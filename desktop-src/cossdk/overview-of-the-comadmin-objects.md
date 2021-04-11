---
description: COMAdmin 物件提供簡單的物件模型，可讓您存取 COM + 類別目錄。
ms.assetid: 84cee7a7-f7a6-41a0-afd5-fae56365612e
title: COMAdmin 物件的總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22837cbe0548b623463234d1a03d17288eba2149
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111673"
---
# <a name="overview-of-the-comadmin-objects"></a>COMAdmin 物件的總覽

COMAdmin 物件提供簡單的物件模型，可讓您存取 COM + 類別目錄。 如此一來，他們就可以建立「元件服務」系統管理工具所提供的所有功能的模型。 每當您進行任何類型的 COM + 管理時，您都會與 COM + 類別目錄互動。 如需目錄的描述，請參閱 [存取 COM + 類別目錄](accessing-the-com--catalog.md)。

您從 [元件服務] 系統管理工具或使用 COMAdmin 物件取得的資訊結構類似，而且您在其中一個內容中執行的動作也類似。 使用 [元件服務] 嵌入式管理單元和以程式設計方式管理的基本關聯性，是嵌入式管理單元的主控台樹中的資料夾，會對應至 COM + 目錄中的集合。 也就是說，就像嵌入式管理單元中的每個資料夾都包含各種專案，例如， **com + 應用程式** 會保存已安裝的 com + 應用程式，com + 目錄中的每個集合都會保存統一種類的專案。 此外，如同資料夾中的每個專案都有可在屬性工作表上設定的屬性，集合中的每個專案都會公開您可以設定的屬性。

為了讓您能夠設定此結構內的物件，COMAdmin 物件會提供您執行下列動作的方法：

-   存取 COM + 類別目錄
-   存取目錄中的集合
-   存取集合中的專案
-   存取集合中專案的屬性

為了支援這些動作，COMAdmin 程式庫提供下列三個類別：

-   [**COMAdminCatalog**](comadmincatalog.md)，代表目錄本身。
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md)，表示任何集合。
-   [**COMAdminCatalogObject**](comadmincatalogobject.md)，代表集合中的任何專案。

如需這些類別的完整說明，請參閱本節中 [COMAdmin 類別的摘要描述](summary-description-of-the-comadmin-classes.md) 。

若要快速瞭解您在程式設計管理中執行的一般動作，請參閱 [使用 COM + 系統管理目錄的簡介範例](introductory-example-using-the-com--administration-catalog.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[交易內的 COM + 管理作業](com--administration-operations-within-transactions.md)
</dt> <dt>

[處理 COM + 管理錯誤](handling-com--administration-errors.md)
</dt> <dt>

[使用 COM + 系統管理目錄的簡介範例](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[在 COM + 類別目錄上取出集合](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[設定屬性並將變更儲存至 COM + 類別目錄](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



