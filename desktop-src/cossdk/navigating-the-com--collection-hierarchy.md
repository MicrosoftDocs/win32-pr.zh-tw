---
description: 流覽 COM + 集合階層
ms.assetid: bd72effe-898f-40a6-973c-a26e7fe2478f
title: 流覽 COM + 集合階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06fc4cde6c56bc08b0326e892409067759e91be6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973162"
---
# <a name="navigating-the-com-collection-hierarchy"></a>流覽 COM + 集合階層

您可以使用 [**COMAdminCatalog**](comadmincatalog.md)物件上的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)方法，輕鬆地取得某些集合。 這個方法會抓取「最上層」集合;也就是 [**應用程式**](applications.md)之類的集合，它本身就是唯一的，而且不會以邏輯方式建立小計另一個集合。

但是，許多集合都是以邏輯方式建立小計在另一個集合之下，因為它們包含屬於某些較大結構的元素。 例如， [**元件**](components.md) 集合是建立小計或相關的 [**應用程式**](applications.md) 集合，因為它包含特定 com + 應用程式中所安裝的元件，而該元件本身會對應到 **應用程式** 集合中的專案。 相關的集合（例如這不是唯一的）;每個不同的應用程式都有一個 **元件** 集合。

因此，集合會以階層式結構排列，並自然地對應到它們所包含的專案之間的邏輯關聯性。 集合階層的圖表可在 [Com + 系統管理集合](com--administration-collections.md)中找到。 針對您想要使用 COMAdmin 物件設定的許多元素，您需要流覽集合階層的某些部分，以取得適當的專案。

這表示實務上，如果您想要取得相關集合中的專案，您必須先完成所有必要的較高層級歸類集合。 若要抓取相關的集合，您需要在父集合中取出與子集合相關的特定專案。 例如，如果您想要設定對應至特定 COM + 應用程式中某個元件的專案，您必須執行下列步驟：

1.  取得 [**應用程式**](applications.md) 集合，並填入。
2.  列舉 [**應用程式**](applications.md) 集合的內容，直到到達對應至正確 com + 應用程式的專案為止。
3.  取得並填入該特定 COM + 應用程式的 [**元件**](components.md) 集合。
4.  列舉 [**元件**](components.md) 集合的內容，直到到達對應至正確元件的專案為止。

下列 Microsoft Visual Basic 範例顯示如何執行上述步驟：


```VB
On Error GoTo My_Error_Handler

Dim Catalog As COMAdminCatalog 
Set Catalog = CreateObject("COMAdmin.COMAdminCatalog")

' Get the Applications collection and populate it.
Dim Applications As COMAdminCatalogCollection 
Set Applications = Catalog.GetCollection("Applications") 
Applications.Populate

' Get the correct application, "My Application".
Dim AppObject As COMAdminCatalogObject 
For Each AppObject in Applications 
    If AppObject.Name = "My Application" Then 
        Exit For 
    End If
Next 

' Get and populate the Components collection for "My Application".
Dim Components As COMAdminCatalogCollection 
Set Components = Applications.GetCollection("Components", AppObject.Key) 
Components.Populate

' Get the correct component, "My Component".
Dim CompObject As COMAdminCatalogObject 
For Each CompObject in Components 
    If CompObject.Name = "My Component" Then 
        Exit For 
    End If
Next 

```



上述範例中使用兩個不同的 **>getcollection** 方法。 第一個是由 [**COMAdminCatalog**](comadmincatalog.md) 所公開，用來取得最上層的集合，在此案例中為「應用程式」。 第二個是由 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 所公開，用來取得與目前集合相關的集合;您可以藉由傳遞名稱 "Components" 和父物件的索引鍵屬性值，精確地指出您想要的集合。 索引鍵屬性值通常是可唯一識別物件的名稱或 GUID。此值會在每個集合的檔中識別。

在最常見的情況下，您必須在收集您想要的集合之前，以反復方式取得集合階層的相關集合。 您所採取的步驟會重複執行相同的一般模型。 如需完整的集合清單，請參閱 [Com + 系統管理集合](com--administration-collections.md)。

在某些情況下，您可能會想要在第二次於收集階層的路徑後面使用快捷方式方法。 只有在您已經快取所有中間的索引鍵值之後，才可以使用這個方法。 如需詳細資訊，請參閱 [**ICOMAdminCatalog：： GetCollectionByQuery**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollectionbyquery)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[填入 COM + 集合](populating-com--collections.md)
</dt> <dt>

[查詢可用的相關集合](querying-for-available-related-collections.md)
</dt> <dt>

[在 COM + 類別目錄上取出集合](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



