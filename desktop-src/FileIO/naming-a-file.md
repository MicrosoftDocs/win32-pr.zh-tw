---
description: Windows 支援的所有檔案系統都會使用檔案和目錄的概念來存取儲存在磁片或裝置上的資料。
ms.assetid: 121cd5b2-e6fd-4eb4-99b4-b652d27b53e8
title: 命名檔案、路徑和命名空間
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: f77b12fa133bb8b35260b49a90c24e202055c8564431f6a0d6d4c09527811ca0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533448"
---
# <a name="naming-files-paths-and-namespaces"></a>命名檔案、路徑和命名空間

Windows 支援的所有檔案系統都會使用檔案和目錄的概念來存取儲存在磁片或裝置上的資料。 使用 Windows api 進行檔案和裝置 i/o 的 Windows 開發人員應該瞭解檔案和目錄的各種規則、慣例和名稱限制。

您可以使用檔案 i/o Api，從磁片、裝置和網路共用存取資料。 檔案和目錄（以及命名空間）都屬於路徑概念的一部分，這是在何處取得資料的字串表示，無論資料是從磁片或裝置或特定作業的網路連接。

某些檔案系統（例如 NTFS）支援連結的檔案和目錄，也跟一般檔案或目錄一樣，也遵循檔案命名慣例和規則。 如需詳細資訊，請參閱永久 [連結和](hard-links-and-junctions.md) 連接以及重新 [分析點和檔案作業](reparse-points-and-file-operations.md)。

如需詳細資訊，請參閱下列小節：

-   [檔案和目錄名稱](#file-and-directory-names)
    -   [命名慣例](#naming-conventions)
    -   [簡短名稱與完整名稱](#short-vs-long-names)
-   [路徑](#fully-qualified-vs-relative-paths)
    -   [完整和相對路徑](#fully-qualified-vs-relative-paths)
    -   [最大路徑長度限制](#maximum-path-length-limitation)
-   [命名空間](#win32-file-namespaces)
    -   [Win32 檔案命名空間](#win32-file-namespaces)
    -   [Win32 裝置命名空間](#win32-device-namespaces)
    -   [NT 命名空間](#nt-namespaces)
-   [相關主題](#related-topics)


若要瞭解如何將 Windows 10 設定為支援長檔案路徑，請參閱[最大路徑長度限制](./maximum-file-path-limitation.md)。


## <a name="file-and-directory-names"></a>檔案和目錄名稱

所有檔案系統都會針對個別檔案遵循相同的一般命名慣例：基底檔案名和選用副檔名（以句號分隔）。 不過，每個檔案系統（例如 NTFS、CDFS.SYS、exFAT、UDF、FAT 和 FAT32）都可以有特定且不同的規則，以便在目錄或檔案的路徑中構成個別元件的形式。 請注意， *目錄* 只是具有特殊屬性的檔案，並將它指定為目錄，但必須遵循所有與一般檔案相同的命名規則。 由於「 *目錄* 」一詞是指檔案系統所關心的特殊檔案類型，因此有些參考資料會使用 *一般詞彙檔案* 來包含目錄和資料檔案的概念。 基於這個原因，除非另有指定，否則檔案的任何命名或使用規則或範例也應套用至目錄。 「詞彙 *路徑* 」（path）是指一或多個目錄、反斜線，以及可能的磁片區名稱。 如需詳細資訊，請參閱 [路徑](#fully-qualified-vs-relative-paths) 一節。

字元計數限制也可以不同，而且會根據所使用的檔案系統和路徑名稱首碼格式而有所不同。 這對回溯相容性機制的支援會更複雜。 例如，較舊的 MS-DOS FAT 檔案系統最多支援8個字元作為基底檔案名和3個字元的副檔名，總共12個字元，包括點分隔符號。 這通常稱為 *8.3 檔案名*。 Windows FAT 和 NTFS 檔案系統都不限於8.3 檔案名，因為它們的檔案名 *支援很長*，但仍支援8.3 版的長檔名。

### <a name="naming-conventions"></a>命名規範

下列基本規則可讓應用程式建立及處理檔案和目錄的有效名稱，而不論檔案系統為何：

-   使用句點將基底檔案名與目錄或檔案的名稱中的副檔名分隔開來。
-   使用反斜線 (\\) 來分隔 *路徑* 的 *元件*。 反斜線會將檔案名與路徑的路徑分開，並將另一個目錄名稱從路徑中的另一個目錄名稱分割。 您不能在實際的檔案或目錄名稱中使用反斜線，因為它是將名稱分隔成元件的保留字元。
-   使用反斜線做為[磁片區名稱](naming-a-volume.md)的一部分，例如，通用命名慣例的 "c：" 中的 "c："、" \\ c： \\ path \\ file" 或 "server \\ \\ \\ share" （ \\ \\ \\ \\ \\ 適用于通用命名慣例 (UNC) 名稱）。 如需 UNC 名稱的詳細資訊，請參閱 [最大路徑長度限制](#maximum-path-length-limitation) 一節。
-   請勿採用區分大小寫。 例如，假設有一些檔案系統 (（例如 POSIX 相容的檔案系統）時，將 OSCAR、Oscar 和 oscar 的名稱視為相同，) 可能會將它們視為不同。 請注意，NTFS 支援 POSIX 語義以區分大小寫，但這不是預設行為。 如需詳細資訊，請參閱 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)。
-   磁片區指示項 (磁碟機號) 同樣不區分大小寫。 例如，"D： \\ " 和 "D： \\ " 指的是相同的磁片區。
-   使用目前字碼頁中的任何字元做為名稱，包括擴充字元集中的 Unicode 字元和字元 (128 – 255) ，但下列情況除外：

    -   下列保留字元：

        -   < (小於)
        -   \> (大於)
        -   ： (冒號) 
        -   " (雙引號)
        -   / (正斜線)
        -   \\ (反斜線) 
        -   \| (分隔號形圖或管道) 
        -   ? (問號)
        -   \* (星號) 

    -   整數值零，有時稱為 ASCII *NUL* 字元。
    -   整數表示的字元在1到31的範圍內，但允許這些字元的替換資料流程除外。 如需檔案資料流程的詳細資訊，請參閱檔案 [資料流程](file-streams.md)。
    -   目的檔案系統不允許的其他任何字元。

-   使用句點做為路徑中的目錄 *元件* 以表示目前的目錄，例如 "。 \\temp.txt」。 如需詳細資訊，請參閱 [路徑](#fully-qualified-vs-relative-paths)。
-    (，請使用兩個連續的句點。) 做為路徑中的目錄 *元件* ，以代表目前的目錄的父系，例如 ".. \\temp.txt」。 如需詳細資訊，請參閱 [路徑](#fully-qualified-vs-relative-paths)。
-   請勿使用下列保留名稱作為檔案名：

    CON、PRN、AUX、NUL、COM1、COM2、COM3、COM4、COM5、COM6、COM7、COM8、COM9、LPT1、LPT2、LPT3、LPT4、LPT5、LPT6、LPT7、LPT8 和 LPT9。 也請避免這些名稱後面緊接著延伸模組;例如，不建議使用 NUL.txt。 如需詳細資訊，請參閱[命名空間](#win32-file-namespaces)。

-   請勿以空格或句號結束檔案或目錄名稱。 雖然基礎檔案系統可能支援這類名稱，但 Windows shell 和使用者介面則不支援。 不過，您可以將句號指定為名稱的第一個字元。 例如，"temp"。

### <a name="short-vs-long-names"></a>簡短名稱與完整名稱

很長的檔案名會視為任何檔案名，而不是超過簡短的 MS-DOS (也稱為 *8.3*) 樣式的命名慣例。 當您建立長檔名時，Windows 也可能會建立名為 *8.3 別名* 或簡短名稱的簡短8.3 格式名稱，並將其儲存在磁片上。 根據特定檔案系統而定，您可以針對全系統或指定磁片區的效能原因來停用此8.3 別名。

**Windows server 2008、Windows Vista、Windows Server 2003 和 Windows XP：** 8.3 無法針對指定的磁片區停用別名，直到 Windows 7 和 Windows Server 2008 R2 為止。

在許多檔案系統中，檔案名會包含一個波狀符號 (~) 名稱太長而不符合8.3 命名規則的每個元件中。

> [!Note]  
> 並非所有檔案系統都遵循波狀符號替代慣例，而系統也可以設定為停用8.3 別名產生（即使它們通常支援的話）。 因此，請勿假設8.3 別名已經存在於磁片上。

 

若要從系統要求8.3 檔案名、長檔名或檔案的完整路徑，請考慮下列選項：

-   若要取得完整檔案名的8.3 格式，請使用 [**GetShortPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getshortpathnamew) 函數。
-   若要取得簡短名稱的完整檔案名版本，請使用 [**GetLongPathName**](/windows/desktop/api/FileAPI/nf-fileapi-getlongpathnamea) 函數。
-   若要取得檔案的完整路徑，請使用 [**>getfullpathname**](/windows/desktop/api/FileAPI/nf-fileapi-getfullpathnamea) 函數。

在較新的檔案系統（例如 NTFS、exFAT、udf 和 FAT32）上，Windows 會以 Unicode 將長檔名儲存在磁片上，這表示一律會保留原始的長檔名。 即使在磁片讀取或寫入作業期間使用中的字碼頁，這也是如此。

使用長檔名的檔案可在 NTFS 檔案系統磁碟分割和 Windows FAT 檔案系統分割區之間複製，而不會遺失任何檔案名資訊。 這可能不適合舊版 MS-DOS FAT 和某些類型的 CDFS.SYS (CD-ROM) 檔案系統，視實際的檔案名而定。 在此情況下，會在可能的情況下替換簡短的檔案名。

## <a name="paths"></a>路徑

指定檔案的 *路徑* 是由一或多個 *元件* 所組成，以特殊字元 (反斜線) ，每個元件通常是目錄名稱或檔案名，但有一些值得注意的例外狀況，如下所述。 在系統解釋路徑的開頭或 *前置* 詞外觀時，通常是很重要的。 這個前置詞會決定路徑所使用的 *命名空間* ，以及在路徑內的哪個位置（包括最後一個字元）使用哪些特殊字元。

如果路徑的元件是檔案名，它必須是最後一個元件。

路徑的每個元件也會受限於針對特定檔案系統指定的最大長度。 一般而言，這些規則分為兩個類別： *short* 和 *long*。 請注意，檔案系統會將目錄名稱儲存為特殊類型的檔案，但檔案的命名規則也適用于目錄名稱。 總而言之，路徑只是存在於特定檔案或目錄名稱的所有目錄之間的階層字串表示。

### <a name="fully-qualified-vs-relative-paths"></a>完整和相對路徑

針對操作檔案的 Windows API 函式，檔案名通常會相對於目前的目錄，而某些 api 則需要完整路徑。 如果檔案名的開頭不是下列其中一項，則會是相對於目前的目錄的檔案名：

-   任何格式的 UNC 名稱，一律以兩個反斜線字元開頭 ( " \\ \\ " ) 。 如需詳細資訊，請參閱下一節。
-   具有反斜線的磁片指示項，例如 "C： \\ " 或 "d： \\ "。
-   單一反斜線，例如 " \\ directory" 或 " \\file.txt"。 這也稱為 *絕對路徑*。

如果檔案名的開頭只有磁片指示項，但不是冒號之後的反斜線，則會以指定的字母解釋為磁片磁碟機上目前目錄的相對路徑。 請注意，根據在該磁片上最新的「變更目錄」作業期間所設定的內容而定，目前目錄可能會或可能不是根目錄。 此格式的範例如下所示：

-   "C:tmp.txt" 指的是磁片磁碟機 C 上目前目錄中名為 "tmp.txt" 的檔案。
-   「C:tempdir \\tmp.txt」指的是在磁片磁碟機 C 上的目前的目錄子目錄中的檔案。

如果路徑包含「雙點」，則也稱為相對路徑;也就是說，路徑的一個元件中有兩個句號。 這個特殊規範是用來表示目前目錄上方的目錄，也就是所謂的「上層目錄」。 此格式的範例如下所示：

-   "..\\tmp.txt」會指定名為 tmp.txt 的檔案，該檔案位於目前的目錄的父系。
-   "..\\..\\tmp.txt」指定的檔案是目前目錄上方的兩個目錄。
-   "..\\tempdir \\tmp.txt」會指定名為 tmp.txt 的檔案，該目錄位於名為 tempdir 的目錄中，而該目錄是目前目錄的對等目錄。

相對路徑可以結合這兩種範例類型，例如 "C:.. \\tmp.txt」。 這項功能很有用，因為雖然系統會追蹤目前磁片磁碟機以及該磁片磁碟機的目前的目錄，但它也會追蹤每個不同磁碟機號的目前目錄 (如果您的系統有一個以上的) ，不論哪一個磁片磁碟機指示項設定為目前磁片磁碟機。

### <a name="maximum-path-length-limitation"></a>最大路徑長度限制


在 Windows 10 1607 版之前的 Windows 版本中，路徑的最大長度是定義為260個字元的 **最大 \_ 路徑**。 在 Windows 的較新版本中，必須變更登錄機碼或使用群組原則工具才能移除限制。 如需完整的詳細資料，請參閱 [最大路徑長度限制](./maximum-file-path-limitation.md) 。


## <a name="namespaces"></a>命名空間

Windows api 中使用的命名空間慣例有兩種主要類別，通常稱為 *NT 命名* 空間和 *Win32 命名空間*。 NT 命名空間的設計是將其他子系統和命名空間存在的最低層級命名空間，包括 Win32 子系統和延伸模組（Win32 namespace）。 POSIX 是 Windows 中的子系統的另一個範例，是以 NT 命名空間為基礎。 舊版 Windows 也定義了數個預先定義或保留的特定特殊裝置名稱，例如通訊 (序列和平行) 埠，而預設顯示主控台則是目前稱為 NT 裝置命名空間的一部分，而且在目前版本的 Windows 中仍支援，以提供回溯相容性。

### <a name="win32-file-namespaces"></a>Win32 檔案命名空間

Win32 命名空間前置和慣例會在本節和下一節中摘要說明，並說明其使用方式的說明。 請注意，這些範例適用于 Windows API 函式，而且不一定能搭配 Windows shell 應用程式使用，例如 Windows 檔案總管。 基於這個理由，您可以使用這些命名空間慣例，從 Windows shell 應用程式通常可以取得較廣泛的可能路徑，而且可以使用這些命名空間慣例來開發利用此功能的 Windows 應用程式。

若為檔案 i/o， \\ \\ 路徑字串的 "？ \\ " 前置詞會指示 Windows 的 api 停用所有字串剖析，並將緊接在其後面的字串傳送至檔案系統。 例如，如果檔案系統支援大型路徑和檔案名，您可以超過 Windows api 所強制執行的 **最大 \_ 路徑** 限制。 如需一般最大路徑限制的詳細資訊，請參閱上一節 [最大路徑長度限制](#maximum-path-length-limitation)。

因為它會關閉路徑字串的自動展開，所以 " \\ \\ ？ \\ " 前置詞也允許在路徑名稱中使用 ".." 和 "."，如果您嘗試使用這些其他保留的相對路徑規範來執行檔案作業，這會很有用。

許多檔案 i/o api 都支援 " \\ \\ ？ \\ "; 您應該查看每個 API 的參考主題以確定。 

請注意，您應該使用 Unicode api 來確定 " \\ \\ ？ \\ " 前置詞允許超過 **最大 \_ 路徑** 

### <a name="win32-device-namespaces"></a>Win32 裝置命名空間

" \\ \\ . \\ " 前置詞會存取 win32 裝置命名空間，而不是 win32 檔案命名空間。 如果 API 支援這種類型的存取，就可以直接完成實體磁片和磁片區的存取，而不需要透過檔案系統。 您可以使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 和 [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) 功能來存取 (磁片以外的許多裝置，例如) 。

例如，如果您想要開啟系統的序列通訊埠1，您可以在對 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式的呼叫中使用 "COM1"。 這是因為 COM1 – COM9 是 NT 命名空間中保留名稱的一部分，不過使用 " \\ \\ . \\ " 前置詞也可以使用這些裝置名稱。 相較之下，如果您已安裝100埠序列擴充面板，而且想要開啟 COM56，則無法使用 "COM56" 開啟它，因為沒有預先定義的 NT 命名空間可供 COM56。 您將需要使用 "來開啟它 \\ \\ 。 \\COM56 "，因為" \\ \\ . \\ "會直接移至裝置命名空間，而不會嘗試找出預先定義的別名。

使用 Win32 裝置命名空間的另一個範例是使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函數搭配 " \\ \\ 。 \\PhysicalDisk *x*" (其中 *x* 是有效的整數值) 或" \\ \\ 。 \\CdRom *X*」。 這可讓您直接存取這些裝置，略過檔案系統。 這是因為這些裝置名稱是由系統所建立，因為系統會列舉這些裝置，而某些驅動程式也會在系統中建立其他別名。 例如，執行名稱 "C：" 的設備磁碟機 \\ 有自己的命名空間，也就是檔案系統。

經過 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)函式的 api 通常會使用 " \\ \\ . \\ " 前置詞，因為 **CreateFile** 是用來開啟檔案和裝置的函式，取決於您使用的參數。

如果您正在使用 Windows API 函式，您應該使用 " \\ \\ . \\ " 前置詞來存取裝置，而不是存取檔案。

大部分的 api 不支援 " \\ \\ . \\ "; 只有設計用來處理裝置命名空間的 api 才能辨識它。 請一律檢查每個 API 的參考主題以確定。

### <a name="nt-namespaces"></a>NT 命名空間

此外，也有 api 可允許使用 NT 命名空間慣例，但 Windows 的物件管理員在大部分情況下都不需要這樣做。 為了說明，您可以使用 Windows Sysinternals [WinObj](/sysinternals/downloads/winobj)工具，在系統物件瀏覽器中流覽 Windows 命名空間，這會很有用。 當您執行此工具時，您看到的是 NT 命名空間（從根目錄開始）或 " \\ "。 名為 "Global？？" 的子資料夾 是 Win32 命名空間所在的位置。 命名裝置物件位於 "Device" 子目錄內的 NT 命名空間中。 您也可以在這裡找到 Serial0 和 Serial1，代表您的系統上的前兩個 COM 埠的裝置物件。 代表磁片區的裝置物件會是類似 "HarddiskVolume1" 的內容，雖然數值尾碼可能不同。 子目錄 "Harddisk0" 下的名稱 "DR0" 是代表磁片的裝置物件範例，依此類推。

為了讓 Windows 的應用程式可存取這些裝置物件，設備磁碟機會建立符號連結， (將 Win32 命名空間中的) 符號連結，也就是其各自的裝置物件。 例如，在 "Global？？" 底下的 COM0 和 COM1 子目錄只是符號連結至 Serial0 和 Serial1，"C：" 是 HarddiskVolume1 的連結，">physicaldrive0" 是要 DR0 的符號連結，依此類推。 如果沒有連結，則會使用先前所述的 Win32 命名空間慣例，將指定的裝置 "Xxx" 提供給任何 Windows 應用程式。 不過，您可以使用任何支援 NT 命名空間絕對路徑 " \\ device Xxx" 格式的 api，將控制碼開啟至該裝置 \\ 。

透過終端機服務和虛擬機器加入多使用者支援，就能進一步將 Win32 命名空間內整個系統的根裝置虛擬化。 這是藉由將名稱為 "GLOBALROOT" 的符號新增至 Win32 命名空間來完成，您可以在 "Global？？" 中看到這個命名空間。 先前討論過的 WinObj 瀏覽器工具子目錄，並可透過「？」路徑存取 \\ \\ 。 \\GLOBALROOT". 這個前置詞可確保之後的路徑會查看系統物件管理員的真實根路徑，而不是會話相依的路徑。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[檔案系統功能比較](filesystem-functionality-comparison.md)
</dt> </dl>

 

 