---
title: 開發通訊協定處理常式增益集
description: 您可以藉由執行自訂通訊協定處理常式，將 Microsoft Windows Desktop Search (WDS) 加入新的資料存放區。
ms.assetid: 2447d95f-5832-453c-8857-3b4f4c158177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc107c8ca51d43e2602206eb993cea6cac6dd9ec866670235daf7fb81452f5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726498"
---
# <a name="developing-protocol-handler-add-ins"></a>開發通訊協定處理常式增益集

> [!NOTE]
> WindowsDesktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集的形式提供。 在之後的版本中，請改用[Windows Search](../search/-search-3x-wds-overview.md) 。

您可以藉由執行自訂通訊協定處理常式，將 Microsoft Windows Desktop Search (WDS) 加入新的資料存放區。

## <a name="indexing-data-stores-with-protocol-handlers"></a>使用通訊協定處理常式編制資料存放區索引

資料存放區是一個內容來源 (資料庫系統、目錄、儲存資料的檔案系統) ，而且可由 WDS 索引子進行編目。 存放區可以是階層式 (例如資料庫) 或以連結為基礎的 (，例如網站) 。 通訊協定處理常式可將 WDS 的索引編制為有系統地編目資料存放區的節點，以解壓縮要包含在索引中的相關資訊。 每個通訊協定處理常式都是用來編制特定資料存放區類型的索引。 WDS 隨附適用于檔案系統存放區的通訊協定處理常式，以及 microsoft Outlook 和 microsoft Outlook Express 資料存放區 (的電子郵件存放區。PST 檔案等) 。 例如，將 Outlook 電子郵件編制索引時，通訊協定處理常式會編目所有資料夾中的所有訊息，並從每個訊息和附件解壓縮資訊。 這項資訊會傳遞至要包含在 WDS 目錄中的索引子。

使用者通常需要搜尋其他資料存放區，例如舊版資料庫、電子郵件存放區或 WDS 不支援的資料結構。 您可以使用或專門針對該資料存放區執行通訊協定處理常式，來擴充 WDS 以編目新的資料存放區。 首先，您應該先判斷資料存放區的通訊協定處理常式是否已存在，或許可以與其他應用程式（例如 SharePoint Services）一起使用。 若是如此，您可以在系統上安裝該通訊協定處理常式。 但是，如果另一個通訊協定處理常式不存在，則您需要執行一個處理常式。 WDS 通訊協定處理常式會使用與 SharePoint Services 相同的設計規格，而且通常可以交換使用。

此外，如果資料存放區包含 WDS 所支援的其中一種200檔案類型以外的資料或檔案類型，您也需要執行篩選來存取和編制存放區中專案內容的索引。 WDS 2.x 使用 SharePoint Services 所使用的通訊協定處理常式和 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)技術。 如果您已經在要編制索引的系統上安裝特定存放區和檔案類型的篩選器，WDS 會使用現有的介面來為此資料編制索引。

 

## <a name="roadmap-to-adding-new-data-stores"></a>新增資料存放區的藍圖

若要擴充 WDS 以編目新的資料存放區，您可以建立通訊協定處理常式，以及下列一或多個增益集：內容功能表處理常式、圖示處理常式和 SearchProtocolOptions 增益集。

1.  建立並註冊資料存放區的多執行緒通訊協定處理常式：
    -   **ISearchProtocol** -此介面會存取通訊協定，並將 URL 對應至 IUrlAccessor。
    -   **IUrlAccessor** -這是用來從內容來源存取專案，並將內容系結至適當篩選的主要介面。
    -   **IProtocolHandlerSite** -此介面可用來要求和載入其他篩選。
    -   **IFilter** -這個介面會傳回資料夾中每個專案的 URL，做為處理的值屬性。

    > [!Note]
    >
    > 從非階層式資料存放區傳回搜尋結果所需的最少增益集功能，是 ISearchProtocol 和 IUrlAccessor 介面的實作為。

     

2.  執行 ISearchProtocolOptions 介面，以包含自訂的通訊協定處理常式選項，例如預先定義的起始頁 (s) ：
    -   **ISearchProtocolOptions** -此介面會定義要處理的通訊協定處理常式的預設 url、判斷通訊協定處理常式的需求，並判斷指定的系統是否符合需求。
3.  藉由執行下列介面，擴充 Shell 以包含使用者介面專案，例如內容功能表和檔案特定圖示：
    -   **IShellFolder** -這是用來管理資料夾的介面，必須提供新存放區中 URL 的 ICoNtextMenu 和 IExtractIcon 介面。
    -   **IPersistFolder** -必須有這個介面，才能指示 Shell 資料夾物件初始化本身。
    -   **IPersist** ：這個介面會提供物件的類別識別碼 (CLSID) ，而該物件可以持續儲存在系統中。
    -   **ICoNtextMenu** -此介面會定義 URL 所指向之專案的滑鼠右鍵內容功能表。
    -   **IExtractIcon** -此介面會定義要針對 URL 所指向之專案顯示的圖示。
4.  執行機制，以通知索引子變更您的資料存放區：
    -   **ISearchItemsChangedSink** -此介面可讓您的通訊協定處理常式通知索引資料存放區的變更。 這可確保索引子不會在累加式索引上編目整個存放區，以改善效能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[執行 WDS 的通訊協定處理常式](-search-2x-wds-phimplementing.md)
</dt> <dt>

[使用 Shell 擴充功能新增圖示、預覽和內容功能表](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[通知索引變更](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[安裝和註冊通訊協定處理常式](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 