---
title: Advanced format (4K) 磁片相容性更新
description: Advanced format (4K) 磁片相容性更新
ms.assetid: 2C9EB0CF-D27B-457A-8FE6-24824BCC084C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0321570e5ed1cc09ef213e97bf4681b8ea0caec0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103842844"
---
# <a name="advanced-format-4k-disk-compatibility-update"></a>Advanced format (4K) 磁片相容性更新

## <a name="platforms"></a>平台

**用戶端**   Windows XP \| Windows Vista \| windows 7 WINDOWS \| 7 SP1 \| Windows 8  
**伺服器**   Windows Server 2003 \| Windows server 2008 \| windows Server 2008 R2 \| Windows SERVER 2008 R2 SP1 \| Windows server 2012 \| Windows server 2012 r2 \| windows server 2016  


## <a name="description"></a>Description

本文是名為512位元組模擬之文章的更新版本 (512e) 磁片相容性更新（已針對 Windows 7 SP1 和 Windows Server 2008 R2 SP1 發行）。 此更新包含許多新的資訊，其中有些只適用于 Windows 8 和 Windows Server 2012。

Areal 密度是每年增加的，而最近一次出現 3 TB 的磁片時，用來處理遞減信號與雜訊比率 (SNR) 的錯誤修正機制變得沒有效率;也就是說，必須增加額外的負荷，以確保媒體可供使用。 其中一個用來改善此錯誤修正機制的儲存體產業解決方案，是引進不同的實體媒體格式，其中包含較大的實體磁區大小。 這種新的實體媒體格式稱為 Advanced Format。 因此，若要對新式儲存裝置的磁區大小做出任何假設，開發人員將需要研究其程式碼的基礎，以判斷是否有影響。

本主題將介紹軟體的先進格式儲存裝置效果、討論應用程式可做些什麼來協助支援這種類型的媒體，以及討論 Microsoft 在 Windows Vista、Windows 7 和 Windows 8 引進的基礎結構，讓開發人員能夠支援這些類型的裝置。 雖然本主題中顯示的內容提供改善與 Advanced Format 磁片相容性的指導方針，但此資訊通常適用于具有執行 Windows Vista、Windows 7 和 Windows 8 的先進格式磁片的所有系統。

**新的大型磁區相關功能摘要**

下列清單摘要說明 Windows 8 和 Windows Server 2012 中提供的新功能，以協助改善大型磁區磁片的客戶和開發人員體驗。 以下是每個專案的更詳細描述。

-   建置於 Windows 7 SP1 的 Windows 7 SP1 支援（含模擬 (512e) ），並為具有4K 磁區大小的磁片提供完整的收件匣支援，而不需要模擬 (4K 原生) 。 部分支援的應用程式和案例包括：
    -   能夠從4K 磁區磁片安裝 Windows 並開機，而不需要模擬 (4K 原生磁片) 
    -   VHD 和新的 VHDX 檔案格式
    -   完整的 HyperV 支援
    -   Windows 備份
    -   NT 檔案系統中的完整支援 (NTFS) 
    -   具有新的儲存空間和集區的完整支援 (SSP) 
    -   Windows Defender 的完整支援
-   提供新的 API，以查詢 (FileFsSectorSizeInformation) 的實體磁區大小：
    -   適用于網路磁片區
    -   可以發行至任何檔案控制代碼
    -   適用于無特殊許可權的應用程式
    -   易記的使用模型
-   包含增強的 fsutil 命令列公用程式，可查詢具有對齊資訊的磁片區的邏輯和實體磁區大小 (基本版本的公用程式，但不含對齊資訊的 Windows 7 適用于具有 microsoft KB 982018 和 Windows Server 2008 R2 與 Microsoft KB 982018 的 Windows 7) 

**Advanced format (4K) 磁片簡介**

以媒體格式引進這項變更的其中一個問題，就是引進現有軟體和硬體的相容性問題的可能性。 作為暫時性的相容性解決方案，存放裝置產業最初推出的是模擬一般512位元組磁區磁片的磁片，但透過標準 ATA 和 SCSI 命令，提供真正磁區大小的相關資訊。 這種模擬的結果是，本質上有兩個磁區的大小：

**邏輯磁區：** 用於邏輯區塊定址媒體的單位。 我們也可以將它視為儲存體可接受的最小寫入單位。 這是模擬。   
**實體磁區：** 裝置的讀取和寫入作業會在單一作業中完成的單位。 這是不可部分完成的寫入單位。  
 大部分目前的 Windows Api （例如 IOCTL \_ 磁片 \_ 取得磁片 \_ 磁碟機 \_ 幾何）都會傳回邏輯磁區大小，但可透過 <a href="/windows-hardware/drivers/ddi/content/ntddstor/ni-ntddstor-ioctl_storage_query_property">IOCTL \_ 儲存體 \_ 查詢 \_ 屬性</a> 控制項程式碼抓取實體磁區大小，並在 <a href="/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor">儲存體 \_ 存取 \_ 對齊 \_ 描述</a> 元結構的 BytesPerPhysicalSector 欄位中包含相關資訊。 本文稍後會更詳細地討論。

**大型磁區媒體的初始類型**

儲存產業很快就能轉換為具有 4 KB 實體磁區大小之媒體的這種新的先進格式儲存體。 有兩種類型的媒體會發佈到市場：

**4 KB 原生：** 此媒體沒有模擬層，並且會直接公開 4 KB 作為其邏輯和實體磁區大小。 這種新型媒體的整體問題是，大部分的應用程式和作業系統都不會查詢 i/o 並使 i/o 與實體磁區大小保持一致，這可能會導致非預期的失敗 i/o。  
**512-位元組模擬 (512e) ：** 此媒體具有如上一節所討論的模擬層，並將512個位元組公開為其邏輯磁區大小 (類似於今日的一般磁片) ，但讓其實體磁區大小資訊 (4 KB) 可用。 這種新型媒體的整體問題是，大部分的應用程式和作業系統都不了解實體磁區大小是否存在，這可能會導致一些問題，如下所述。  
**大型磁區媒體的整體 Windows 支援**

下表記載各種媒體的官方 Microsoft 支援原則及其產生的報告磁區大小。 如需詳細資訊，請參閱這 [篇知識庫文章](https://support.microsoft.com/kb/2510009) 。



| 一般名稱                                  | 回報的邏輯磁區大小 | 回報的實體磁區大小 | 支援的 Windows 版本                                                                                                                                                                                                                                                                             |
|-----------------------------------------------|------------------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 512-位元組原生、512n                         | 512 個位元組                    | 512 個位元組                     | 所有 Windows 版本                                                                                                                                                                                                                                                                                     |
| Advanced Format、512e、AF、512-位元組模擬 | 512 個位元組                    | 4 KB                          | Windows Vista w/MS KB 2553708 <br/> Windows Server 2008 \* w/MS KB 2553708 <br/> Windows 7 w/MS KB 982018 <br/> Windows Server 2008 R2 * w/MS KB 982018 <br/> Windows 7 SP1 及更高版本的所有 Windows 版本。 <br/> Server 2008 R2 SP1 和以上版本的所有伺服器版本。 <br/> <br/> \*但 Hyper-v 除外。 請參閱「 [大型磁區磁片磁碟機的應用程式支援需求](https://support.microsoft.com/help/2510009/microsoft-support-policy-for-4k-sector-hard-drives-in-windows) 」一節。 |
| 預先格式化、AF、4K 原生、4Kn            | 4 KB                         | 4 KB                          | 從 Windows 8 或更早的所有 Windows 版本 <br/> Windows Server 2012 及更高版本的所有伺服器版本 <br/>                                                                                                                                                                                                                                                      |
| 其他                                         | 不是 4 KB 或512個位元組        | 不是 4 KB 或512個位元組         | 不支援                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> 雖然上表不會有壓力，但是 Windows XP、Windows Server 2003 和 Windows Server 2003 R2 不支援512e 或4Kn 媒體。 雖然系統可能會開機並可正常運作，但可能有未知案例的功能問題、資料遺失或次佳效能。 因此，Microsoft 對於以 windows xp 程式碼基底 (（例如 Windows Home Server 1.0、Windows Server 2003、Windows Server 2003 R2、windows XP 64-bit Edition、Windows XP Embedded、Windows Small Business Server 2003 和 Windows Small Business Server 2003 R2) ）使用512e 媒體時，會有強烈的警告。

 

## <a name="how-emulation-works-read-modify-write-rmw"></a>模擬的運作方式：讀取-修改-寫入 (RMW) 

儲存媒體具有可在其中修改實體媒體的特定單位。 也就是說，媒體只能以實體磁區大小的單位來寫入或重寫。 因此，不會在此單元層級執行的寫入會需要額外的步驟，我們將逐步解說下列範例。

在此案例中，應用程式必須更新位於512位元組邏輯磁區內的 Datastor 記錄內容。 下圖說明存放裝置完成寫入所需的步驟：

![儲存體裝置完成寫入的步驟](images/512ermwsteps.png)

如上所示，此程式牽涉到可能導致效能遺失的儲存裝置一些工作。 若要避免這種額外的工作，應用程式必須更新為：

-   查詢實體磁區大小
-   確定寫入與回報的實體磁區大小相符

雖然這一開始可能只是效能問題，但是可能會有更嚴重的問題。 讓我們在下一節討論這一點。

**復原：讀取-修改-寫入的隱藏成本**

復原是指應用程式在會話之間復原狀態的能力。 我們已瞭解512e 儲存體裝置執行512位元組磁區所需的內容，可寫入讀寫寫入迴圈。 如果覆寫媒體上先前的實體磁區的程式中斷，讓我們看看會發生什麼事。 結果是什麼？

-   因為大部分的硬碟磁片磁碟機就地更新，所以實體磁區，也就是實體磁區所在媒體的部分，可能因為部分覆寫而損毀，但不完整的資訊。 換句話說，您可以將它視為可能遺失所有8個邏輯磁區， (實體磁區以邏輯方式包含) 。
-   雖然大部分具有資料存放區的應用程式都是設計成能夠從媒體錯誤中復原、遺失八個磁區，或以另一種方式進行，否則可能會導致資料存放區無法正常復原。 系統管理員可能需要以手動方式從備份還原資料庫，或甚至可能需要執行冗長的重建。
-   另一個重要的影響是，另一個應用程式造成讀寫寫入迴圈的動作，可能會導致資料遺失，即使您的應用程式不在執行中也一樣。 這只是因為您的資料和其他應用程式資料可能位於相同的實體磁區內。

記住這一點之後，應用程式軟體必須重新評估程式碼中所採取的任何假設，並留意邏輯實體磁區大小的差異，以及本文稍後討論的一些有趣的客戶案例。

**(避免讀取-修改-寫入)**

雖然某些存放裝置廠商可能會在某些512e 儲存體裝置內引進一些緩和措施，以嘗試減輕讀寫寫入迴圈的效能和復原問題，但是在工作負載方面，風險降低也有很多。 因此，應用程式不應該依賴這項緩和措施作為長期解決方案。 此外，也不保證所有的磁片類別都有這項緩和措施，也無法保證緩和功能的設計是妥善設計的。

這項解決方案並不是磁片磁碟機的風險降低，而是設計應用程式來進行正確的設定，以協助支援這種類型的媒體。 本節討論應用程式可能會發生大型磁區磁片問題的常見案例，並建議進行調查的途徑，以嘗試解決每個問題。

**問題1：資料分割未對齊實體磁區界限**

當系統管理員/使用者分割磁片時，第一個磁碟分割可能尚未在對齊的界限上建立。 這可能會導致所有後續寫入變成未對齊實體磁區界限。 從 Windows Vista SP1 和 Windows Server 2008 開始，第一個磁碟分割會放置在磁片 4 GB 或更大的磁片 (的第一個 1024 KB，否則對齊是符合 4 KB 實體磁區界限的 64 KB) 。 不過，由於 Windows XP 中的預設資料分割、協力廠商分割公用程式或 Windows Api 的使用不正確，因此建立的分割區可能無法對齊實體磁區界限。 開發人員必須確保使用正確的 Api 來協助確保對齊。 以下列出建議的 Api 以協助確保資料分割對齊。

建立新磁片區時，IVdsPack：： CreateVolume 和 IVdsPack2：： CreateVolume2 Api 不會使用指定的對齊參數，而是使用作業系統的對齊值預設 (Windows Vista SP1 將使用63個位元組，而 post Windows Vista SP1 將使用上述) 的預設值。 相反地，請使用 IVdsCreatePartitionEx：： CreatePartitionEx 或 IVdsAdvancedDisk：： CreatePartition Api，針對需要建立分割區的應用程式使用指定的對齊參數。

協助確保對齊正確的最佳方式，就是在一開始建立資料分割時正確地進行。 否則，您的應用程式在執行寫入時或在初始化時，必須考慮調整帳戶，這可能是非常複雜的程式。

**問題2：未緩衝的寫入未對齊實體磁區大小**

最簡單的問題是未緩衝的寫入與儲存體媒體的回報實體磁區大小不一致。 另一方面，緩衝的寫入會對齊大小為 4 KB 的頁面大小，coincidently 是第一代大型磁區媒體的實體磁區大小。 不過，大部分具有資料存放區的應用程式都會執行未緩衝的寫入，因此必須確保這些寫入是以實體磁區大小的單位來執行。

一些案例範例，其中產生的應用程式 i/o 未對齊：

**認可記錄會填補至512個位元組的磁區：** 具有資料存放區的應用程式通常會有某種形式的認可記錄，其中會維護中繼資料變更的相關資訊，或維護資料存放區的結構。 為了確保遺失磁區不會影響多筆記錄，此認可記錄通常會填補至磁區大小。 使用具有較大實體磁區大小的磁片時，應用程式將需要查詢實體磁區大小（如上一節所示），並確保每個認可記錄都會填補至該大小。 使用4K 磁片時，可確保 i/o 不會失敗。 使用512e 的磁片時，不僅可避免讀取-修改-寫入迴圈，還可協助確保如果遺失實體磁區，則只會遺失一個認可記錄。  
**記錄檔會以未對齊的區塊寫入：** 當更新或附加至記錄檔時，通常會使用未緩衝的 i/o。 應用程式可以切換至緩衝 i/o，或在內部緩衝處理記錄檔更新為實體磁區大小的單位，以避免失敗的 i/o 或觸發讀寫寫入。  
 為協助判斷您的應用程式是否發出未緩衝處理的 i/o， \_ \_ \_ 當您呼叫 CreateFile 函式時，請務必在 *DWFLAGSANDATTRIBUTES* 參數中包含 FILE 旗標無緩衝旗標。

此外，如果您目前正在將寫入調整為磁區大小，此磁區大小很可能只是邏輯磁區大小，因為查詢媒體磁區大小的大部分現有 Api 只會查詢定址單位（也就是邏輯磁區的大小）。 這裡的磁區大小是實體磁區大小，也就是不可部分完成項的實際單位。 一些可取得邏輯磁區大小的 Api 範例如下：

-   GetDiskFreeSpace, GetDiskFreeSpaceEx
-   FileFsVolumeInformation
-   IOCTL \_ 磁片 \_ 取得磁片 \_ 磁碟機 \_ 幾何、IOCTL \_ 磁片取得磁片 \_ \_ 磁碟機幾何（ \_ \_ 例如
-   IVdsDisk：： GetProperties、IVdsDisk3：： GetProperties2

以下是您可以查詢實體磁區大小的方式：

**Windows 8 的慣用方法**

透過 Windows 8，Microsoft 引進了新的 API，可讓開發人員輕鬆地在其應用程式中整合4K 支援。 這項新的 API 所支援的案例數目，比下列討論 Windows Vista 和 Windows 7 的舊版方法更多。 此 API 會啟用這些呼叫案例：

-   從無特殊許可權的應用程式呼叫
-   呼叫任何有效的檔案控制代碼
-   透過 SMB2 呼叫遠端磁片區上的檔案控制代碼
-   簡化的程式設計模型

API 的形式為新的 info 類別 FileFsSectorSizeInformation，具有相關聯的結構檔案 \_ FS \_ 磁區 \_ 大小 \_ 資訊，定義如下：


```
typedef struct _FILE_FS_SECTOR_SIZE_INFORMATION {  
    ULONG LogicalBytesPerSector;  
    ULONG PhysicalBytesPerSectorForAtomicity;  
    ULONG PhysicalBytesPerSectorForPerformance;  
    ULONG FileSystemEffectivePhysicalBytesPerSectorForAtomicity;  
    ULONG Flags;  
    ULONG ByteOffsetForSectorAlignment;  
    ULONG ByteOffsetForPartitionAlignment;  
} FILE_FS_SECTOR_SIZE_INFORMATION, *PFILE_FS_SECTOR_SIZE_INFORMATION;
```



**適用于 Windows 7 和 Windows Vista 的舊版方法**

Windows Vista 和 Windows Server 2008 引進了 Api，可針對以 AHCI 為基礎的儲存控制器來查詢所連接存放裝置的實體磁區大小。 在 Windows 7 和 Windows Server 2008 R2 中，從 SP1 (或 Microsoft 知識庫 982018) 開始，此支援延伸至 Storport 型儲存控制器。 Microsoft 已在 MSDN 上提供程式 [代碼範例](/windows/desktop/api/winioctl/ns-winioctl-storage_access_alignment_descriptor) ，詳述應用程式如何查詢磁片區的實體磁區大小。

雖然上面的程式碼範例可讓您取得磁片區的實體磁區大小，但您應該在使用之前，先對所報告的實體磁區大小執行一些基本的健全檢查，因為觀察到某些驅動程式可能不會傳回格式正確的資料：

-   請確定回報的實體磁區大小 >= 回報的邏輯磁區大小;如果不是，則您的應用程式應該使用等於所報告邏輯磁區大小的實體磁區大小
-   確定所報告的實體磁區大小是2的乘冪;如果不是，則您的應用程式應該使用等於所報告邏輯磁區大小的實體磁區大小
-   如果實體磁區大小是介於 512-個位元組和 4 KB 之間的2個值，您應該考慮將實體磁區大小舍入至報告的邏輯磁區大小。
-   如果實體磁區大小是大於 4 KB 的兩個值，您應該先評估您的應用程式是否能夠處理此案例，再使用該值;否則，您應該考慮使用舍入至 4 KB 的實體磁區大小

使用這個 IOCTL 來取得實體磁區大小有幾項限制。 強烈

-   需要更高的許可權;如果您的應用程式未以許可權執行，您可能需要撰寫 Windows 服務應用程式，如上面所述
-   不支援 SMB 磁片區;您也可能需要撰寫 Windows 服務應用程式，以支援這些磁片區上的實體磁區大小查詢
-   無法發行至任何檔案控制代碼 (必須將 IOCTL 發出至磁片區控制碼) 

**問題3：依賴512位元組磁區的檔案格式**

某些採用標準檔案格式 (例如 VHD 1.0) 的應用程式可能會將這些檔案硬式編碼，以採用512位元組的磁區大小。 因此，對此檔案所做的更新和寫入會導致裝置上的讀寫寫入迴圈，這可能會導致您的客戶產生效能和復原問題。 不過，有一些方法可讓應用程式支援在這種類型的媒體上操作，例如：

-   使用緩衝來確保寫入是以實體磁區大小的單位來執行
-   執行內部讀寫寫入，以協助確保以所報告的實體磁區大小單位來執行更新
-   可能的話，請將記錄填補至實體磁區，以將填補視為空白空間
-   請考慮重新設計應用程式資料結構的版本，並支援較大的磁區

**問題4：回報的實體磁區大小可能會在會話之間變更**

在許多案例中，裝載 Datastor 的基礎儲存體所報告的實體磁區大小可能會變更。 最常見的情況是將 Datastor 遷移到另一個磁片區，或甚至是在網路上。 針對許多應用程式，報告的實體磁區大小變更可能是未預期的事件，而且可能會導致某些應用程式無法重新初始化。

這不是最簡單的支援案例，在此將其視為諮詢。 您應考慮客戶的行動性需求，並據此調整您的支援，以協助確保客戶不會受到使用4K 原生或512e 媒體的負面影響。

**使用者可以如何取得磁片區的邏輯和實體磁區大小**

Windows 中的 Windows 是一個公用程式，可顯示磁片區的磁區大小資訊。 具有支援的 fsutil 的 Windows 版本如下：

-   Windows 8
-   Windows Server 2012
-   Windows 7 SP1 （含 Microsoft KB 982018）
-   具有 Microsoft KB 982018 的 Windows 7
-   Windows Server 2008 R2 SP1 與 Microsoft KB 982018 (v3) 
-   Windows Server 2008 R2 與 Microsoft KB 982018 (v3) 
-   Windows Vista 與 Microsoft KB 2553708
-   Windows Server 2008 與 Microsoft KB 2553708

若要取得磁區大小資訊，請從提升許可權的命令提示字元中，呼叫公用程式：


```
fsutil fsinfo ntfsinfo <drive letter>
```



具有512位元組模擬的4K 磁區磁片會將 [每個磁區的位元組] 欄位設定為 [512]，並將 [每個實體磁區的位元組] 欄位設定為4096：

![使用512位元組模擬的4k 磁區磁片每個磁區和每個實體磁區位元組](images/4ksectordiskwith512emulation.png)

4K 原生磁片具有每個磁區的位元組數和每個實體磁區欄位的位元組數，兩者皆設定為4096，如下所示

![4k 原生磁片的每個磁區和每個實體磁區位元組數](images/4knativedisk.png)

> [!Note]  
> 如果 [每個實體磁區的位元組] 欄位顯示為不受支援，則表示儲存體驅動程式不支援 IOCTL \_ 儲存 \_ 查詢 \_ 屬性，或在抓取資訊時發生錯誤。

 

## <a name="resources"></a>資源

-   [Windows 一般支援聲明](https://support.microsoft.com/kb/2510009)
-   [Microsoft KB 982018](https://support.microsoft.com/kb/982018)
-   [Microsoft KB 2553708](https://support.microsoft.com/kb/2553708)
-   [適用于 Windows 7 和 Windows Server 2008 R2 的修正程式](https://support.microsoft.com/kb/982018)
-   [Windows Vista 和 Windows Server 2008 的修正程式](https://support.microsoft.com/kb/2553708)
-   [HyperV 支援聲明](https://support.microsoft.com/kb/2515143)
-   [有關 IOCTL \_ 儲存體 \_ 查詢 \_ 屬性控制項程式碼的一般資訊](/windows-hardware/drivers/ddi/ntddstor/ni-ntddstor-ioctl_storage_query_property)
-   [IOCTL \_ 儲存體 \_ 查詢 \_ 屬性控制項程式碼](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property)
-   [儲存體 \_ 存取 \_ 對齊 \_ 描述元結構的一般資訊](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-_storage_access_alignment_descriptor)
-   [描述 Microsoft 軟體更新所用標準術語的描述](https://support.microsoft.com/kb/824684/)
-   [WDK 範例程式碼，其中包含如何在 \_ \_ \_ 呼叫 IOCTL \_ 儲存體 \_ 查詢 \_ 屬性控制項程式碼時，從儲存體存取對齊描述元結構中將報告的儲存體存取調整資訊解壓縮的詳細資料](/windows/win32/api/winioctl/ns-winioctl-storage_access_alignment_descriptor)
-   [ImageX Command-Line 選項的一般資訊](/previous-versions/windows/it-pro/windows-7/dd799302(v=ws.10))
-   [支援 4 KB 磁區磁片磁碟機的 Intel 晶片組驅動程式需求](https://www.intel.com/support/chipsets/imsm/sb/CS-031502.htm)

 

