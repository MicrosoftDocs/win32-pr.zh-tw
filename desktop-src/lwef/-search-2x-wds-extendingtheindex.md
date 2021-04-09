---
title: " (舊版 Windows 環境功能擴充索引) "
description: 使用和開發 Microsoft Windows 桌面搜尋的2.x 版 (WDS) 強烈建議您改用 Windows Search。
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093719"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a> (舊版 Windows 環境功能擴充索引) 

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在之後的版本中，請改用 [Windows Search](../search/-search-3x-wds-overview.md) 。

使用和開發 Microsoft Windows 桌面搜尋的2.x 版 (WDS) 強烈建議您改用 [Windows Search](../search/-search-3x-wds-overview.md)。

您可以擴充 WDS 來為新檔案類型和資料存放區的內容編制索引。 目前，WDS 2.x 包含超過200種專案類型的篩選 (包括 HTML、XML 和原始程式碼檔案等純文字專案) ，並使用與 SharePoint 服務相同的 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)和通訊協定處理常式技術。 如果您已針對新的檔案類型安裝篩選器，WDS 可以使用現有的篩選介面來為此資料編制索引。

WDS 2.x 增益集可讓索引進行資料和資料結構的往返分析，以取得要新增至可搜尋目錄的資訊。 這些增益集也可以擴充 Windows Shell，將圖示和內容功能表處理常式與新的檔案類型和資料存放區產生關聯。 若要在 WDS 目錄中包含新的檔案類型，增益集必須執行 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面。 若要加入新的資料存放區，增益集必須是通訊協定處理常式。 如果新的資料存放區包含內嵌檔案或新的檔案類型本身，您也必須撰寫適當的篩選。

> [!Note]
>
> 篩選和通訊協定處理常式必須以機器碼撰寫，因為處理所有增益集時，可能發生 CLR 版本控制問題。

 

## <a name="adding-file-types-to-the-index"></a>將檔案類型新增至索引

增益集可以擴充 WDS 以建立新的或專屬檔案類型的索引，並將每個新的檔案類型與特定檔案的圖示或內容功能表產生關聯。 若要這樣做，您可以建立並註冊增益集，以：

1.  為每個檔案類型執行 [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)介面，讓 WDS 可以存取和編制檔案類型的文字和中繼資料的索引。
2.  會執行 **IExtractIcon** 和 **ICoNtextMenu** 介面，以新增圖示和內容功能表，以提供更好的整合和可用性。

如需有關如何執行篩選的討論，請參閱 [開發 IFilter 增益集](-search-2x-wds-ifilteraddins.md)。

## <a name="adding-data-stores-to-the-index"></a>將資料存放區加入至索引

增益集可以擴充 WDS 來建立新資料存放區的索引，並將檔案與檔案特定的圖示或內容功能表產生關聯。 若要這樣做，您可以建立並註冊通訊協定處理常式，以：

1.  會執行 **ISearchProtocol** 和 **IUrlAccessor** 介面，以處理和系結內容來源中的個別專案。 WDS 會使用 Url 來唯一識別專案，不論這些專案是在檔案系統、類似資料庫的存放區內或在 Web 上。
2.  會執行 **IPersistFolder** 介面和 **IShellFolder** 介面的部分，以新增圖示和內容功能表，以提供更好的整合和可用性。

如需有關如何執行通訊協定處理常式的討論，請參閱 [開發通訊協定處理常式](-search-2x-wds-phaddins.md)。

## <a name="add-in-installer-guidelines"></a>增益集安裝程式指導方針

增益集的安裝應遵循下列指導方針：

-   安裝程式必須使用 EXE 或 MSI 安裝程式。
-   必須提供版本資訊。
-   每個安裝的增益集都必須建立 [ **新增/移除程式** ] 專案。
-   安裝程式必須接管目前增益集所瞭解的特定檔案類型或存放區的所有登錄設定。
-   如果先前的增益集遭到覆寫，安裝程式應通知使用者。
-   如果較新的增益集已覆寫先前的增益集，應該可以還原先前增益集的功能，並將它設為該檔案類型的預設增益集，或重新儲存。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[開發 IFilter 增益集](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[開發通訊協定處理常式](-search-2x-wds-phaddins.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
