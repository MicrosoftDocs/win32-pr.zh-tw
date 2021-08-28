---
description: 瞭解 Windows Search 如何讓您使用搜尋管理員、目錄管理員和編目範圍管理員來管理 Windows Search 索引。
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: 用於管理索引的介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec4b7986001a03dacd004f158406b70de81152040065e8a9951148f14414f6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597788"
---
# <a name="interfaces-for-managing-the-index"></a>用於管理索引的介面

Windows搜尋可讓您使用三個主要元件來管理 Windows Search 索引：搜尋管理員、目錄管理員和編目範圍管理員。 其中一些管理介面可以搭配標準使用者權限使用，但變更索引狀態的那些管理介面需要系統管理許可權。

## <a name="about-the-interfaces-for-managing-the-index"></a>關於用來管理索引的介面

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>元件</th>
<th>介面</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>搜尋管理員</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></td>
<td>提供方法來取得和設定 Windows Search 的相關資訊：
<ul>
<li>取得特定目錄之目錄管理員的實例。</li>
<li>取得或設定 proxy 資訊。</li>
<li>取得 Windows Search 引擎的版本資訊。</li>
</ul>
如需詳細資訊，請參閱 <a href="-search-3x-wds-mngidx-searchmanager.md">使用搜尋管理員</a>。<br/></td>
</tr>
<tr class="even">
<td>目錄管理員</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br/></td>
<td>提供管理個別搜尋目錄的方法，例如造成重新編制索引或設定超時時間。 此介面會在四個區域中管理目錄：
<ul>
<li>目錄內容-確保新的資料已編制索引，而且其他應用程式和元件可以正常運作，方法是強制重新編制所有或部分類別目錄的索引，或重設整個目錄。</li>
<li>目錄屬性-設定屬性，以決定當連接到通訊協定處理常式時，目錄如何管理時間超時，以及如何在搜尋中處理變音符號標記。</li>
<li>目錄狀態-取得目錄的相關資訊，包括狀態、大小和目前的活動狀態。</li>
<li>存取其他介面-抓取編目範圍管理員所需的其他搜尋相關介面、資料變更通知，以及 <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> 介面。</li>
</ul>
如需詳細資訊，請參閱 <a href="-search-3x-wds-mngidx-catalog-manager.md">使用目錄管理員</a>。<br/></td>
</tr>
<tr class="odd">
<td>編目範圍管理員</td>
<td><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a><br/> <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a><br/> <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a><br/> <a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a><br/></td>
<td>提供方法來通知搜尋引擎有關要編目或監看的容器，以及要在索引中包含或排除的容器底下的專案。 您也可以查詢編目範圍管理員，以查看特定的 URL 是否在編目範圍中。 如需詳細資訊，請參閱 <a href="-search-3x-wds-extidx-csm.md">使用編目範圍管理員</a>。<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>相關主題

[管理索引](-search-3x-wds-mngidx-overview.md)

[使用搜尋管理員](-search-3x-wds-mngidx-searchmanager.md)

[使用目錄管理員](-search-3x-wds-mngidx-catalog-manager.md)

[使用編目範圍管理員](-search-3x-wds-extidx-csm.md)
