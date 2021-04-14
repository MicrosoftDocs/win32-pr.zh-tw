---
description: Windows Search SDK 提供 interopability 元件，可讓您使用元件物件模型 (COM) 物件，這些物件是使用 managed 程式碼針對介面和類別所公開的 Windows Search 和其他程式。
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: 搭配 Shell 資料和 Windows Search 使用 Managed 程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112492"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a>搭配 Shell 資料和 Windows Search 使用 Managed 程式碼

Windows Search SDK 提供 interopability 元件，可讓您使用元件物件模型 (COM) 物件，這些物件是使用 managed 程式碼針對介面和類別所公開的 Windows Search 和其他程式。 Interopability 元件是由 Microsoft 數位簽署，可透過 [Windows Search 範例](-search-samples-ovw.md)找到。

本主題的組織方式如下：

-   [使用 Windows API CodePack](#using-the-windows-api-codepack)
    -   [存取索引結果](#accessing-index-results)
    -   [使用 Windows API Codepack 的範例應用程式](#sample-application-using-the-windows-api-codepack)
-   [相關主題](#related-topics)

## <a name="using-the-windows-api-codepack"></a>使用 Windows API CodePack

如果您是在 Microsoft .NET 環境中工作，請使用 [適用于 microsoft .NET Framework 的 WINDOWS API Code Pack](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) 來取得搜尋結果，或只流覽命名空間。 [適用于 Microsoft .NET Framework 的 WINDOWS API 程式碼套件](https://www.nuget.org/packages/Microsoft.Windows.Compatibility)會提供 Shell 專案的集合，這些專案基本上是原生[IShellItem 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)周圍的包裝函式。 您可以逐一查看此集合，並取得各種屬性值的方式，類似于從物件連結與嵌入資料庫 (OLE DB) 查詢中列舉資料表的結果。

下列程式碼片段說明如何逐一查看搜尋專案，以及取得每個專案的屬性值。


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a>存取索引結果

您可以透過 OLE DB 或 Shell 資料模型來存取索引結果。 這兩種方法都有其優點和缺點。 其中一個優點是資料庫程式設計人員熟悉 OLE DB 和結構化查詢語言 (SQL)  (SQL) 。 在查詢索引子時，其他優點更能控制效能，以及存取其他功能，例如能夠快速地在新的資料列集中尋找先前的結果。

Shell 資料模型的優點是它會在不同的資訊來源（例如 OpenSearch）之間抽象化，並提供其他功能（例如縮圖和屬性處理常式）的存取權。 Shell 物件模型也不需要針對非檔案名結果（例如訊息項目和 OneNote 結果）或任何位於使用者索引中的專案進行特殊的案例支援。 請注意，在 Shell [KNOWNFOLDERID](../shell/knownfolderid.md) 中，是本機索引內容的已知資料夾範圍。 如需建立 Shell 資料來源的詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。

在 Windows 7 和更新版本中，不會透過 OLE DB 針對同盟搜尋來公開 OpenSearch 資料來源。 基於這個理由，我們建議您考慮撰寫 Shell 命名空間的 LINQ 提供者，而不是使用 OLE DB 來存取索引子的結果。 如需詳細資訊，請參閱 [逐步解說：建立 IQUERYABLE LINQ 提供者](/previous-versions/bb546158(v=vs.140))。

### <a name="sample-application-using-the-windows-api-codepack"></a>使用 Windows API Codepack 的範例應用程式

下列螢幕擷取畫面表示以 [Microsoft .NET Framework 的 WINDOWS API Code Pack](https://www.nuget.org/packages/Microsoft.Windows.Compatibility)建立的範例應用程式模擬。

![顯示電子郵件訊息的 media player 應用程式螢幕擷取畫面](images/folderid-searchhome.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 中的同盟搜尋](-search-federated-search-overview.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[不同語言之間的互通性](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))
</dt> </dl>

 

 
