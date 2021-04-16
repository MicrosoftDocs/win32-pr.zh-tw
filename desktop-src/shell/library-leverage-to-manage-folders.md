---
description: 本主題說明什麼是程式庫，以及它們如何受益于使用者和開發人員。
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: 關於程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e577e7b5df0a1e072a07a096434af84ff8e2c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563030"
---
# <a name="about-libraries"></a>關於程式庫

本主題說明什麼是程式庫，以及它們如何受益于使用者和開發人員。

程式庫是使用者定義的資料夾集合。 程式庫會持續追蹤每個資料夾的實體儲存位置，以免除使用者和該工作的軟體。 使用者可以在程式庫中將相關資料夾群組在一起，即使這些資料夾儲存在不同的硬碟或不同的電腦上也一樣。

在文件庫中，資料夾和檔案會以單一集合的形式顯示給使用者，而使用 Shell 程式庫 API，程式庫的內容也可能會出現在程式的單一位置中。

在文件庫中，內容（例如使用者的檔、相片、影片或音樂）可以依使用者的需要排序並顯示，而不像檔案系統的需求。 例如，使用者可以使用程式庫中專案的屬性來組織文件庫的內容，如此一來，即使相關專案儲存在不同的資料夾中，也會一起排序。

![程式庫使用者介面的螢幕擷取畫面](images/libraries-whatare.png)

本主題內容：

-   [程式庫優點](#library-benefits)
    -   [使用者權益](#user-benefits)
    -   [開發人員權益](#developer-benefits)
-   [管理程式庫中的資料夾](#managing-folders-in-libraries)
-   [相關主題](#related-topics)

## <a name="library-benefits"></a>程式庫優點

本節將說明程式庫從終端使用者的觀點和程式開發人員觀點的一些優點。

### <a name="user-benefits"></a>使用者權益

將程式庫支援新增至您的程式，可為使用者提供下列優點：

-   **程式庫在 Windows 7 中提供一致的使用者介面**

    [一般檔案] 對話方塊支援程式庫，並提供與 Windows 7 中的 Windows 檔案總管相同的使用者體驗。 當您在 Windows 7 中使用程式時，您程式中的支援程式庫將有助於為使用者提供更順暢的互動。

-   **使用者決定儲存內容的位置**

    程式庫讓使用者可以控制其內容的儲存位置。 同時，程式庫會為不想要在電腦中管理該詳細資料層級的使用者提供合理的預設值。 使用者會決定要在何處及如何儲存其內容，以及程式庫如何以任何方式運作，來控制他們想要執行的控制程度。

### <a name="developer-benefits"></a>開發人員權益

您可以使用程式中的程式庫提供更具彈性且方便的使用者介面，而不需要新增許多複雜的程式碼。 新增程式庫支援的一些優點包括：

-   **程式庫支援程式庫和檔案系統存取**

    使用 [**Shell 程式庫 API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)，程式可以為使用者提供程式庫支援，同時減少其檔案和資料夾管理程式碼的複雜度。 如果您的程式已使用檔案系統 API，您可以視需要保留大部分的現有程式碼，並藉由從 **Shell 程式庫 API** 取得必要的檔案系統資訊，為使用者提供程式庫支援。

-   **更簡單的變更通知**

    當受監視資料夾或程式庫的內容變更時，檔案系統和 Shell API 都可以通知您的程式。 不過，您可以使用 Shell API 來監視程式庫中的所有資料夾，並使用單一通知，即使程式庫中的資料夾可能儲存在不同的磁片磁碟機或甚至不同的電腦上也一樣。

-   **程式庫使用檔案屬性**

    程式可以使用檔案屬性，控制在開啟和儲存使用一般檔案對話方塊的作業期間所顯示的檔案。 程式也可以使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面存取檔案屬性。 您也可以設定 [一般檔案] 對話方塊，讓使用者更新與其內容相關聯的屬性。

-   **程式可以建立專用程式庫**

    當現有的使用者程式庫不符合程式的需求時，就可以建立新的程式庫，例如，如果程式建立新類型的使用者內容。 您可以使用代表其內容的唯一圖示來設定新的程式庫，並讓程式庫易於在 Windows 檔案總管中識別。

## <a name="managing-folders-in-libraries"></a>管理程式庫中的資料夾

使用者可以藉由新增、移動或移除文件庫中的資料夾來組織其程式庫。 不過，並非所有資料夾都支援文件庫可提供的所有功能。 許多程式庫功能都需要快速存取資料夾的不同屬性，以及只能透過 Windows Search 使用的內容。 若要提供完整的程式庫功能，必須能夠 Windows Search 的資料夾編制索引。

程式庫不允許使用者新增未提供完整程式庫功能的資料夾。 不過， [**Shell 程式庫 API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) 可以新增這類資料夾。 如果程式庫包含不支援完整程式庫功能的資料夾，程式庫將在安全模式下運作，並提供有限的功能。 下表說明支援完整程式庫功能的資料夾，以及不支援這些功能的資料夾。



| 支援完整程式庫功能的資料夾類型                                                               | 不支援完整程式庫功能的資料夾類型                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| 固定和外部 NTFS 和 FAT32 硬碟。                                                                     | 抽取式磁碟機（例如 USB 快閃磁片磁碟機）或安全的數位 (SD) 記憶卡。               |
| 由 Windows Search （例如部門伺服器、Windows 7 或 Windows Vista 家用電腦）編制索引的檔案共用。 | 卸載式媒體，例如 CD-ROM 或 DVD 媒體。                                                 |
| 可離線使用的檔案共用，例如重新導向的 **我的檔** 資料夾或 Client-Side 快取。        | 無法離線使用或從遠端索引的網路共用，例如 NAS 磁片磁碟機。   |
|                                                                                                                    | 其他資料來源，例如 Microsoft SharePoint、Microsoft Exchange 和 Microsoft OneDrive。 |



 

下圖顯示在安全模式下，程式庫內容的有限顯示。

![當程式庫處於安全模式時開啟對話方塊](images/libraries-supportedfolders.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於程式庫](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Shell 連結](./links.md)
</dt> <dt>

[已知的資料夾](known-folders.md)
</dt> <dt>

[程式庫描述架構](library-schema-entry.md)
</dt> </dl>

 

 
