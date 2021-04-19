---
description: COMAdmin 程式庫提供三個類別 (comadmin.dll) ，其中每個類別都會執行 COM 雙重介面。
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: COMAdmin 類別的摘要描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971954"
---
# <a name="summary-description-of-the-comadmin-classes"></a>COMAdmin 類別的摘要描述

COMAdmin 程式庫提供三個類別 (comadmin.dll) ，其中每個類別都會執行 COM 雙重介面。 您可以使用從這些類別建立的物件來取得目錄的存取權，以表示目錄中的集合，以及代表集合中包含的專案。

## <a name="comadmincatalog"></a>COMAdminCatalog

[**COMAdminCatalog**](comadmincatalog.md)類別代表目錄本身。 從 **COMAdminCatalog** 建立的物件是您在程式設計管理中使用的基本物件。 除了在具現化時建立與目錄伺服器的基本連線， **COMAdminCatalog** 提供的方法可讓您執行下列作業：

-   取得目錄的集合。
-   連接至遠端電腦上的目錄伺服器。
-   安裝、匯出、啟動、關閉，以及取得 COM + 應用程式的相關資訊。
-   將元件安裝至 COM + 應用程式，並取得有關元件的資訊。
-   啟動、停止或重新整理電腦上正在執行的服務。
-   重新整理、還原或備份目錄資訊。

在 COM + 1.0 中， [**COMAdminCatalog**](comadmincatalog.md) 類別會執行 [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) 介面。 在 COM + 1.5 中， **COMAdminCatalog** 類別會將 [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) 實作為其預設介面。

## <a name="comadmincatalogcollection"></a>COMAdminCatalogCollection

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)類別代表目錄中的任何集合，方法是在物件具現化時提供命名特定集合的字串。  (可用的目錄集合會在 [Com + 系統管理集合](com--administration-collections.md)的資料表中命名。當您藉由呼叫 [**COMAdminCatalog**](comadmincatalog.md)物件的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)方法來抓取最上層集合時，會從這個類別建立 ) 物件。 藉由呼叫其父集合物件的 **>getcollection** 方法，以抓取子集合時，也會建立這些物件。 **COMAdminCatalogCollection** 物件可讓您執行下列作業：

-   列舉集合中包含的專案。
-   從集合中取出專案。
-   在集合中加入或移除專案。
-   儲存或捨棄對集合所做的任何暫止變更或其包含的專案。
-   取得目錄中不同的集合。

[**COMAdminCatalogObject**](comadmincatalogobject.md)類別會實 [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)介面。

## <a name="comadmincatalogobject"></a>COMAdminCatalogObject

[**COMAdminCatalogObject**](comadmincatalogobject.md)類別代表集合中包含的任何專案。 當透過目錄集合物件的 [**item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) 屬性取得專案時，會從這個類別建立物件。 從 **COMAdminCatalogObject** 類別建立的物件可讓您執行下列作業：

-   取得或設定物件用來表示之專案所支援的屬性。
-   取得專案及其屬性的相關資訊。

[**COMAdminCatalogObject**](comadmincatalogobject.md)類別會實 [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[存取 COM + 類別目錄](accessing-the-com--catalog.md)
</dt> <dt>

[COMAdmin 物件的總覽](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 



