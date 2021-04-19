---
description: 使用 Windows Search 來查詢索引的方式有好幾種。
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: 以程式設計方式查詢索引
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967097"
---
# <a name="querying-the-index-programmatically"></a>以程式設計方式查詢索引

使用 Windows Search 來查詢索引的方式有好幾種。

本節提供以程式設計方式查詢索引的概念架構：

-   [使用 SQL 和 AQS 方法來查詢索引](using-sql-and-aqs-to-query-the-index.md)
-   [使用 ISearchQueryHelper 查詢索引](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [使用搜尋-ms 通訊協定來查詢索引](-search-3x-wds-qryidx-searchms.md)
-   [使用 Windows Search SQL 語法來查詢索引](-search-sql-windowssearch-entry.md)
-   [以程式設計方式使用 Advanced 查詢語法](-search-3x-advancedquerysyntax.md)

> [!Note]  
> 舊版 Microsoft Windows 桌面搜尋 (WDS) 2x 相容性：在執行 Windows XP 及更新版本的電腦上， [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) 已被取代。 相反地，開發人員應該使用 [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) 取得連接字串，並將使用者的查詢剖析成結構化查詢語言 (SQL)  (SQL) ，然後查詢物件連結與嵌入資料庫 (OLE DB) 。

 

## <a name="additional-resources"></a>其他資源

-   如需 OLE DB 的詳細資訊，請參閱 [OLE DB 程式設計總覽](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx)。 如需 OLE DB 之 .NET Framework Data Provider 的詳細資訊，請參閱 system.string [命名空間](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1)。
-   如需在查詢中使用屬性的其他背景，請參閱下列主題：
    -   [屬性系統](../properties/building-property-handlers.md)
    -   [系統屬性](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
-   如需有關如何建立和修改搜尋資料夾的詳細資訊，請參閱 [**ISearchFolderItemFactory 介面**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory)。
-   如需有關搜尋技術的社區支援問題和討論訊息板，請參閱 [MSDN 論壇： Windows 桌面搜尋開發](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads)。
-   若要下載搜尋 SDK 程式碼範例：
    -   針對 Windows 7： [在 GitHub 上 Windows Search 範例](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)
    -   Windows Vista： [WINDOWS SEARCH SDK 範例](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
-   若要下載 Windows SDK：
    -   適用于 windows 7： [適用于 windows 7 和 .NET Framework 的 Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
    -   Windows Vista：適用于 [Windows vista 和 .NET Framework 的 Windows SDK](https://www.microsoft.com/download/details.aspx?id=31950)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Search 開發指南](-search-developers-guide-entry-page.md)
</dt> <dt>

[管理索引](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[擴充 Windows Search 索引](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[擴充語言資源](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
