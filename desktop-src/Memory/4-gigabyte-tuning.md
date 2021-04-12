---
description: 4 gb 調整： BCDEdit 和 Boot.ini
ms.assetid: 991eb86f-9e6f-4084-8b6f-f979e42104b5
title: 4 gb 調整： BCDEdit 和 Boot.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f997ae09748370d5ec8ec246da80b6440d7aaf45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192658"
---
# <a name="4-gigabyte-tuning-bcdedit-and-bootini"></a>4 gb 調整： BCDEdit 和 Boot.ini

在32位版本的 Windows 上，應用程式有 4 gb 的可用虛擬位址空間 (GB) 。 虛擬位址空間已分割，因此應用程式可以使用 2 GB，而其他 2 GB 僅供系統使用。 4 gb 調整 (4GT 或 4GT RAM 調整) 功能（使用 *BCDEdit/set increaseuserva* 命令啟用）會增加應用程式可用的虛擬位址空間（最多 3 GB），並將可供系統使用的空間減少為1到 2 gb。

對於需要海量儲存體的應用程式（例如 (DBMS) 的資料庫管理系統），使用較大的虛擬位址空間可提供可觀的效能和擴充性優勢。 不過，檔案快取、分頁集區和非分頁集區較小，可能會對具有大量網路或 i/o 的應用程式造成負面影響。 因此，您可能會想要在負載下測試您的應用程式，並檢查效能計數器，以判斷您的應用程式是否受益于較大的位址空間。

若要啟用4GT，請使用 [BCDEdit/set](/windows-hardware/drivers/devtest/bcdedit--set) 命令將 **increaseuserva** 開機專案選項設定為介於 2048 (2 GB) 和 3072 (3 GB) 之間的值。

**Windows Server 2003 及更早版本：** 若要啟用4GT，請將 **/3gb** 參數新增至 Boot.ini 檔案。 下列系統支援 **/3gb** 參數：

-   Windows Server 2003
-   Windows XP Professional

**/3gb** 參數會為應用程式提供完整的 3 GB 虛擬位址空間，並將系統可用數量減少為 1 GB。 在 Windows Server 2003 上，可以調整應用程式可用的位址空間量，方法是將 Boot.ini 中的 **/USERVA** 參數設定為介於2048和3072之間的值，這樣會增加系統可用的位址空間量。 當應用程式需要 2 GB 以上的位址空間時，這有助於維護整體系統效能。

若要讓應用程式使用較大的位址空間，請在映射標頭中設定 [**影像檔案的 \_ \_ 大型 \_ 位址 \_ 感知**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) 旗標。 Microsoft Visual C++ 隨附的連結器支援 **/LARGEADDRESSAWARE** 參數，以設定此旗標。 設定此旗標，然後在沒有4GT 支援的系統上執行應用程式時，應該不會影響應用程式。

在64位版本的 Windows 中，以 [**圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) 旗標標記的32位應用程式有 4 GB 的可用位址空間。

**Itanium 版本的 Windows Server 2003：** 在 SP1 之前，32位進程只有 2 GB 的位址空間可用。

使用下列指導方針來支援應用程式中的4GT：

-   接近 2 GB 界限的位址通常會由各種系統 Dll 使用。 因此，即使有整個 4 GB 的位址空間可供使用，32位程式也無法配置超過 2 GB 的連續記憶體。
-   若要取得總使用者虛擬空間的數量，請使用 [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) 函數。 若要取得可能的最高使用者位址，請使用 [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) 函數。 一律在執行時間偵測實際值，並避免使用硬式有線常數定義，例如： `#define HIGHEST_USER_ADDRESS 0xC0000000` 。
-   避免與指標進行簽署的比較，因為它們可能會導致應用程式在啟用4GT 的系統上損毀。 在 2 GB 以上的指標，如下所示的條件為 false： `if (pointer > 40000000)` 。
-   當4GT 啟用時，針對應用程式定義目的使用指標最高位的程式碼將會失敗。 例如，如果32位字低於0x80000000，可能會被視為使用者模式位址，如果有的話，則會被視為錯誤碼。 這對4GT 的情況並不成立。

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 通常會傳回較高位址之前的低位址。 因此，除非配置海量儲存體或有分散的虛擬位址空間，否則您的進程可能不會使用非常高的位址。 若要強制配置在較低位址之前從較高的位址配置以供測試之用，請在呼叫 **VirtualAlloc** 或將下列登錄值設定為0x100000 時，指定 [**記憶體 \_ 上限 \_** ]：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制** \\ **會話管理員** \\ **記憶體管理** \\ **AllocationPreference**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 版本的記憶體限制](memory-limits-for-windows-releases.md)
</dt> <dt>

[實體位址擴充功能](physical-address-extension.md)
</dt> <dt>

[4 GT 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))
</dt> </dl>

 

 
