---
description: 從 Windows Installer 版本3.0 開始，修補程式作者可以使用安裝程式所快取的產品基準，更輕鬆地以較小的 delta 修補程式來服務應用程式。
ms.assetid: ab5b193d-79ce-4ed4-af53-89a4197197c1
title: 減少修補程式大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa365e831ab8685073347dc254bac58269135f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981564"
---
# <a name="reducing-patch-size"></a>減少修補程式大小

從 Windows Installer 版本3.0 開始，修補程式作者可以使用安裝程式所快取的產品基準，更輕鬆地以較小的 delta 修補程式來服務應用程式。 在許多情況下，將服務資訊傳遞給應用程式的 [*delta 修補*](d-gly.md) 程式，可能會比提供相同資訊的完整檔案修補程式或安裝套件小得多。

**Windows Installer 2.0：** 不支援。 從 Windows Installer 3.0 開始，安裝程式會選擇性地儲存更新檔案時的相關基準資訊。

Windows Installer 提供三種方法來更新和服務應用程式： [小型更新](small-updates.md)、 [次要升級](minor-upgrades.md)和 [主要升級](major-upgrades.md)。 小型更新也稱為快速修正工程 (QFE) 更新，而次要升級也稱為 service pack (SP) update。 一般的主要升級會移除先前的應用程式，並安裝新的應用程式。 Windows Installer 可以將服務資訊以 [安裝套件](installation-package.md) 的形式提供給應用程式 ( .msi 檔案) 或作為 [修補套件](patch-packages.md) ( .msp 檔) 。

針對小型更新或次要升級提供服務資訊的 Windows Installer 修補套件，通常比提供相同服務資訊的對等安裝套件小很多。 建議將修補套件用於小型和次要升級的散發。 建議您將安裝套件用於散發主要升級。

Windows Installer 修補程式 ( .msp 檔) 可以從完整的檔案或檔案差異產生， (也稱為檔案差異。 ) 從檔案差異產生的 Windows Installer 修補程式可能會比對等的完整檔案修補程式小得多。 所有版本的 Windows Installer 都可以使用完整檔案修補程式或 delta 修補程式。

從 Windows Installer 版本3.0 開始，安裝程式會選擇性地儲存更新檔案時的相關基準資訊。  (RTM 版本) 的原始基底應用程式相關資訊，以及最新的次要升級 (service pack) 會在應用程式安裝或收到次要升級時儲存在私人位置。

安裝程式會執行下列動作，以將基準快取的大小降至最低：

-   每個應用程式都不會維護兩個以上的基準：原本發行 (RTM) 的檔案基準，以及最新次要升級 (service pack 中的檔案基準。 ) 
-   在修補檔案之前，不會將檔案新增至快取。 基準快取是寫入時複製。
-   如果從未更新過應用程式，基準快取中沒有任何檔案。
-   當應用程式的最後一項服務是 (service pack 的次要升級時) 應用程式位於基準層級，而且電腦上最多可以有兩個檔案複本。 其中一個檔案複本位於安裝的目標目錄中。 另一個複本可以位於 RTM 基準快取中。
-   當應用程式的最後一項服務是小型更新時 (QFE) 應用程式不在基準層級，而且電腦上最多可以有三個檔案複本。 檔案的第一個複本位於安裝的目標目錄中。 檔案的第二個複本位於 RTM 基準快取中。 檔案的最後一個複本是最新的基準快取。
-   卸載產品時，會移除應用程式的基準快取。

從 Windows Installer 版本3.0 開始，當修補程式套用至應用程式時，安裝程式可以使用基準快取。 您可以使用基準資訊來套用差異修補程式，或在卸載修補程式期間將檔案還原為先前的版本。 這可以讓修補程式作者受益于較小的差異修補程式。 如果安裝程式發現 delta 修補程式無法套用至目標檔案，則安裝程式會嘗試使用儲存在基準快取中的檔案做為起始點。 安裝程式只會在嘗試快取中的所有可能性之後，才要求原始安裝來源。

遵循下列指導方針可協助修補作者使用 Windows Installer 3.0 版修補程式和基準快取來建立較小的 delta 修補程式：

-   撰寫包含 [MsiPatchSequence 資料表](msipatchsequence-table.md)的修補程式。 需要有此資料表才能使用基準快取，從 Windows Installer 版本3.0 開始提供。
-   請勿設定防止基準快取的原則。 [MaxPatchCacheSize](maxpatchcachesize.md)原則的值會指定可用磁碟空間的最大百分比。 如果 MaxPatchCacheSize 原則設定為0，則基準快取中不會儲存任何其他檔案。 如果未設定此原則，則預設值為最多可使用10% 的磁碟空間。 如果快取的總大小達到磁碟空間的最大百分比，則不會儲存任何其他檔案。 原則不會影響已儲存的檔案。 即使停用快取，安裝程式還是可以使用現有的產品基準快取。
-   如果套用的第一個修補套裝程式含 [MsiPatchSequence 資料表](msipatchsequence-table.md)，則會為應用程式啟用快取。
-   如果服務交易中的任何修補程式未包含 [MsiPatchSequence 資料表](msipatchsequence-table.md)，則只有在包含 MsiPatchSequence 資料表的次要升級修補程式 (service pack) 已成功套用至產品時，才會為應用程式啟用快取。
-   使用修補程式建立工具產生修補程式套件，例如 [Msimsp.exe](msimsp-exe.md) 和 [PATCHWIZ.DLL](patchwiz-dll.md)。
-   請一律以應用程式 RTM 版本的修補程式為目標，或 (service pack) 版本的應用程式進行次要升級。 在 Patch 建立屬性 (PCP) 檔案的 [TargetImages 資料表](targetimages-table-patchwiz-dll-.md) 中指定的目標應該是 [**ProductVersion**](productversion.md) 屬性的前三個欄位所定義的產品檢查點。
-   絕對不要將修補程式的目標設為小型更新映射。 建立修補程式的目標不應包含先前的小型更新升級映射。

 

 



