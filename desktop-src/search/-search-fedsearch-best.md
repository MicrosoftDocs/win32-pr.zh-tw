---
description: 本主題列出您可以用來建立可使用 Windows 同盟搜尋來搜尋之 web 資料存放區的最佳作法，並將您的遠端資料源與 Windows 檔案總管整合，而不需要撰寫或部署任何 Windows 用戶端程式代碼。
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: 遵循 Windows 同盟搜尋的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112460"
---
# <a name="following-best-practices-in-windows-federated-search"></a>遵循 Windows 同盟搜尋的最佳作法

本主題列出您可以用來建立可使用 Windows 同盟搜尋來搜尋之 web 資料存放區的最佳作法，並將您的遠端資料源與 Windows 檔案總管整合，而不需要撰寫或部署任何 Windows 用戶端程式代碼。

本主題的組織方式如下：

-   [Windows 同盟搜尋的最佳作法](#best-practices-for-windows-federated-search)
-   [建立 RSS 輸出的最佳作法](#best-practices-for-creating-rss-output)
-   [其他資源](#additional-resources)
-   [相關主題](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>Windows 同盟搜尋的最佳作法

在 Windows 7 中使用 [OpenSearch](https://github.com/dewitt/opensearch) 的最佳作法如下：

-   支援 *{startIndex}* 和 *{count}* 個參數，而且除非您傳回最後一個結果，否則務必一律傳回所要求的專案數。
-   如果您知道副檔名，請將其對應至 [FileExtension](../properties/props-system-fileextension.md) Windows Shell 屬性。 使用副檔名是識別 MIME 類型之檔案類型的較佳方式。
-   確定您在 RSS 中指定的 MIME 類型或副檔名，符合在要求專案內容時裝載專案之 web 伺服器的 HTTP 標頭中所傳回的檔案名和 MIME 類型。
-   如果您要傳回檔案專案，請盡可能傳回檔案大小。 這樣可確保 [下載進度] 對話方塊正確無誤。
-   確認對結果集結尾以外的專案所提出的要求不會傳回任何結果。
    > [!Note]  
    > 不要重複結果。

     

-   請勿將 HTML 標籤放在不屬於的位置。 根據 RSS 規格，它們在 [描述] 欄位中是有效的，但不在 [標題] 欄位中。
-   請勿建立網頁專案的主機殼。 例如，如果您建立主機殼並對應 .aspx 的副檔名，則會 Windows 檔案總管將檔案下載至網際網路快取，並從該處執行該檔案。 Web 瀏覽器不會處理 .aspx 檔案類型。 使用者會收到 **開啟檔案** 對話方塊，或者檔案可能會由 Microsoft Visual Studio 之類的應用程式開啟。 只要針對網頁傳回 link 元素，即可避免此情況。
-   使用 URL 範本搭配，在 .osdx 檔案中提供 web 向前復原 URL `format="text\html"` 。
-   將自訂元素 URL 值對應至 [ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell 屬性，以提供父資料夾、容器或網頁的 url。

## <a name="best-practices-for-creating-rss-output"></a>建立 RSS 輸出的最佳作法

建立 RSS 輸出的最佳作法如下：

-   每個專案都必須傳回 `link` `enclosure` (或相等的 URL 或值，例如 `media:content`) 
-   請勿在 **title** 屬性中包含任何 HTML 格式標記，否則這些標記會出現在標題中，並顯示在 Windows 檔案總管中。
-   針對 **description** 元素：
    -   顯示足夠的資訊，讓使用者知道此結果可能相關的原因。
    -   請勿包含 HTML 格式。 [OpenSearch](https://github.com/dewitt/opensearch)提供者會移除格式，而這可能會導致您的描述產生小於預期的結果。
    -   請勿包含已經在其他元素中提供的中繼資料，例如，機殼檔案名、大小、修改日期等，因為 Windows 檔案總管已經顯示中繼資料。 將它顯示在 **description** 元素中會是多餘的。
-   針對主機殼或內容 Url：
    -   將類型屬性指定為有效的 MIME 類型。
    -   指定檔案大小（以位元組為單位）。
-   如果您要使用 .NET 在 .NET 中執行 RSS 輸出 `DateTime` ，請在 Microsoft Internet Explorer 中測試您的摘要，以查看它是否有效，再將其部署至 Windows 檔案總管。

## <a name="additional-resources"></a>其他資源

如需有關使用 Windows 7 和更新版本中的 OpenSearch 技術來執行遠端資料存放區之搜尋同盟的詳細資訊，請參閱 [windows 同盟搜尋中](/previous-versions//dd742958(v=vs.85))的「其他資源」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 中的同盟搜尋](-search-federated-search-overview.md)
</dt> <dt>

[在 Windows 中使用同盟搜尋開始使用](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[在 Windows 同盟搜尋中連接您的 Web 服務](-search-federated-search-web-service.md)
</dt> <dt>

[在 Windows 同盟搜尋中啟用資料存放區](-search-federated-search-data-store.md)
</dt> <dt>

[在 Windows 同盟搜尋中建立 OpenSearch 描述檔案](-search-federated-search-osdx-file.md)
</dt> <dt>

[在 Windows 同盟搜尋中部署搜尋連接器](-search-federated-search-deploying.md)
</dt> <dt>

[擴充索引](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
