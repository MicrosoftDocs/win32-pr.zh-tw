---
description: 描述檔案緩衝的應用程式控制考慮，也稱為未緩衝的檔案輸入/輸出 (i/o) 。
ms.assetid: ae1e5d0f-9b55-4aae-8402-b9c8e33d9363
title: 檔案緩衝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f6724622b2c3116fa24a6109efb6c0d9f1d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194758"
---
# <a name="file-buffering"></a>檔案緩衝

本主題涵蓋檔案緩衝的應用程式控制的各種考慮，也稱為未緩衝的檔案輸入/輸出 (i/o) 。 檔案緩衝通常是由系統在幕後處理，除非另有指定，否則會被視為 Windows [作業系統內檔案](file-caching.md) 快取的一部分。 雖然「快取 *」和「* *緩衝* 處理」有時會交替使用，但本主題只會在說明如何與)  (未快取的資料進行互動的內容中使用「 *緩衝區* 」一詞，而在其他情況下，使用者模式應用程式的直接控制也是如此。

使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式開啟或建立檔案時，不能指定檔案 **\_ 旗 \_ \_** 標來停用從檔案讀取或寫入資料的系統快取。 雖然這可讓您完整且直接控制資料 i/o 緩衝，但在檔案和類似的裝置中，也需要考慮資料的對齊需求。

> [!Note]  
> 這種對齊方式資訊適用于裝置上的 i/o，例如支援搜尋的檔案，以及檔案位置指標 (或 *位移*) 的概念。 針對未搜尋的裝置（例如具名管道或通訊裝置），關閉緩衝可能不需要任何特定的對齊方式。 在該情況下，可能會因一致而獲得的任何限制或效率，取決於基礎技術。

 

在簡單的範例中，應用程式會使用「檔案」 **\_ 旗標 \_ 無 \_ 緩衝** 旗標來開啟檔案以進行寫入存取，然後使用在應用程式內定義的資料緩衝區來執行 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) 函式的呼叫。 在這些情況下，這個本機緩衝區實際上是此作業唯一存在的檔案緩衝區。 由於實體磁片配置、檔案系統儲存配置以及系統層級的檔案指標位置追蹤，除非本機定義的資料緩衝區符合某些對齊準則（如下一節所述），否則此寫入作業將會失敗。

> [!Note]  
> 快取的討論不會考慮實體磁片本身的任何硬體快取，這在任何情況下都不保證會在系統的直接控制內。 這不會影響此主題中指定的需求。

 

如需檔案旗標 **如何 \_ \_ 無 \_ 緩衝** 與其他快取相關旗標互動的詳細資訊，請參閱 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)。

## <a name="alignment-and-file-access-requirements"></a>對齊和檔案存取需求

如前所述，應用程式必須符合特定需求，才能使用檔案旗標（ **\_ \_ 沒有 \_ 緩衝**）開啟的檔案。 適用下列細節：

-   檔案存取大小（包含重 [**迭結構中的選擇性**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) 檔案位移，如果有指定）必須是磁片區磁區大小的整數倍數的位元組數目。 例如，如果磁區大小為512個位元組，則應用程式可以要求512、1024、1536或2048位元組的讀取和寫入，但不能要求335、981或7171位元組。
-   讀取和寫入作業的檔案存取緩衝區位址應該是實體磁區對齊的，這表示在記憶體中的位址與磁片區的實體磁區大小的整數倍數相符。 視磁片而定，可能不會強制執行這項需求。

應用程式開發人員應該注意到市場中新的存放裝置類型，其實體媒體磁區大小為4096個位元組。 這些裝置的產業名稱是「Advanced Format」。 因為可能會有直接導入4096個位元組的相容性問題作為媒體的定址單位，所以暫時性的相容性解決方案是引進可模擬一般512位元組磁區存放裝置的裝置，但透過標準 ATA 和 SCSI 命令提供真正磁區大小的相關資訊。

這種模擬的結果是，開發人員必須瞭解的兩個磁區大小：

-   邏輯磁區：用於邏輯區塊定址媒體的單位。 我們也可以將它視為儲存體可接受的最小寫入單位。 這是「模擬」。
-   實體磁區：裝置的讀取和寫入作業會在單一作業中完成的單位。 這是不可部分完成的寫入單位，以及需要對齊的非緩衝 i/o，以達到最佳效能和可靠性特性。

最新的 Windows Api （例如 [**IOCTL \_ 磁片 \_ 取得磁片 \_ 磁碟機 \_ 幾何**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_geometry)和 [**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)）將會傳回邏輯磁區大小，但可透過 [**IOCTL \_ 儲存體 \_ 查詢 \_ 屬性**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property)控制項程式碼抓取實體磁區大小，並在 [**儲存體 \_ 存取 \_ 對齊 \_ 描述**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor)元結構中包含 **BytesPerPhysicalSector** 成員所含的相關資訊。 如需範例，請參閱 [**儲存體 \_ 存取 \_ 對齊 \_ 描述**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor)項的範例程式碼。 Microsoft 強烈建議開發人員將未緩衝的 i/o 對齊，如 **IOCTL \_ 儲存體 \_ 查詢 \_ 屬性** 控制項程式碼所報告的實體磁區大小，以協助確保其應用程式已針對此磁區大小轉換做好準備。

**Windows Server 2003 和 WINDOWS XP：** 無法使用 [**儲存體 \_ 存取 \_ 對齊 \_ 描述**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_access_alignment_descriptor) 元結構。 它是在 Windows Vista 和 Windows Server 2008 中引進的。

由於讀取和寫入作業的緩衝區位址必須為磁區對齊，因此應用程式必須能夠直接控制這些緩衝區的配置方式。 磁區對齊緩衝區的其中一種方式是使用 [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) 函數來配置緩衝區。 請考慮下列事項：

-   [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) 配置的記憶體會對齊系統的頁面大小的整數倍數的位址。 針對 Itanium 型系統，頁面大小為 x64 和 x86 或8192位元組上的4096個位元組。 如需詳細資訊，請參閱 [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) 函數。
-   對於直接存取存放裝置而言，磁區大小通常是512到4096位元組 (硬碟) ，而2048位元組適用于光碟。
-   頁面和磁區大小都是2的乘冪。

因此，在大部分情況下，頁面對齊的記憶體也會對齊磁區，因為磁區大小大於頁面大小的情況很罕見。

取得手動對齊的記憶體緩衝區的另一種方式，是使用來自 C Run-Time 程式庫的[ \_ 對齊 \_ malloc](/cpp/c-runtime-library/reference/aligned-malloc?view=vs-2019)函數。 如需如何手動控制緩衝區對齊的範例，請參閱 [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)的範例程式碼一節中的 c + + 語言程式碼範例。

 

 
