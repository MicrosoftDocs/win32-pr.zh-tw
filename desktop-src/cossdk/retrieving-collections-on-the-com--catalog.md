---
description: 在 COM + 類別目錄上取出集合
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: 在 COM + 類別目錄上取出集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688692"
---
# <a name="retrieving-collections-on-the-com-catalog"></a>在 COM + 類別目錄上取出集合

COM + 目錄中的資料會儲存在集合的階層中。 在 [元件服務] 系統管理工具中，其中許多集合會顯示為主控台樹中的資料夾。 未顯示為資料夾的集合只能以程式設計的方式存取。 集合可做為專案的容器。 指定集合中的專案都是一致的類型;也就是說，它們全都代表相同種類的元素，而且集合中可以有任意數目的專案。 例如， [**應用程式**](applications.md) 集合包含電腦上所安裝之每個 com + 應用程式的專案。 此集合會在系統管理工具中顯示為 [ **Com + 應用程式** ] 資料夾。

集合會以階層式結構的形式出現，因為它們所包含的專案會遵循固有的包含順序。 例如，因為元件是安裝在 COM + 應用程式中，所以 [**元件**](components.md) 集合會以邏輯方式在 [**應用程式**](applications.md) 集合下建立小計。 更特別的是，若要將安裝的元件存放至該特定應用程式，**應用程式** 集合中的每個專案都有一個不同的 **元件** 集合。

只要您想要取得專案並設定其屬性，您就必須在目錄上取得集合。 在一般情況下，您需要逐步執行數個集合，以取得您想要的專案。 如需執行此操作的程式，請參閱 [流覽 COM + 集合](navigating-the-com--collection-hierarchy.md)階層。

在您抓取集合，而且可以直接使用其包含的專案之前，您必須填入集合，以從 COM + 類別目錄提取集合內容的資料。 如需詳細資訊，請參閱填入 [COM + 集合](populating-com--collections.md)。

此外，您還可以使用此工具，以動態方式查詢以查看您所持有的指定集合中有哪些相關的集合可供使用。 如需詳細資訊，請參閱 [查詢可用的相關集合](querying-for-available-related-collections.md)。

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

[設定屬性並將變更儲存至 COM + 類別目錄](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



