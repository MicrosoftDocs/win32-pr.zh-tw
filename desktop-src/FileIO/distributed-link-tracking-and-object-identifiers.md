---
description: 分散式連結追蹤服務可讓用戶端應用程式追蹤已移動的連結來源。
ms.assetid: 6f438c72-f23d-4ca4-83bd-fe3bc433ceeb
title: 分散式連結追蹤和物件識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6077ec45f99543f42ec8ad61b3763dab4b2a56d6e555832acdc2b3e66feaee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117997660"
---
# <a name="distributed-link-tracking-and-object-identifiers"></a>分散式連結追蹤和物件識別碼

使用路徑和檔案名儲存檔案或目錄的參考並不可靠。 如果使用者重新命名檔案，則會中斷檔案的連結。 如果使用者重新命名目錄，它會中斷檔案的連結，以及目錄樹狀結構中的所有檔案和子目錄。

**分散式連結追蹤服務** 可讓用戶端應用程式追蹤已移動的連結來源。 訂閱連結追蹤服務的用戶端可以維持其參考的完整性，並以對使用者而言是透明的方式來追蹤物件。

## <a name="object-identifiers"></a>物件識別碼

連結追蹤服務會使用 **物件識別碼 (識別碼)** 來維護物件的連結。 物件識別碼是選擇性的屬性，可唯一識別磁片區上的檔案或目錄。

所有物件識別碼的索引都會儲存在磁片區上。 重新命名、備份和還原作業會保留物件識別碼。 不過，複製作業並不會保留物件識別碼，因為這樣會違反其唯一性。

您可以對物件識別碼執行下列作業：

-   建立
-   刪除
-   查詢

當您建立物件識別碼時，您會建立連結追蹤服務的檔案身分識別。 相反地，當您刪除物件識別碼時，連結追蹤服務會停止維護檔案的連結。 如需對物件識別碼執行作業的檔案系統控制程式代碼清單，請參閱檔案 [管理控制程式代碼](file-management-control-codes.md)。

分散式連結追蹤服務會追蹤 shell 快捷方式的連結來源，以及 NTFS 檔案系統磁片區中的 OLE 連結。 連結用戶端可以修正中斷的連結，其中包含連結來源新位置的更新資訊。

## <a name="link-tracking-features"></a>連結追蹤功能

Shell 快速鍵包含使用樹狀目錄搜尋演算法的啟發式連結追蹤，以找出與移動的連結來源相符的結果。 搜尋演算法是根據檔案的最後一個已知路徑，以及包含建立日期、檔案大小和檔案名與副檔名的檔案資訊。

OLE 連結包含相同的啟發式連結追蹤。 Windows 也包含相同的啟發式連結追蹤，其中有一些額外的增強功能，可讓您在某些常見的案例中，搜尋命名空間來產生結果。 這些增強功能包括下列程式，取決於用戶端應用程式所加諸的時間限制。

**搜尋命名空間**

1.  從最後一個目錄搜尋四個目錄層級。
2.  向上移動一個目錄，然後重複步驟1和2，這三次可能會產生結果（如果物件已移到附近）。
3.  從桌面根目錄向下搜尋四個層級，如果物件已移至相同桌面上的位置，則會產生結果。
4.  從每個本機固定磁片磁碟機上的根目錄搜尋四個層級。
5.  重複步驟1-3，而不包含四個目錄限制。

> [!Note]  
> 這些連結追蹤配置對終端使用者而言是透明的。 不過，它們不一定會產生正面的結果，而且可能相當耗時。

 

如需有關 shell 快速鍵的詳細資訊，請參閱 [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)。

如需 OLE 連結的詳細資訊，請參閱 [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink)。

如果在 NTFS 3.0 或更新版本上對檔案進行連結，而檔案移至相同網域中具有 NTFS 3.0 或更新版本的任何其他磁片區，則追蹤服務可以找到該檔案，但受限於時間考慮。 此外，如果檔案是移至網域或工作組內，則會找到該檔案。

若要取得 NTFS 版本的磁片區，請使用系統管理員存取權限開啟命令提示字元，然後執行下列命令：

**fsutil fsinfo ntfsinfo** *X ** * *：*

其中 *X* 是磁片區的磁碟機號。

在檔案中建立連結時，會將目標檔案視為 **連結來源**，而連結的建立者會是 **連結用戶端**。 例如，如果建立了 shell 快捷方式來連結到文字檔，則文字檔是連結來源，而 shell 快捷方式是連結用戶端。

分散式連結追蹤服務會在網域內發生的下列情況中維護檔案連結：

-   連結來源檔案會從一個 NTFS 檔案系統磁片區移至相同網域中的另一個磁片區。
-   保存連結來源的電腦名稱稱已重新命名。
-   連結來源電腦上的網路共用已變更。
-   保存連結來源檔案的磁片區會移至相同網域中的另一部電腦。

分散式連結追蹤服務也會嘗試在先前的情況下維持連結，即使它們不是在網域內（也就是跨網域或工作組內）也不會發生。 連結來源電腦上的網路共用變更時，一律可以在這些情況下維護連結。 當連結來源在電腦內移動時，也可以進行維護。 連結來源移至另一部電腦時，通常可以維持連結，但是這種形式的追蹤在一段時間內會較不可靠。

## <a name="link-tracking-functionality"></a>連結追蹤功能

連結追蹤功能主要是以下列兩個系統服務的形式來執行：

-   散佈式連結追蹤用戶端
-   分散式連結追蹤伺服器

<dl> <dt>

<span id="Distributed_Link_Tracking_Client"></span><span id="distributed_link_tracking_client"></span><span id="DISTRIBUTED_LINK_TRACKING_CLIENT"></span>分散式連結追蹤用戶端
</dt> <dd>

分散式連結追蹤用戶端會在所有電腦上執行，並管理該電腦的連結追蹤活動。 這些活動包括搜尋連結來源和處理連結來源移動。 手機連結來源之後，服務會將資訊傳遞至在網域控制站上執行的分散式連結追蹤伺服器。

</dd> <dt>

<span id="Distributed_Link_Tracking_Server"></span><span id="distributed_link_tracking_server"></span><span id="DISTRIBUTED_LINK_TRACKING_SERVER"></span>分散式連結追蹤伺服器
</dt> <dd>

分散式連結追蹤伺服器會在網域中的每個網域控制站上執行。 服務會接受從電腦上的追蹤服務移動檔案和磁片區的通知，並允許分散式連結追蹤用戶端查詢連結來源的目前位置。

此伺服器服務會在網域控制站中維護已移動之磁片區和檔案的相關資訊。 移動的相關資訊不能增加超過特定大小，並且會在不必要的情況下自動移除。

</dd> </dl>

連結追蹤服務是由 [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka) 和 [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) 介面所公開。 因此，shell 快捷方式會使用它們。 當呼叫 [**IShellLink：： Resolve**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) 方法且找不到參照檔案時（例如，當使用者啟動 shell 快捷方式時），系統會自動呼叫追蹤服務來尋找檔案。 同樣地，當 [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) 執行在其 [**BindToSource**](/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource) 方法中找不到檔案時，它會自動在追蹤服務上呼叫。

## <a name="link-tracking-limitations"></a>連結追蹤限制

分散式連結追蹤服務僅適用于 NTFS 檔案系統，且僅適用于 NTFS 3.0 或更新版本上的連結來源。 因此，如果連結來源移至 FAT 檔案系統磁片區，則追蹤資訊會遺失。 此外，如果在 NTFS 3.0 或更新版本之間手機連結來源，但正在執行移動的電腦正在執行舊版 Windows，則會遺失連結追蹤資訊。 當連結追蹤資訊遺失時，連結來源檔案本身不會有任何損害，因為分散式連結追蹤服務並不會可追蹤。

若要取得 NTFS 版本的磁片區，請使用系統管理員存取權限開啟命令提示字元，然後執行下列命令：

**fsutil fsinfo ntfsinfo** *X ** * *：*

其中 *X* 是磁片區的磁碟機號。

不會維護卸載式媒體上的檔案連結。 此外，追蹤服務無法辨識新的 NTFS 檔案系統磁片區，直到系統重新開機為止。 由於重新分割、將 FAT 檔案系統磁片區重新格式化為 NTFS 檔案系統，或連接新的外部磁片磁碟機，因此新的磁片區可能會變成可用。

 

 
