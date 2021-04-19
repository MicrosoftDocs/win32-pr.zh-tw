---
description: 概述 Windows 7 的程式庫簡介。
ms.assetid: 83c47963-4c8e-45ee-b707-bd45cfe048cd
title: Windows 7 中的 windows Shell 程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb94551d80d0230966626f1bd6499801aff889c4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106986004"
---
# <a name="windows-shell-libraries-in-windows"></a>Windows 中的 windows Shell 程式庫

本主題概述 Windows 7 和更新版本的程式庫簡介。 程式庫是 Windows Shell 的功能。 若要存取 Windows Shell 功能，例如程式庫，Windows Search 應用程式的協力廠商開發人員必須先執行 Shell 資料存放區。 如需詳細資訊，請參閱 [執行基本資料夾物件介面](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))。

本主題的組織方式如下：

- [程式庫](#libraries)
  - [使用者資料進入點](#user-data-entry-points)
  - [資料夾集合](#collections-of-folders)
  - [程式庫中支援的資料夾](#supported-folders-in-libraries)
  - [儲存體支援](#storage-backed)
  - [非檔案系統 Shell 容器](#non-file-system-shell-containers)
  - [程式庫描述](#library-descriptions)
- [相關主題](#related-topics)

## <a name="libraries"></a>程式庫

在 Windows 7 和更新版本中，程式庫是使用者資料的預設存放庫。 使用者可以使用與在資料夾中相同的方式流覽檔案，也可以依屬性（例如日期、類型和作者）來查看其檔案。 與資料夾不同的是，程式庫不會實際儲存專案，而是同時顯示儲存在數個資料夾中的檔案。 程式庫提供單一存取點，而豐富的視圖會對其匯總內容的使用者進行透視。 比方說，如果使用者除了 [ **我的音樂** ] 資料夾之外，還在外部磁片磁碟機上的資料夾中有音樂檔案，則他們可以透過「音樂」媒體櫃立即存取所有音樂檔案。

### <a name="user-data-entry-points"></a>使用者資料進入點

預設程式庫 (例如 **我的檔**、 **我的圖片** 等等) 相當於 [已知資料夾](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85))。 預設程式庫會為使用者提供熟悉的進入點，但由於文件庫內容不限於已知的資料夾內容庫，讓使用者能夠更自由地判斷檔和媒體的儲存位置。 程式庫會透過 Shell 命名空間 (Shell 資料來源) 公開。 您的應用程式可以藉由啟用程式庫感知和流覽功能，為使用者提供與資料相同的熟悉進入點。

### <a name="collections-of-folders"></a>資料夾集合

程式庫是使用者定義的內容集合。 Windows Search 在程式庫中包含資料夾時，將支援的資料夾編制索引。 這可讓您立即搜尋，以及程式庫中以屬性為基礎的堆疊排列檢視。

### <a name="supported-folders-in-libraries"></a>程式庫中支援的資料夾

針對程式庫中支援的資料夾，這些檔案必須可在本機電腦上編制索引，並在遠端 Windows 電腦上編制索引，或在伺服器上以 Windows Search 索引的檔案編制索引。

使用者無法在 [Windows 程式庫管理] 對話方塊中新增不支援的資料夾。 如果使用 [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) API 將非索引的遠端資料夾新增至程式庫，則程式庫使用者體驗會還原為程式庫 **安全模式**。 在 **安全模式** 功能（例如屬性型堆疊排列檢視、篩選建議和 [ **開始] 功能表** 搜尋支援）會從受影響的程式庫中移除。

下表列出使用 Windows 檔案總管程式庫管理對話方塊所包含的程式庫中的資料夾，以及 **安全模式** 中不支援的資料夾：

| 支援的資料夾                                                                                                                            | 不支援的資料夾                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| 固定和外部 NTFS 和 FAT32 硬碟                                                                                                | 抽取式磁碟機 (例如 thumbdrives 和 SD 卡)                                                      |
| 由 Windows Search (編制索引的共用，例如部門伺服器，以及執行 Windows 10 的電腦和 Windows 7 Home edition)  | 卸除式媒體 (例如 Cd 和 Dvd)                                                                   |
| 可離線 (的共用，例如重新 **導向我的檔**、 **用戶端** 快取)                                                | 無法離線使用或遠端索引的網路共用 (例如 NAS 磁片磁碟機)              |
| n/a                                                                                                                                          | 其他資料來源 (例如 Microsoft SharePoint、Microsoft Exchange、Microsoft OneDrive 等)  |

### <a name="storage-backed"></a>Storage-Backed

程式庫是儲存體資料夾的集合。 使用者可以直接儲存檔案，並將檔案複製到文件庫，因為每個文件庫都有預設的儲存位置，可將這些檔案傳送到其中。 針對預設程式庫，這是包含在程式庫中的使用者已知資料夾 (例如 **我的檔**) ，或新增至自訂程式庫的第一個資料夾。 這是當使用者將檔案拖曳至文件庫，或使用 [一般檔案] 對話方塊儲存至程式庫時，檔案的所在資料夾。 使用者可以在任何時間點變更文件庫的預設儲存位置，但如果她移除預設的儲存位置，則會選取程式庫中的下一個資料夾做為新的儲存位置。 使用者可以另外儲存至程式庫中已包含許可權的任何資料夾。

### <a name="non-file-system-shell-containers"></a>非檔案系統 Shell 容器

程式庫可以包含檔案系統 Shell 容器（例如 **電腦** 和 **主控台**），但包含檔案系統專案。 您可以使用舊版作業系統中檔案系統檔案和資料夾的 Api 來列舉和存取程式庫資料夾和內容。 如果您的應用程式非常依賴檔案系統專屬的 Api，則可以使用 [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) API 來取得程式庫中資料夾和檔案的檔案系統路徑。 在大部分情況下，建議您使用 Shell 程式設計模型，以支援多個 Windows 版本和專案彈性。 如需詳細資訊，請參閱 [流覽 Shell 命名空間](https://msdn.microsoft.com/library/dd378496(VS.85).aspx)。

### <a name="library-descriptions"></a>程式庫描述

程式庫描述會以 XML 檔案的形式儲存在% appdata% Microsoft \\ Windows library \\ 資料夾 (中，而且可能會以 **FOLDERID 連結 \_ 庫** 的形式儲存在磁片上。 如需 FOLDERID 連結 **\_ 庫** 的詳細資訊，請參閱 [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)。

程式庫說明檔是副檔名為 library-ms 的 XML 檔。 應用程式永遠不能存取或編輯這些檔案。 保存在程式庫描述檔案中的資料夾路徑文字不一定是最新的。 程式庫資料夾會以序列化的二進位 [Shell 連結](/windows/desktop/shell/links) 格式保存在程式庫描述檔案中。 如需程式庫和程式庫描述架構的詳細資訊，請參閱連結 [庫描述架構](../shell/library-schema-entry.md)。 如需同盟搜尋連接器和搜尋連接器描述架構的詳細資訊，請 [搜尋連接器描述架構](search-sconn-desc-schema-entry.md)。

> [注意]  
> 應用程式應該一律使用 Shell 程式設計模型或 [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) API 來取用和操作程式庫內容，而且永遠不會嘗試手動存取或編輯程式庫描述檔案。

## <a name="related-topics"></a>相關主題

[Windows 7 搜尋](./-search-3x-wds-overview.md)

[適用于 Windows 7 搜尋的新](new-for-windows-7-search.md)

[在 Windows 7 中編制優先順序和資料列集事件的索引](indexing-prioritization-and-rowset-events.md)