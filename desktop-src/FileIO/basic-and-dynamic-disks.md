---
description: 描述兩種磁片儲存體類型，並討論分割區樣式。
ms.assetid: 5d511654-92e0-4236-80e7-bb2417403186
title: 基本和動態磁碟
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f134f0dd7c8d81522733d26a6c5efb433d0e425978e1cbffd7edf3b0937b949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582623"
---
# <a name="basic-and-dynamic-disks"></a>基本和動態磁碟

在分割磁片磁碟機或取得磁片磁碟機磁碟分割配置的相關資訊之前，您必須先瞭解基本和動態磁碟儲存體類型的功能和限制。

基於本主題的目的，「磁片區」一詞是用來參考磁碟分割的概念，該磁片 *分區是由* Windows 作業系統用來儲存檔案的有效檔案系統（最常見的 NTFS）所格式化。 磁片區具有 Win32 路徑名稱，可由 [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) 和 [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) 函式列舉，而且通常會有指派給它的磁碟機號，例如 c： 如需有關磁片區和檔案系統的詳細資訊，請參閱 [檔案系統](file-systems.md)。

本主題內容：

-   [基本磁碟](#basic-disks)
-   [動態磁碟](#dynamic-disks)
-   [分割區樣式](#partition-styles)
    -   [主開機記錄](#master-boot-record)
    -   [GUID 磁碟分割表格](#guid-partition-table)
-   [偵測磁片類型](#detecting-the-type-of-disk)
-   [相關主題](#related-topics)

在此內容中參考儲存體類型時，有兩種類型的磁片： *基本磁碟* 和 *動態磁碟*。 請注意，此處所討論的儲存體類型與實體磁片或分割區樣式不同，但有不同的概念。 例如，參考基本磁碟並不代表特定的磁碟分割樣式，也需要指定用於討論之磁片的磁碟分割樣式。 如需基本磁碟儲存體類型與實體硬碟的關聯方式的簡化說明，請參閱 [磁片裝置和磁碟分割](disk-devices-and-partitions.md)。

## <a name="basic-disks"></a>基本磁碟

*基本磁碟* 是最常搭配 Windows 使用的儲存體類型。 *基本磁碟* 一詞是指包含磁碟分割的磁片，例如主要磁碟分割和邏輯磁片磁碟機，而這些磁碟分割通常會以檔案系統格式化，以成為檔案儲存的磁片區。 基本磁碟提供簡單的儲存體解決方案，可容納一系列實用的儲存體需求案例。 基本磁碟也支援叢集磁片、美國的電氣和電子技術工程師 (IEEE) 1394 磁片，以及通用序列匯流排 (USB) 抽取式磁碟機。 為了回溯相容性，基本磁碟通常會使用相同的主開機記錄 (MBR) 磁碟分割樣式做為 Microsoft MS-DOS 作業系統和所有 Windows 版本所使用的磁片，但也可以在支援的系統上支援 **GUID** 磁碟分割資料表 (GPT) 磁碟分割。 如需有關 MBR 和 GPT 磁碟分割樣式的詳細資訊，請參閱 [磁碟分割樣式](#partition-styles) 一節。

您可以藉由將現有的主要磁碟分割及邏輯磁碟機延伸到相同磁碟上相鄰的連續未配置空間，將更多空間新增至這些磁碟區。 若要延伸基本磁碟區，必須以 NTFS 檔案系統來格式化該磁碟區。 您可以在包含邏輯磁碟機之延伸磁碟分割的連續可用空間內延伸該磁碟機。 如果您延伸邏輯磁碟機超出延伸磁碟分割中提供的可用空間，只要延伸磁碟分割後面接著連續未配置的空間，延伸磁碟分割就會擴大來包含邏輯磁碟機。 如需詳細資訊，請參閱 [基本磁碟和磁片區的運作方式](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10))。

您只能在基本磁碟上執行下列作業：

-   建立和刪除主要和延伸磁碟分割。
-   建立和刪除延伸磁碟分割內的邏輯磁碟機。
-   格式化分割區，並將它標示為作用中。

## <a name="dynamic-disks"></a>動態磁碟

> [!NOTE]
> 針對鏡像開機磁碟區以外的所有使用方式 (使用鏡像磁片區來裝載作業系統) ，動態磁碟已淘汰。 對於需要復原磁片磁碟機失敗的資料，請使用儲存空間，這是一個彈性的儲存體虛擬化解決方案。 如需詳細資訊，請參閱[儲存空間總覽](/windows-server/storage/storage-spaces/overview)。

*動態磁碟* 提供基本磁碟所沒有的功能，例如能夠建立跨多個磁片的磁片區， (跨距和等量磁片區) ，以及建立容錯磁片區 (鏡像和 raid-5 磁片區) 的能力。 就像基本磁碟一樣，動態磁碟也可以在同時支援這兩者的系統上使用 MBR 或 GPT 磁碟分割樣式。 動態磁碟上的所有磁片區都稱為動態磁碟區。 動態磁碟提供大量管理的彈性，因為它們會使用資料庫來追蹤磁片上的動態磁碟區以及電腦中其他動態磁碟的相關資訊。 因為電腦中的每個動態磁碟都會儲存動態磁碟資料庫的複本，所以損毀的動態磁碟資料庫可以使用另一個動態磁碟上的資料庫修復一個動態磁碟。 資料庫的位置取決於磁片的磁碟分割樣式。 在 MBR 磁碟分區上，資料庫會包含在磁片的最後 1 mb (MB) 中。 在 GPT 磁碟分割上，資料庫會包含在 1 MB 保留的 (隱藏) 分割區中。

動態磁碟是一種不同的磁片區管理格式，可讓磁片區在一或多個實體磁片上具有非連續的範圍。 動態磁碟和磁片區依賴邏輯磁片管理員 (LDM) 和虛擬磁碟服務 (VDS) 與其相關聯的功能。 這些功能可讓您執行工作，例如將基本磁碟轉換為動態磁碟，以及建立容錯磁片區。 為了鼓勵使用動態磁碟，已從基本磁碟移除多磁碟分割磁片區支援，而且現在可在動態磁碟上獨佔支援。

您只能在動態磁碟上執行下列作業：

-   建立和刪除簡單、跨距、等量、鏡像和 RAID-5 磁片區。
-   延伸簡單或跨距磁片區。
-   從鏡像磁片區移除鏡像，或將鏡像磁片區分成兩個磁片區。
-   修復鏡像或 RAID-5 磁片區。
-   重新開機遺失或離線的磁片。

基本和動態磁碟之間的另一項差異是，動態磁碟區可以由一或多個實體磁片上的一組非連續範圍所組成。 相較之下，基本磁碟上的磁片區是由單一磁片上的一組連續範圍所組成。 由於 LDM 資料庫所需的磁碟空間的位置和大小，Windows 無法將基本磁碟轉換為動態磁碟，除非磁片上至少有 1 MB 的未使用空間。

無論系統上的動態磁碟是否使用 MBR 或 GPT 磁碟分割樣式，您都可以在系統上建立高達2000的動態磁碟區，雖然建議的動態磁碟區數目是32或更少。 如需使用動態磁碟和磁片區的詳細資訊和其他考慮，請參閱 [動態磁碟和磁片](/previous-versions/windows/it-pro/windows-server-2003/cc757696(v=ws.10))區。

如需動態磁碟的更多功能和使用案例，請參閱 [何謂動態磁碟和磁片區？](/previous-versions/windows/it-pro/windows-server-2003/cc737048(v=ws.10))。

基本和動態磁碟的一般作業如下：

-   支援 MBR 和 GPT 磁碟分割樣式。
-   檢查磁片屬性，例如容量、可用空間和目前狀態。
-   查看磁碟分割屬性，例如 offset、length、type，以及是否可在開機時將資料分割當做系統磁碟區使用。
-   查看磁片區屬性，例如大小、磁碟機號指派、標籤、類型、Win32 路徑名稱、磁碟分割類型和檔案系統。
-   為磁片區或磁碟分割建立磁碟機號指派，以及為 CD-ROM 裝置建立磁碟機號指派。
-   將基本磁碟轉換成動態磁碟，或是將動態磁碟轉換為基本磁碟。

除非另有指定，否則 Windows 預設會將磁片磁碟機分割為基本磁碟。 您必須明確地將基本磁碟轉換為動態磁碟。 不過，在您嘗試這麼做之前，必須先考慮一些磁碟空間的考慮。 如需詳細資訊，請參閱[如何在 Windows XP Professional 轉換成基本和動態磁碟](https://support.microsoft.com/kb/309044)。

## <a name="partition-styles"></a>分割區樣式

*分割區樣式*（有時也稱為資料 *分割* 配置）是指磁片配置的特定基礎結構，以及資料分割的實際相片順序、功能是什麼，以及限制為何的詞彙。 若要開機 Windows，x86 型和 x64 型電腦中的 BIOS 執行需要至少包含一個主要開機記錄的基本磁碟， (MBR) 磁碟分割標示為作用中，其中 Windows 作業系統的相關資訊 (但不一定是整個作業系統安裝) ，以及磁碟分割的相關資訊儲存位置。 這項資訊會放在不同的位置，而這兩個位置可能位於不同的資料分割或單一分割區中。 所有其他實體磁片儲存體都可以設定為兩個可用分割區樣式的組合，如下列各節所述。 如需其他系統類型的詳細資訊，請參閱有關資料 [分割樣式](/previous-versions/windows/it-pro/windows-server-2003/cc738081(v=ws.10))的 TechNet 主題。

如先前所述，動態磁碟會遵循稍有不同的使用案例，而且使用這兩個數據分割樣式的方式會受到該使用方式的影響。 因為動態磁碟通常不會用來包含系統開機磁碟區，所以會簡化此討論以排除特殊案例。 如需分割區資料區塊配置的詳細資訊，以及與磁碟分割樣式相關的基本或動態磁碟使用案例，請參閱 [基本磁碟和](/previous-versions/windows/it-pro/windows-server-2003/cc739412(v=ws.10)) 磁片區的運作方式，以及 [動態磁碟和磁片區的運作方式](/previous-versions/windows/it-pro/windows-server-2003/cc758035(v=ws.10))。

### <a name="master-boot-record"></a>主開機記錄

所有執行 Windows 的 x86 型和 x64 型電腦都可以使用稱為「*主開機記錄* (MBR) 的磁碟分割樣式。 MBR 磁碟分區樣式包含描述磁碟分割位於磁片上的磁碟分割資料表。 由於 MBR 是 x86 電腦上唯一可用的磁碟分割樣式，在 Windows Server 2003 Service Pack 1 (SP1) 之前，您不需要選擇此樣式。 它會自動使用。

您可以使用 MBR 磁碟分區配置在基本磁碟上最多建立四個磁碟分割：四個主要分割區，或三個主要分割區，以及一個擴充。 延伸磁碟分割可包含一或多個邏輯磁碟機。 下圖說明三個主要磁碟分割的範例版面配置，以及基本磁碟上使用 MBR 的一個延伸磁碟分割。 延伸磁碟分割中包含四個擴充的邏輯磁碟機。 延伸磁碟分割可能會位於磁片的結尾，但不一定是邏輯磁碟機 1-n 的單一連續空間。

![在基本磁碟上使用 mbr 的三個主要磁碟分割和一個擴充磁碟分割](images/basic-mbr.png)

每個分割區（不論是主要或擴充）都可以格式化為 Windows 磁片區，並具有與磁片區間的一對一關聯性。 換句話說，單一分割區不能包含多個單一磁片區。 在此範例中，總共會有七個磁片區可供 Windows 用於檔案儲存體。 Windows 中的檔案儲存體無法使用未格式化的磁碟分割。

動態磁碟 MBR 配置看起來與基本磁碟 MBR 配置非常類似，不同之處在于只允許一個主要磁碟分割 (稱為 LDM 磁碟分割) 、不允許任何擴充的資料分割，而且在 LDM 資料庫的磁片結尾有隱藏的磁碟分割。 如需有關 LDM 的詳細資訊，請參閱「 [動態磁碟](#basic-and-dynamic-disks) 」一節。

### <a name="guid-partition-table"></a>GUID 磁碟分割表格

執行 Windows Server 2003 SP1 和更新版本的系統，除了 MBR 磁碟分區樣式之外，還可以使用稱為全域唯一識別碼 (**GUID**) 磁碟分割資料表 (GPT) 的磁碟分割樣式。 使用 GPT 磁碟分割樣式的基本磁碟最多可有128的主要磁碟分割，而動態磁碟則會有單一的 LDM 磁碟分割，如同 MBR 分割一樣。 因為使用 GPT 磁碟分割的基本磁碟不會將您限制為四個磁碟分割，所以您不需要建立延伸磁碟分割或邏輯磁碟機。

GPT 磁碟分割樣式也有下列屬性：

-   允許大於 2 tb 的磁碟分割。
-   已新增複寫和迴圈冗余檢查的可靠性 (CRC) 資料分割資料表的保護。
-   支援由原始設備製造商所定義的其他磁碟分割類型 **GUID** (oem) 、獨立軟體廠商 (isv) 和其他作業系統。

下圖說明基本磁碟的 GPT 磁碟分割版面配置。

![gpt 版面配置](images/basic-gpt.png)

GPT 磁碟分割配置有保護 MBR 區域，可回溯相容于在 MBR 上運作的磁片管理公用程式。 GPT 標頭會定義分割區專案可使用的邏輯區塊位址範圍。 GPT 標頭也會定義其在磁片上的位置、其 **GUID** 和32位迴圈冗余檢查 (CRC32) checksum，用來確認 GPT 標頭的完整性。 每個 **GUID** 資料分割專案的開頭都是磁碟分割類型 GUID。 16位元組磁碟分割類型 **GUID**（類似于 MBR 磁碟的磁碟分割資料表中的系統識別碼）會識別分割區包含的資料類型，並識別磁碟分割的使用方式，例如，如果是基本磁碟或動態磁碟。 請注意，每個 **GUID** 磁碟分割專案都有備份複本。

動態磁碟 **GPT** 磁碟分割配置看起來類似此基本磁碟範例，但如先前所述，只有一個 LDM 分割專案，而不是基本磁碟上允許的 1-n 個主要磁碟分割。 另外還有隱藏的 LDM 資料庫分割區，其中包含對應的 **GUID** 資料分割專案。 如需有關 LDM 的詳細資訊，請參閱「 [動態磁碟](#basic-and-dynamic-disks) 」一節。

## <a name="detecting-the-type-of-disk"></a>偵測磁片類型

沒有特定的函式可透過程式設計方式偵測特定檔案或目錄所在的磁片類型。 有間接方法。

* 將檔案或目錄路徑傳遞至 [**GetVolumePathName**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew) ，以取得掛接點。
* 將掛接點傳遞至 [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) 以取得磁片區名稱。
* 從磁片區名稱中移除尾端的反斜線。
* 將沒有尾端反斜線的磁片區名稱傳遞至 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ，以開啟磁片區。
* 搭配 [**使用 \_ IOCTL \_ 磁片區和磁片 \_ \_ \_ 區磁片區**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_volume_get_volume_disk_extents) 來取得磁片編號。
* 使用磁片編號來建立磁片路徑，例如 " \\ \\ ？ \\PhysicalDrive *X*」。
* 將每個磁片路徑傳遞至 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 以開啟磁片。
* 使用 [**IOCTL \_ 磁片 \_ 取得 \_ 磁片 \_ 磁碟機 \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_get_drive_layout_ex) 配置，例如取得分割區清單。
* 檢查資料分割清單中每個專案的 **PartitionType** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於磁片區管理](about-volume-management.md)
</dt> <dt>

[基本磁碟和磁片區技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[動態磁碟與磁片區技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Windows XP 中的基本儲存體與動態儲存體]( https://support.microsoft.com/kb/314343/)
</dt> </dl>

 

 
