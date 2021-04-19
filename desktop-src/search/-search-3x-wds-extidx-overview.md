---
description: 您可以擴充 Windows Search，以使用資料增益集介面來編制新檔案格式和資料存放區的內容和屬性的索引。
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: 擴充索引 (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972607"
---
# <a name="extending-the-index-windows-search"></a>擴充索引 (Windows Search)

您可以擴充 Windows Search，以使用 [資料增益集介面](./-search-data-addins-interfaces-entry-page.md)來編制新檔案格式和資料存放區的內容和屬性的索引。 若要建立 Windows Search 增益集，協力廠商開發人員必須先執行 Shell 資料存放區，然後再開發通訊協定處理常式，讓 Windows Search 可以存取資料來編制索引。 如果您有自訂的檔案格式，您必須開發篩選處理常式來為檔案內容編制索引，以及將每個檔案類型的屬性處理常式建立為索引屬性。

Windows Search 目前支援將超過200種類型的專案編制索引 (例如 .txt、.html 和 .xml 檔案格式) 而且可以使用多種類型的資料存放區 (例如 NTFS 檔案系統和 Microsoft Outlook) 。 Windows Search 使用與 SharePoint Server 類似的篩選和通訊協定處理常式技術。 因此，如果您已經有檔案格式的執行，您可以使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 來更新要使用資料流程初始化的執行，以便讓篩選準則可以使用 Windows Search。

> [!Note]  
> 篩選處理常式、屬性處理常式和通訊協定處理常式必須以機器碼撰寫。 這是因為可能的 common language runtime (CLR) 在中執行多個增益集的進程的版本控制問題。

 

使用增益集擴充索引的這一節包含下列主題：

-   [開發篩選處理常式](-search-ifilter-conceptual.md)
-   [開發 Windows Search 的屬性處理常式](-search-3x-wds-extidx-propertyhandlers.md)
-   [開發通訊協定處理常式](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a>其他資源

如需相關的程式碼範例，請參閱 [Windows Search 程式碼範例](-search-samples-ovw.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Search 開發指南](-search-developers-guide-entry-page.md)
</dt> <dt>

[管理索引](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[以程式設計方式查詢索引](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[擴充語言資源](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
