---
description: 本主題介紹軟體的先進格式儲存裝置效果、討論應用程式如何協助支援這種類型的媒體，以及討論 Microsoft 在 Windows 7 SP1 和 Windows Server 2008 R2 SP1 引進的基礎結構，讓開發人員能夠支援這些類型的裝置。
ms.assetid: 1D2847A7-15E9-42E0-90EB-7F43E76D3E44
title: 512 位元組模擬 (512e) 磁碟相容性更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b654473fa8be5fbea997bd063df2c1f898a7d1
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107315001"
---
# <a name="512-byte-emulation-512e-disk-compatibility-update"></a>512 位元組模擬 (512e) 磁碟相容性更新

## <a name="platform"></a>平台

 **客戶** 端-windows Vista、windows 7、WINDOWS 7 SP1  
**伺服器** -windows server 2008、windows Server 2008 R2、windows Server 2008 R2 SP1  

## <a name="feature-impact"></a>功能影響

**嚴重性** -高  
**頻率** -高  









## <a name="description"></a>描述

Areal 密度是每年增加的，而最近一次出現 3 TB 的磁片時，用來處理遞減信號對雜訊比率 (SNR) 的錯誤修正機制會變得沒有效率，也就是為了確保媒體可供使用，需要增加的額外負荷量。 其中一個用來改善此錯誤修正機制的儲存體產業解決方案，是引進不同的實體媒體格式，其中包含較大的實體磁區大小。 這種新的實體媒體格式稱為 *Advanced format*。 因此，若要對新式儲存裝置的磁區大小做出任何假設，開發人員將需要研究其程式碼的基礎，以判斷是否有影響。

本主題介紹軟體的先進格式儲存裝置效果、討論應用程式如何協助支援此類型的媒體，以及討論可讓開發人員支援這些裝置類型的基礎結構。 雖然本主題中顯示的內容提供改善與 Advanced Format 磁片相容性的指導方針，但這項資訊通常適用于所有具有 Advanced Format 磁片的系統。 下列 Windows 版本提供查詢實體磁區大小的支援：

-   具有 Microsoft KB 982018 的 Windows 7
-   Windows 7 SP1
-   Windows Server 2008 R2 （含 Microsoft KB 982018）
-   Windows Server 2008 R2 SP1
-   Windows Vista 與 Microsoft KB 2553708
-   Windows Server 2008 與 Microsoft KB 2553708

如需其他詳細資訊，請參閱 [Windows 中適用于大型磁區磁片磁碟機的 Microsoft 支援原則的相關資訊](https://support.microsoft.com/kb/2510009)。

如需有關 Advanced Format 磁片的詳細資訊，請洽詢您的存放裝置廠商。

## <a name="logical-vs-physical-sector-size"></a>邏輯與實體磁區大小

以媒體格式引進這項變更的其中一項考慮，是與目前市場上目前可用的軟體和硬體相容。 做為暫時的解決方案，存放裝置產業最初推出的磁片會模擬一般的512位元組磁區磁片，但透過標準 ATA 和 SCSI 命令，提供真正磁區大小的相關資訊。 這種模擬的結果有兩個磁區大小：

-   **邏輯磁區**：用於邏輯區塊定址媒體的單位。 我們也可以將它視為儲存體可接受的最小寫入單位。 這是模擬。

-   **實體磁區**：裝置的讀取和寫入作業會在單一作業中完成的單位。 這是不可部分完成的寫入單位。

大部分目前的 Windows Api （例如 **IOCTL \_ 磁片 \_ 取得 \_ 磁片磁碟機 \_ 幾何**）都會傳回邏輯磁區大小，但可透過 [IOCTL \_ 儲存體 \_ 查詢 \_ 屬性](/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property)控制項程式碼抓取實體磁區大小，並以 [儲存體 \_ 存取 \_ 對齊 \_ 描述](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)元結構中的 **BytesPerPhysicalSector** 欄位包含相關資訊。 本文稍後會更詳細地討論。

## <a name="initial-types-of-large-sector-media"></a>大型磁區媒體的初始類型

存放裝置產業很快就能針對具有 4 KB 實體磁區大小的媒體轉換成這種新的先進格式儲存體。 有兩種類型的媒體會發佈到市場：

-   **4 KB 原生**：此媒體沒有模擬層，並且會直接公開 4 KB 作為其邏輯和實體磁區大小。 Windows 和大部分其他作業系統目前不支援此媒體。 不過，Microsoft 會在未來的 Windows 版本中，針對支援這類媒體的可行性進行調查，並在適當時發出知識庫文章。
-   **512-位元組模擬 (512e)**：此媒體具有如上一節所討論的模擬層，並公開512位元組做為其邏輯磁區大小 (類似於今日的一般磁片) ，但讓其實體磁區大小資訊 (4 KB) 可用。 這是我們目前為市場推出的數個儲存體廠商。 這種新型媒體的整體問題是，大部分的應用程式和作業系統都不了解實體磁區大小是否存在，這可能會導致一些問題，如下所述。

## <a name="how-emulation-works-read-modify-write-rmw"></a>模擬的運作方式：讀取-修改-寫入 (RMW) 

儲存媒體具有可在其中修改實體媒體的特定單位。 也就是說，媒體只能以實體磁區大小的單位來寫入或重寫。 因此，不會在此單元層級執行的寫入會需要額外的步驟，我們將在下列範例中逐步解說。

在此案例中，應用程式必須更新位於512位元組邏輯磁區內的 Datastor 記錄內容。 下圖說明存放裝置完成寫入所需的步驟：

![在512位元組邏輯磁區內升級 datastor 記錄所需的步驟](images/512ermwsteps.png)

如上所示，此程式牽涉到可能導致效能遺失的儲存裝置一些工作。 若要避免這項額外的工作，必須更新應用程式，以執行下列動作：

-   查詢實體磁區大小。
-   請確定寫入與該報告的實體磁區大小一致。

## <a name="the-resiliency-impact-of-read-modify-write"></a>讀取-修改-寫入的復原影響

復原是指應用程式在會話之間復原狀態的能力。 我們已瞭解512e 儲存體裝置在執行512位元組磁區寫入（讀取-修改-寫入迴圈）時所需的內容。 讓我們看看覆寫媒體上先前實體磁區的程式中斷時，會發生什麼事。 結果是什麼？

-   因為大部分的硬碟磁片磁碟機都有就地更新，所以實體磁區（也就是實體磁區所在的媒體部分）可能會因為部分覆寫而損毀，但不完整的資訊。 換句話說，您可以將它視為可能遺失所有8個邏輯磁區， (實體磁區以邏輯方式包含) 。

-   雖然大部分具有資料存放區的應用程式都是設計成能夠從媒體錯誤中復原、遺失八個磁區，或以另一種方式進行，否則可能會導致資料存放區無法正常復原。 系統管理員可能需要以手動方式從備份還原資料庫，或甚至可能需要執行冗長的重建。

-   另一個重要的影響是，另一個應用程式造成讀寫寫入迴圈的動作，可能會導致資料遺失（即使您的應用程式不在執行中）。 這只是因為您的資料和其他應用程式的資料都位於相同的實體磁區內。

記住這一點之後，應用程式軟體必須重新評估程式碼中所採取的任何假設，並留意邏輯實體磁區大小的差異，以及本文稍後討論的一些有趣的客戶案例。

如果您的應用程式依賴記錄結構資料存放區，則可能會發生這個問題。

## <a name="avoiding-read-modify-write"></a>避免讀取-修改-寫入

雖然有些存放裝置廠商可能會在某些512e 儲存體裝置內引進一些緩和措施，以嘗試並協助您簡化讀寫寫入迴圈的效能和復原問題，但是在工作負載方面只會有很多緩和措施可處理。 因此，應用程式不應該依賴這項緩和措施作為長期解決方案。

這項解決方案並不是磁片磁碟機的風險降低，而是讓應用程式進行正確的工作集，以避免讀寫寫入迴圈。 本節討論應用程式可能會發生大型磁區磁片問題的常見案例，並建議進行調查的途徑，以嘗試解決每個問題。

### <a name="issue-1-the-partition-is-not-aligned-to-a-physical-sector-boundary"></a>問題1：資料分割未對齊實體磁區界限

當系統管理員/使用者分割磁片時，第一個磁碟分割可能尚未在對齊的界限上建立。 這可能會導致所有後續寫入變成未對齊實體磁區界限。 從 Windows Vista SP1 和 Windows Server 2008 開始，第一個磁碟分割會放置在磁片 4 GB 或更大的磁片 (的第一個 1024 KB，否則對齊是符合 4 KB 實體磁區界限的 64 KB) 。 不過，由於 Windows XP 中的預設資料分割、協力廠商分割公用程式或 Windows Api 的使用不正確，因此建立的分割區可能無法對齊實體磁區界限。 開發人員必須確保使用正確的 Api 來協助確保對齊。 以下列出建議的 Api 以協助確保資料分割對齊。

建立新磁片區時， **IVdsPack：： CreateVolume** 和 **IVdsPack2：： CreateVolume2** api 不會使用指定的對齊參數，而是改用作業系統的對齊值預設 (windows vista sp1 將使用63個位元組，而 post windows vista sp1 將使用上述) 的預設值。 因此，建議需要建立分割區的應用程式改用 **IVdsCreatePartitionEx：： CreatePartitionEx** 或 **IVdsAdvancedDisk：： CreatePartition** api，這會使用指定的對齊參數。

協助確保對齊正確的最佳方式，就是在一開始建立資料分割時正確地進行。 否則，您的應用程式在執行寫入時或在初始化時，必須考慮調整帳戶，這可能是非常複雜的事情。 從 Windows Vista SP1 來，這通常不是問題;不過，舊版的 Windows 可以建立未配置的磁碟分割，可能會導致某些 Advanced Format 磁片的效能問題。

### <a name="issue-2-unbuffered-writes-not-aligned-to-physical-sector-size"></a>問題2：未緩衝的寫入未對齊實體磁區大小

基本問題是未緩衝的寫入與儲存媒體的回報實體磁區大小不一致，這會在可能導致效能問題的磁片磁碟機中觸發讀寫寫入。 相反地，緩衝的寫入會對齊頁面大小– 4 KB – coincidently 是第一代大型磁區媒體的實體磁區大小。 不過，大部分具有資料存放區的應用程式都會執行未緩衝的寫入，因此必須確保這些寫入是以實體磁區大小的單位來執行。

若要協助判斷您的應用程式是否發出未緩衝處理的 i/o，請在呼叫 **CreateFile** 函式時，查看 *dwFlagsAndAttributes* 參數中是否包含 **FILE \_ 旗標 \_ 無 \_ 緩衝** 旗標。

此外，如果您目前正在調整寫入至磁區大小，則此磁區大小很可能只是 *邏輯* 磁區大小，因為查詢媒體磁區大小的大部分現有 api 其實只會查詢定址單位（也就是邏輯磁區的大小）。 這裡的磁區大小是實體磁區大小，也就是不可部分完成項的實際單位。 一些可取得邏輯磁區大小的 Api 範例如下：

-   **GetDiskFreeSpace**、 **GetDiskFreeSpaceEx**
-   **FileFsVolumeInformation**
-   **IOCTL \_磁片 \_ 取得磁片 \_ 磁碟機 \_ 幾何**、 **IOCTL \_ 磁片取得磁片 \_ \_ 磁碟機 \_ 幾何 \_ 例如**
-   **IVdsDisk：： GetProperties**、 **IVdsDisk3：： GetProperties2**

**如何查詢實體磁區大小**

Microsoft 在 MSDN 上提供了程式碼範例，詳述應用程式如何查詢磁片區的實體磁區大小。 程式碼範例位於 <https://msdn.microsoft.com/library/ff800831.aspx> 。

雖然上面的程式碼範例可讓您取得磁片區的實體磁區大小，但您應該在使用之前先對所報告的實體磁區大小執行一些基本的健全檢查，因為觀察到某些驅動程式可能不會傳回格式正確的資料：

-   請確定回報的實體磁區大小 >= 回報的邏輯磁區大小。 如果不是，則您的應用程式應該使用等於所報告邏輯磁區大小的實體磁區大小。
-   確定所報告的實體磁區大小是2的乘冪。 如果不是，則您的應用程式應該使用等於所報告邏輯磁區大小的實體磁區大小。
-   如果實體磁區大小是介於 512-個位元組和 4 KB 之間的2個值，您應該考慮將實體磁區大小舍入至報告的邏輯磁區大小。
-   如果實體磁區大小是大於 4 KB 的兩個值，您應該先評估應用程式處理此案例的能力，然後再使用該值。 否則，您應該考慮使用舍入至 4 KB 的實體磁區大小。

使用這個 IOCTL 來取得實體磁區大小有幾項限制：

-   需要更高的許可權。 如果您的應用程式未以許可權執行，您可能需要撰寫 Windows 服務應用程式，如上面所述。

-   不支援 SMB 磁片區。 您也可能需要撰寫 Windows 服務應用程式，以支援在這些磁片區上進行實體磁區大小的查詢。

-   無法發行至任何檔案控制代碼 (必須將 IOCTL 發出至磁片區控制碼) 。

-   只有本文開頭所列的 Windows 版本才支援。

**認可記錄會填補至512個位元組的磁區**

具有資料存放區的應用程式通常會有某種形式的認可記錄，其中會維護中繼資料變更的相關資訊，或維護資料存放區的結構。 為了確保遺失磁區不會影響多筆記錄，此認可記錄通常會填補至磁區大小。 使用具有較大實體磁區大小的磁片時，應用程式將需要查詢實體磁區大小（如上一節所示），並確保每個認可記錄都會填補至該大小。 這並不只會避免讀取-修改-寫入迴圈，它有助於確保在遺失實體磁區的情況下，只有一個認可記錄會遺失。

**記錄檔會以未對齊的區塊寫入**

當更新或附加至記錄檔時，通常會使用未緩衝的 i/o。 有幾種方式可協助確保這些更新已正確對齊：

-   在內部將記錄更新緩衝至作業媒體的回報實體磁區大小，並只在實體磁區單位已滿時發出記錄檔寫入
-   使用緩衝 i/o

### <a name="issue-3-file-formats-relying-on-512-byte-sectors"></a>問題3：依賴512位元組磁區的檔案格式

有些具有標準檔案格式 (例如 VHD 1.0) 的應用程式可能會以硬式編碼的方式，來採用512位元組的磁區大小。 因此，對此檔案所做的更新和寫入會導致裝置上的讀取-修改-寫入迴圈，這可能會導致客戶的效能和復原問題。 不過，有一些方法可讓應用程式支援在這種類型的媒體上操作，例如：

-   使用緩衝來確保寫入是以實體磁區大小的單位來執行
-   執行內部讀寫寫入，以協助確保以所報告的實體磁區大小單位來執行更新
-   可能的話，請將記錄填補至實體磁區，以將填補視為空白空間
-   請考慮重新設計新版本的應用程式資料結構，並支援較大的磁區

### <a name="issue-4-the-reported-physical-sector-size-can-change-between-sessions"></a>問題4：回報的實體磁區大小可能會在會話之間變更

在許多案例中，裝載 Datastor 的基礎儲存體所報告的實體磁區大小可能會變更。 最常見的情況是將 Datastor 遷移到另一個磁片區，或甚至是在網路上。 針對許多應用程式，報告的實體磁區大小變更可能是未預期的事件，而且可能會導致某些應用程式甚至無法重新初始化。

這不是最簡單的支援案例，在此將其視為諮詢。 您應考慮客戶的行動性需求，並據此調整您的支援，以協助確保客戶不會受到使用512e 媒體的負面影響。

## <a name="4-kb-native-media"></a>4 KB 原生媒體

512位元組模擬媒體的目的是要在512位元組原生和 4 KB 原生媒體之間進行轉換，而且我們預期會在512e 可供使用後立即發行 4 KB 的原生媒體。 此媒體有幾個重要的含意應注意：

-   邏輯和實體磁區大小都是 4 KB
-   因為沒有模擬層，所以儲存體將會失敗未對齊的寫入
-   沒有隱藏的恢復功能-應用程式可以運作或無法運作

雖然 Microsoft 目前正在調查未來版本的 Windows 中支援這些類型的媒體，但在適當的情況下，應用程式開發人員應考慮事先提供這些類型媒體的支援。

## <a name="closing"></a>關閉

在本文中，我們討論了大型磁區媒體在許多常見部署案例中引進的影響。 我們已經看過讀寫寫入的效能和復原效應、此媒體可引進的一些有趣案例，以及它們可能會造成的問題組合（最終會影響使用者）。 儲存產業正在以較大的磁區大小快速轉換至媒體，而且很快的客戶將無法購買具有傳統512位元組磁區大小的磁片。

這是一份即時檔，旨在協助開發人員協助您瞭解這項轉換。 您應該與您的個別組織開始交談，讓客戶、IT 專業人員和您的硬體廠商討論大型磁區的轉換，以及它如何影響對您很重要的案例。

## <a name="links-to-other-resources"></a>其他資源的連結

-   **Windows 一般支援聲明**： <https://support.microsoft.com/kb/2510009>
-   **適用于 windows 7 和 Windows Server 2008 R2 的修正程式**： <https://support.microsoft.com/kb/982018>
-   **Windows Vista 和 Windows Server 2008 的修正程式**： <https://support.microsoft.com/kb/2470478>
-   **HyperV 支援聲明**： <https://support.microsoft.com/kb/2515143>
-   **關於 IOCTL \_ 的一般資訊儲存體 \_ 查詢 \_ 屬性控制項程式碼**： [https://msdn.microsoft.com/library/ff560590.aspx](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   **IOCTL \_儲存體 \_ 查詢 \_ 屬性控制項程式碼**： [https://msdn.microsoft.com/library/ff800830.aspx](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   **儲存體 \_ 的一般資訊存取 \_ 對齊 \_ 描述元結構**： [https://msdn.microsoft.com/library/ff566344.aspx](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   **描述 Microsoft 軟體更新所用標準術語的描述**： <https://support.microsoft.com/kb/824684/>
-   **WDK 範例程式碼**，其中包含如何在呼叫 **IOCTL \_ 儲存體 \_ 查詢 \_ 屬性** 控制項程式碼時，從 **儲存體 \_ 存取 \_ 對齊 \_ 描述** 元結構中將回報的儲存體存取調整資訊解壓縮的詳細資訊： [/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   **有關 ImageX Command-Line 選項的一般資訊**： <https://technet.microsoft.com/library/dd799302(WS.10).aspx>
-   **支援 4 KB 磁區磁片磁碟機的 Intel 晶片組驅動程式需求**： <https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm>
-   如需有關 Advanced Format 磁片的詳細資訊，請造訪下列 IDEMA 網站：
    -   <http://idema.org/?page_id=2172>
    -   <http://idema.org/?download=7926>

 

 
