---
title: 建立磁片清理處理常式
description: 在電腦的世界中，一次條真理經過證實的時間，不論電腦的儲存容量大小為何，最後都會填滿。
ms.assetid: f85e0db7-fbdb-452e-90c8-672f716b5692
keywords:
- 磁片清理處理常式
- 磁碟清理
- DataDrivenCleaner
- 註冊，磁片清理處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ce7fc96e16cb27168e00196b65d48d378758a47594122cca978dc1a1f4de94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479889"
---
# <a name="creating-a-disk-cleanup-handler"></a>建立磁片清理處理常式

在電腦的世界中，一次條真理經過證實的時間，不論電腦的儲存容量大小為何，最後都會填滿。 雖然電腦硬碟的平均大小會隨著時間大幅增加，但應用程式也會隨之增加，讓使用者尋找建立更多可用硬碟空間的方法。 應用程式基於備份或效能考慮而建立的許多暫存檔案，也會減少可用空間。 當磁碟空間變少時，就必須減少應用程式所使用的空間量。 您可以使用各種不同的方法來釋放磁碟空間，包括下列各項：

-   刪除檔案。
-   壓縮檔案。
-   將檔案移至備份媒體。
-   將檔案傳送至遠端伺服器。

非常適合清除的檔案包括：

-   使用者將永遠不需要的檔案。
-   只有基於效能考慮才存在的暫存檔案。
-   可從安裝光碟還原的檔案（如有需要）。
-   可能已由較新版本取代的資料檔案，例如舊的備份檔案。
-   長時間未使用的舊檔案。

刪除特別適用于使用者不再需要的檔案，例如基於效能考慮暫時快取的檔案。 刪除也適合方便還原的檔案，例如可從安裝光碟重載的圖形檔案。 使用者稍後可能需要或難以重建的檔案，是更適合壓縮或備份的候選項目。

需要使用者手動清除檔案系統並不是理想的解決方案。 使用者可能不知道有許多檔案的所在位置，或是如何辨識哪些檔案可以安全地移除。 此外，使用者可能會有可能刪除重要檔案的風險。

本主題將討論磁片清理公用程式的下列 facet。

-   [Windows 磁片清理公用程式](#the-windows-disk-cleanup-utility)
-   [執行基本概念](#implementation-basics)
    -   [Initialize/InitializeEx](#initializeinitializeex)
    -   [GetSpaceUsed](#getspaceused)
    -   [Interactivesession.showproperties](#showproperties)
    -   [清除](#purge)
    -   [停用](#deactivate)
-   [註冊磁片清理處理常式](#registering-a-disk-cleanup-handler)
    -   [註冊處理常式的 CLSID](#registering-a-handlers-clsid)
    -   [使用磁片清理管理員來註冊處理常式：一般](#registering-a-handler-with-the-disk-cleanup-manager-general)
    -   [使用磁片清理管理員來註冊處理常式： Windows 2000 或更新版本的系統](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
    -   [使用 DataDrivenCleaner 物件](#using-the-datadrivencleaner-object)
    -   [磁片清理處理常式的註冊範例](#example-registration-of-a-disk-cleanup-handler)

## <a name="the-windows-disk-cleanup-utility"></a>Windows 磁片清理公用程式

從 Windows 98 開始，Windows 作業系統包含磁片清理，這是一個公用程式，可讓使用者更輕鬆地管理可用的硬碟空間。 磁片清理公用程式是設計用來釋出盡可能多的磁碟空間，並降低使用者不小心刪除重要檔案的風險。

您可以用三種方式起始磁片清理。

-   使用者可以按一下 [ **開始**] 來起始磁片清理;指向 [ **所有程式**]、[ **附屬** 應用程式] 和 [ **系統工具**];然後按一下 [ **磁片清理**]。
-   系統會通知使用者，指出未使用的磁碟空間已達重大模式。 大於 2.25 gb 的磁片磁碟機的重大模式閾值 (GB) 200 mb (MB) 。 後續的警告會在80、50和 1 MB 提供。 使用者可以選擇手動釋出磁碟空間，或啟動磁片清理公用程式。
-   使用者可以在較舊的系統上 Windows 排程的工作 Wizard (稱為「維護嚮導」) 在排程的時間自動執行磁片清理公用程式。

磁片清理所固有的基本挑戰是，盡可能釋放磁碟空間，而不需要刪除重要的檔案。 因為沒有任何標準的方式可標示要清除的檔案，所以沒有任何單一應用程式可以可靠地偵測和清除所有 unessential 檔案。 磁片清理公用程式會藉由分割單一 *磁片清理管理員* 與 *磁片清理處理常式* 集合之間的清除操作來解決此問題。

執行磁片清理公用程式時，使用者會看到下列對話方塊。  (如果電腦上有一個以上的磁片或磁碟分割，系統會先要求使用者選擇磁片磁碟機，然後才會顯示此對話方塊。 ) 

![[清除] 對話方塊的螢幕擷取畫面](images/cleanup1.png)

磁片清理管理員是作業系統的一部分。 它會顯示上圖中顯示的對話方塊、處理使用者輸入，以及管理清除操作。 實際選取和清除不需要的檔案是由 [磁片清理管理員] 清單方塊中顯示的個別磁片清理處理常式所完成。 使用者可以選擇啟用或停用個別處理常式，方法是在 [磁片清理管理員] UI 中選取或清除其核取方塊。

每個處理常式都負責一組妥善定義的檔案。 例如，在圖例中選取的處理常式會負責清除下載的程式檔。 在圖例中選取的處理常式也會提供 [ **View Files** ] 按鈕。 藉由按一下按鈕，使用者可以要求處理常式顯示 UI，通常是 Windows 檔案總管視窗，可讓使用者指定要清除的檔案或檔案類別。

雖然 Windows 有許多磁片清理處理常式，但它們並不是用來處理其他應用程式所產生的檔案。 磁片清理管理員的設計目的是要讓任何開發人員都能執行並註冊自己的磁片清理處理常式，以提供彈性且可擴充的功能。 任何開發人員都可以藉由執行和註冊磁片清理處理常式來擴充可用的磁片清理服務。

產生暫存檔案的所有應用程式都可以執行和註冊磁片清理處理常式。 這麼做可讓使用者有便利且可靠的方式來管理應用程式的暫存檔案。 當您執行此處理程式時，您可以決定哪些檔案受到影響，並決定實際的清除動作。

## <a name="implementation-basics"></a>執行基本概念

清除處理常式是 (COM) 物件的同進程伺服器元件物件模型。 Windows 提供現有的處理常式物件，稱為 DataDrivenCleaner 供您使用。 您也可以選擇自行執行處理常式，以提供更大的彈性。 然後，這些物件可讓您指定如何選取檔案、釋放磁碟空間，以及在執行的處理常式時，顯示選用的 UI 以進行更細微的控制。 本節將討論如何執行您自己的處理常式。 如需有關使用 DataDrivenCleaner 物件的詳細資訊，請參閱 [使用 DataDrivenCleaner 物件](#using-the-datadrivencleaner-object)。

磁片清理處理常式應該執行這五個基本工作。

-   初始化處理常式物件。
-   掃描磁片以判斷可以釋放多少磁碟空間。
-   顯示 UI 以取得要清除哪些檔案的使用者意見反應。 (選用)
-   進行清除。
-   [關閉]。

若要讓「磁片清理管理員」管理這些工作，處理常式必須為 Windows Millennium 版本 (Windows 我) 、Windows 2000 和 Windows XP 的 Windows 98 或 [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)匯出 [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) 。 由於 **IEmptyVolumeCache2** 繼承自 **IEmptyVolumeCache**，因此只新增額外的方法 **InitializeEx**，因此不需要額外的工作來執行兩者。 除非您的處理常式只適用于其中一個作業系統，否則它應該匯出這兩個介面。

若要匯出這些介面，您必須執行對應至五個基本工作的這些方法。

-   [Initialize/InitializeEx](#initializeinitializeex)
-   [GetSpaceUsed](#getspaceused)
-   [Interactivesession.showproperties](#showproperties)
-   [清除](#purge)
-   [停用](#deactivate)

### <a name="initializeinitializeex"></a>Initialize/InitializeEx

執行磁片清理公用程式時，會呼叫兩個相當類似的初始化方法。 Windows 98 disk 清理管理員會呼叫處理常式的 [**IEmptyVolumeCache：： Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize)方法。 不過，Windows Millennium Edition (Windows 我) 、Windows 2000 或 Windows XP disk 清理管理員，則會先嘗試呼叫 [**IEmptyVolumeCache2：： InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) ，而且只有在處理常式未公開 [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)時，才會使用 **IEmptyVolumeCache：： Initialize** 。 磁片清理管理員會將資訊傳遞給方法，例如處理常式的登錄機碼和要清除的磁片區。

這兩種方法都可以傳回各種顯示字串，並設定一或多個旗標。 這兩種方法的主要差異在於如何處理磁片清理管理員中顯示的文字。 下列三個字串會受到影響。



| String       | 目的                                                                            | 初始化                                                                           | InitializeEx                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 顯示名稱 | 處理常式的名稱會顯示在 [磁片清理管理員] 清單方塊中。               | 如果 *ppwszDisplayName* 為 **Null**，則會從登錄取出預設值。 | 您必須在 *ppwszDisplayName* 中指定正確的當地語系化字串，而不會使用任何登錄值。 |
| 描述  | 選取處理常式的名稱時，顯示于清單方塊下方的描述性文字。 | 如果 *ppwszDescription* 為 **Null**，則會從登錄取出預設值。 | 您必須在 *ppwszDescription* 中指定正確的當地語系化字串，而不會使用任何登錄值。 |
| 按鈕文字  | 選擇性按鈕的文字，可讓使用者顯示處理常式的 UI。        | 沒有任何可用的參數。 必須在登錄中指定。                           | 您必須在 *ppwszBtnText* 中指定正確的當地語系化字串，而不會使用任何登錄值。     |



 

在這兩個初始化方法中找到的 *pdwFlags* 參數會辨識同一組旗標。 磁片清理管理員會將這兩個旗標傳遞給方法。

-   **EVCF \_ SETTINGSMODE**

    如果正在依排程執行磁片清理管理員，則會設定 **EVCF \_ SETTINGSMODE** 旗標。 如果設定此旗標，則「磁片清理管理員」不會呼叫 [GetSpaceUsed](#getspaceused)、 [清除](#purge)或 [interactivesession.showproperties](#showproperties) 方法。 處理常式的 [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) 或 [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) 方法必須處理通常由 [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) 和 [**清除**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge)執行的所有工作。 由於沒有機會提供使用者意見反應，因此應該只觸及非常安全地清除的檔案。 您應忽略初始化方法的 *pcwszVolume* 參數，並清除不需要的檔案，不論它們在什麼磁片磁碟機上。

-   **EVCF \_ OUTOFDISKSPACE**

    如果已設定 **EVCF \_ OUTOFDISKSPACE** 旗標，則使用者的磁片磁碟機的空間相當短。 處理常式應該積極地刪除檔案，即使會導致效能遺失也一樣。 不過，處理常式顯然不應該刪除會導致應用程式失敗或使用者遺失資料的檔案。

其餘旗標是由「磁片清理」處理常式所設定，並傳回到「磁片清理管理員」。 如需詳細資訊，請參閱 [**IEmptyVolumeCache：： Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) 和 [**IEmptyVolumeCache2：： InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex)的方法參考頁面。

-   EVCF \_ DONTSHOWIFZERO

    只有當 [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) 傳回的值指出處理常式可以釋放一些磁碟空間時，才會在 [磁片清理管理員] 清單方塊中顯示處理常式。

-   EVCF \_ ENABLEBYDEFAULT

    指定預設會啟用處理常式。 除非使用者在磁片清理管理員的處理常式清單中清除其核取方塊，否則會在每次發生磁片清理時執行它。

-   EVCF \_ ENABLEBYDEFAULT \_ 自動

    指定自動啟用處理常式，以便在排程的清除期間執行。

-   EVCF \_ HASSETTINGS

    如果您的處理常式具有可顯示的 UI，請設定此旗標。 在 [回應] 中，[磁片清理管理員] 會在清單方塊中選取該處理常式時顯示按鈕。 如果按一下該按鈕，「磁片清理管理員」就會呼叫 [**interactivesession.showproperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties)。

-   EVCF \_ REMOVEFROMLIST

    在處理常式執行一次之後，從可用的處理常式清單中刪除處理常式的名稱。 也會一併刪除處理常式的登錄資訊。

### <a name="getspaceused"></a>GetSpaceUsed

磁片清理管理員會呼叫這個方法，以判斷磁片清理處理常式可能可用的空間量。 [磁片清理管理員] 接著會在清單方塊中顯示處理常式名稱右邊的值。 當管理員啟動時，以及在管理員的主要 UI 顯示之前，所有向「磁片清理管理員」註冊的處理常式都會執行這項操作。 呼叫 [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) 時，處理常式應該掃描其負責的檔案、判斷哪些是清除候選項目，並傳回可釋放的磁碟空間量。

由於掃描可能是很長的程式，因此磁片清理管理員會使用這個方法的 *picb* 參數，將指標傳遞至 [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) 介面。 處理常式會在掃描期間定期使用介面，以呼叫 [**IEmptyVolumeCacheCallBack：： ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)，這有兩個用途。

-   允許 [磁片清理管理員] 更新進度列，通知使用者掃描的進度。
-   當按一下進度視窗的 [ **取消** ] 按鈕時，通知處理常式停止掃描。 該按鈕事件不會直接傳達給處理常式;相反地，磁片清理管理員會 \_ 在下一次 [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) 呼叫 [**IEmptyVolumeCacheCallBack：： ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)時，傳回 E ABORT。

### <a name="showproperties"></a>Interactivesession.showproperties

開始清除之前，處理常式可以使用 Windows 檔案總管視窗的形式來顯示 UI，以允許使用者查看由處理常式選取要清除的檔案或檔案類別清單。 如果處理常式在呼叫 [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize)或 [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex)時設定了 **EVCF \_ HASSETTINGS** 旗標，使用者就可以在 [磁片清理管理員] 中，按一下針對該目的所顯示的按鈕來要求 UI。 按鈕文字會因處理常式而異，但 [View Files]、[View Pages] 和 [Options] 是常見的標籤。

按一下按鈕時，「磁片清理管理員」會呼叫 [**interactivesession.showproperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties) 以提示處理常式顯示 UI。 UI 應該建立為視窗的子系，其控制碼會以 **interactivesession.showproperties** 方法的 *hwnd* 參數傳遞。

### <a name="purge"></a>清除

「磁片清理管理員」會呼叫處理常式的 [**清除**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) 方法來設定動態清除。 方法的 *picb* 參數是磁片清理管理員的 [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) 介面指標。 如同 [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) 方法，處理常式應該定期使用回呼介面來報告其進度，並查詢「磁片清理管理員」是否已按下 [ **取消**]。 不過請注意， **清除** 方法必須呼叫 [**IEmptyVolumeCacheCallBack：:P urgeprogress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress)，而不是 [**ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)。

### <a name="deactivate"></a>停用

當「磁片清理管理員」準備關閉時，會呼叫「 [**停用**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-deactivate) 」方法。 處理常式應該執行任何必要的清除工作並傳回。 如果您不想要再次執行處理常式，請在初始化方法的 *pdwFlags* 參數中設定 **EVCF \_ REMOVEFROMLIST** 旗標。 如果設定此旗標，則磁片清理管理員會從其清單中移除處理常式，並刪除處理常式的登錄專案。 您必須重新加入登錄專案，才能再次執行處理常式。 此旗標通常用於只執行一次的處理常式。

## <a name="registering-a-disk-cleanup-handler"></a>註冊磁片清理處理常式

若要將處理常式新增至 [磁片清理管理員] 清單，必須將某些索引鍵和值新增至 Windows 登錄。

-   [註冊處理常式的 CLSID](#registering-a-handlers-clsid)
-   [使用磁片清理管理員來註冊處理常式：一般](#registering-a-handler-with-the-disk-cleanup-manager-general)
-   [使用磁片清理管理員來註冊處理常式： Windows 2000 或更新版本的系統](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
-   [使用 DataDrivenCleaner 物件](#using-the-datadrivencleaner-object)
-   [磁片清理處理常式的註冊範例](#example-registration-of-a-disk-cleanup-handler)

### <a name="registering-a-handlers-clsid"></a>註冊處理常式的 CLSID

和所有 COM 物件一樣，處理常式物件的 GUID 和 DLL 都必須在 **HKEY \_ 類別 \_ 根目錄** 的 **CLSID** 機碼下註冊。 您也可以在 [磁片清理管理員] 清單方塊中，註冊顯示于處理常式名稱旁邊的圖示，但這是選擇性的。 下列範例會顯示相關的索引鍵、值和資料。

```
HKEY_CLASSES_ROOT
   CLSID
      Handler's GUID
         DefaultIcon
            (Default) = Handler's Icon Path, Icon Index
         InprocServer32
            (Default) = Handler's DLL path
            ThreadingModel = Apartment
```

### <a name="registering-a-handler-with-the-disk-cleanup-manager-general"></a>使用磁片清理管理員來註冊處理常式：一般

若要完成註冊，處理常式必須加入保存其細節的金鑰，如下所示。 本節的其餘部分將討論此機碼的內容。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Handler's Key
```

一般而言，保存處理常式細節的金鑰名稱會以它所處理的檔案類型命名，例如 **下載的程式** 檔案，但這不是必要條件。 下表詳細說明在此機碼下找到的可能值。

> [!Note]  
> 只有指定處理常式之類別識別碼 (CLSID) 的預設值，其他所有值都是選擇性的。

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>類型</th>
<th>意義</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>預設</td>
<td>REG_SZ</td>
<td>在<strong>HKEY_CLASSES_ROOT</strong>clsid 下註冊的處理常式 CLSID \ <strong> </strong>。</td>
</tr>
<tr class="even">
<td>AdvancedButtonText</td>
<td>REG_SZ</td>
<td>選擇性按鈕的文字，使用者可以按一下此按鈕以顯示處理常式的 UI。 您可以在字元之前放置 & 字元，以指派按鈕的鍵盤快速鍵。 公開 <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2：： InitializeEx</strong></a>的處理常式會忽略 AdvancedButtonText 值。</td>
</tr>
<tr class="odd">
<td>CleanupString</td>
<td>REG_SZ</td>
<td>指定可執行檔和選擇性命令列參數的命令列。 此命令列會在磁片清理完成時執行。</td>
</tr>
<tr class="even">
<td>CSIDL</td>
<td>REG_DWORD</td>
<td>要包含在檔案搜尋中之特殊資料夾的系統獨立識別碼。 此值必須輸入為實例的數值，0x0000001c，而不是 CSIDL_LOCAL_APPDATA。 如需可能值的清單，請參閱 <a href="/windows/desktop/shell/csidl"><strong>CSIDL</strong></a>。 只能使用單一值。<br/> 如果指定了資料夾值，則會在該資訊前面加上 CSIDL 值所指出的位置，以撰寫搜尋路徑。 例如，請考慮下列案例。<br/>
<ul>
<li>CSIDL 值會指定為 0x0000000d (CSIDL_MYMUSIC) </li>
<li>[我的音樂] 資料夾位於 c:\documents and 和設定 \ 使用者<em>名稱</em>\My 音樂</li>
<li>資料夾值包含 &quot; Jazz\Singers&quot;</li>
</ul>
該案例的結果是磁片清理處理常式會搜尋 c:\documents and 和設定 \ 使用者<em>名稱</em>\My Music\Jazz\Singers 資料夾。 請注意，如果資料夾值前面沒有斜線，則會加以新增。<br/></td>
</tr>
<tr class="odd">
<td>描述</td>
<td>REG_SZ</td>
<td>選取處理常式的名稱時，顯示在 [磁片清理管理員] 清單方塊下方的描述性文字。 您可以在這裡說明處理常式的功能、其關注的檔案，以及 elucidatory 給使用者的任何其他資訊。 如果<a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2：： InitializeEx</strong></a>不是由處理常式公開，則在呼叫方法時，可以在<em>ppwszDescription</em>參數中指定替代字串，藉此覆寫此文字。 <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong></strong></a></td>
</tr>
<tr class="even">
<td>顯示</td>
<td>REG_SZ</td>
<td>要在 [磁片清理管理員] 清單方塊中顯示的處理常式名稱。 如果<a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2：： InitializeEx</strong></a>不是由處理常式公開，則在呼叫方法時，可以在<em>ppwszDisplayName</em>參數中指定替代字串，藉此覆寫此文字。 <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong></strong></a></td>
</tr>
<tr class="odd">
<td>FileList (檔案清單)</td>
<td>REG_SZ 或 REG_MULTI_SZ</td>
<td>此處理程式所搜尋和清除的檔案清單。 您可以使用來指定萬用字元？ 或 * 個字元。 如果值是 REG_SZ 類型，則會使用多個擴充功能來分隔 |或：字元，其中任一端沒有空格。<br/> 如果在旗標值中設定 DDEVCF_REMOVEDIRS 旗標，這些值可以指定目錄名稱和檔案。<br/></td>
</tr>
<tr class="even">
<td>Flags</td>
<td>REG_DWORD 或 REG_BINARY</td>
<td>控制搜尋和清除程式元素的旗標。 下列一個或多個值。
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001) 。 以遞迴方式搜尋和移除。</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002) 。 當處理常式執行一次之後，請將它從登錄中移除。</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004) 。 移除符合搜尋條件的檔案（即使它們是唯讀的）。</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008) 。 移除符合搜尋條件的檔案，即使它們是系統檔案也一樣。</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010) 。 移除符合搜尋條件的檔案（即使它們是隱藏的檔案）。</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020) 。 如果沒有任何檔案符合搜尋準則，請勿在 [磁片清理管理員] 中顯示此處理程式。</li>
<li>DDEVCF_REMOVEDIRS (0x00000040) 。 比對目錄的 FileList 值，並移除相符專案及其所有子目錄。</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080) 。 只有在磁片清理管理員透過 <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache：： Initialize</strong></a> 或 <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2：： InitializeEx</strong></a>設定 EVCF_OUTOFDISKSPACE 旗標時，才會執行此處理程式。</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100) 。 一旦清除程式執行之後，請移除指定檔案的上層目錄。</li>
<li>DDEVCF_PRI加值稅E_LASTACCESS (0x10000000) 。 如果有提供，請使用 LastAccess 值，在查明應清除的檔案。 使用 <a href="#using-the-datadrivencleaner-object">DataDrivenCleaner</a> 時，會忽略此旗標（一律使用任何提供的 LastAccess 值）。</li>
</ul></td>
</tr>
<tr class="odd">
<td>資料夾</td>
<td>REG_SZ、REG_MULTI_SZ 或 REG_EXPAND_SZ</td>
<td>特定資料夾或資料夾，用來搜尋符合 FileList 值中專案的專案。 您可以使用來指定萬用字元？ 或 * 個字元。 如果值是 REG_SZ 類型，則會使用多個資料夾名稱來分隔 |字元，其中任何一側都沒有空格。<br/> 如果有 CSIDL 值，此值中只能指定一個資料夾。 CSIDL 值所指示的位置會在該資料夾路徑的前面加上，以撰寫搜尋路徑。 如需範例，請參閱 CSIDL 值描述。<br/> 如果 Windows Vista Service Pack 1 (SP1) 和更新版本中沒有此值，則會忽略清除處理常式，並在初始化時傳回 S_FALSE。<br/> 如果此值不存在於 Windows Vista 和更早版本的原始版本上，則會使用目前磁片區的根資料夾。 在該情況下，需要 DDEVCF_DOSUBDIRS 旗標來搜尋整個磁片磁碟機。 如果沒有它，就只會搜尋根資料夾本身。<br/> 必須指定磁片磁碟機或磁片磁碟機。 這可以透過 CSIDL 值或 REG_EXPAND_SZ 字串來提供。 不過，您必須在資料夾名稱中指定要搜尋的磁片磁碟機，才能禁止這些選項。 使用？：搜尋目前磁片磁碟機上的資料夾。<br/></td>
</tr>
<tr class="even">
<td>>iconpath</td>
<td>REG_SZ 或 REG_EXPAND_SZ</td>
<td>資源的路徑，從中取得要與處理常式關聯的圖示。</td>
</tr>
<tr class="odd">
<td>LastAccess</td>
<td>REG_DWORD 或 REG_BINARY</td>
<td>自上次存取檔案以來經過的天數，或針對要視為清除的檔案或目錄建立的目錄。</td>
</tr>
<tr class="even">
<td>優先順序</td>
<td>REG_DWORD 或 REG_BINARY</td>
<td>判斷處理常式相對於其他處理常式的執行順序。 數位愈高，處理常式在處理常式中執行的程式就越早。 沒有任何已定義的範圍可接受任何數位。</td>
</tr>
<tr class="odd">
<td>PropertyBag</td>
<td>REG_SZ</td>
<td>用來為顯示名稱、描述和按鈕文字提供當地語系化文字之資源的 CLSID。 當處理常式未執行<a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>IEmptyVolumeCache</strong></a> ，且處理常式是在 Microsoft Windows NT 或 Windows XP 下執行時，此資源就很有用。<br/> 「磁片清理管理員」會先檢查處理程式的初始化常式是否傳回這些字串，就像 <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2</strong></a> 的情況一樣。 若失敗，管理員接下來會在此值中開啟名為的屬性包。 如果未提供任何內容，則會從登錄抓取文字。<br/></td>
</tr>
<tr class="even">
<td>StateFlags</td>
<td>REG_DWORD</td>
<td>藉由從命令列執行磁片清理管理員的可執行檔 Cleanmgr.exe，您可以宣告清除 <em>設定檔</em>。 這些設定檔是由可用的處理常式子集所組成，而且會獲得唯一的數值標籤。 這可讓您在不同時間自動執行不同組的處理常式。<br/> 命令列 &quot;cleanmgr.exe/sageset：<strong>nnnn</strong> &quot; ，其中<strong>nnnn</strong>是唯一的數值標籤，會顯示 UI，讓您選擇要包含在該設定檔中的處理常式。 除了定義設定檔，sageset 參數也會將名為 StateFlags<strong>nnnn</strong>的值寫入，其中 <strong>nnnn</strong> 是您在參數中使用的標籤，以及 <strong>VolumeCaches</strong>底下的所有子機碼。 這些專案有兩個可能的資料值。
<ul>
<li>0：當此設定檔執行時，請勿執行此處理程式。</li>
<li>2：執行此設定檔時，請包含此處理程式。</li>
</ul>
<br/> 例如，假設命令列 &quot;cleanmgr.exe/sageset： 1234 &quot; 執行。 在顯示的 UI 中，使用者選擇下載的 <strong>程式</strong>檔，但不會選擇 [ <strong>網際網路暫存</strong>檔案]。 接著會將下列值寫入登錄中。<br/>
<pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Downloaded Program Files
                        StateFlags1234 = 0x00000002
                     Internet Cache Files
                        StateFlags1234 = 0x00000000</code></pre>
<br/> 命令列 &quot;cleanmgr.exe/sagerun：<strong>nnnn</strong> &quot; ，其中<strong>nnnn</strong>的值符合以 sageset 參數宣告的標籤，會執行在該設定檔中選取的所有處理常式。<br/> 當磁片清理正常執行時，會將一般 StateFlags 值寫入登錄中。 此值只會儲存狀態 (在最後一次呈現為使用者的選項時，檢查或取消核取處理常式) 。 這些專案有兩個可能的資料值。
<ul>
<li>0：未選取處理常式。</li>
<li>1：已選取處理常式。</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>使用磁片清理管理員來註冊處理常式： Windows 2000 或更新版本的系統

在登錄中指定顯示文字可能會使軟體難以當地語系化。 基於這個理由，Windows 2000 和 Windows XP 支援 [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)介面及其慣用的初始化方法 [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex)。 在 Windows 2000 或更新版本下，一律會嘗試在 [**IEmptyVolumeCache：： Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize)之前呼叫 **IEmptyVolumeCache2：： InitializeEx** 。 如果未公開 **IEmptyVolumeCache2** ，系統只會使用 **initialize** 來初始化處理常式。

就登錄而言，Windows 2000 或更新版本下的唯一差異在於，您可以在處理常式公開 [**IEmptyVolumeCache2：： InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex)時省略 AdvancedButtonText、顯示及描述值。 這些值（包含適當當地語系化的文字）在呼叫 **InitializeEx** 時，會提供給「磁片清理管理員」。

### <a name="using-the-datadrivencleaner-object"></a>使用 DataDrivenCleaner 物件

作業系統會提供基本的磁片清理處理常式（稱為 DataDrivenCleaner）。 若要使用此物件做為處理常式，而不是執行自己的處理常式，請使用 CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} 做為 **VolumeCaches** 上處理常式子機碼的預設值，如使用 [磁片清理管理員註冊處理常式所述：一般](#registering-a-handler-with-the-disk-cleanup-manager-general)。

DataDrivenCleaner 不會公開 [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)，因此會透過登錄提供顯示和描述值。 宣告這些字串時，請注意這可能會導致當地語系化問題。 您可以透過 PropertyBag 值提供當地語系化文字。 AdvancedButtonText 值會被忽略，因為沒有 UI，因此沒有可顯示的按鈕，此處理程式會提供此值。

### <a name="example-registration-of-a-disk-cleanup-handler"></a>磁片清理處理常式的註冊範例

以下顯示電話公司所執行之磁片清理處理常式的註冊範例。 此處理程式會同時執行 [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache)和 [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)，因此會在執行 Windows 98 的電腦上使用時，提供 AdvancedButtonText、描述和顯示值。 此處理程式會結合 CSIDL 和資料夾值，以搜尋 C： Program 中的檔案 \\ \\ 電話的公司 \\ Temp 目錄，並設定 DDEVCF \_ DOSUBDIRS 旗標，因此也會搜尋其子目錄。 只有使用 .tmp 和 tpc 副檔名的檔案會被視為清除，而且會 \_ 設定 DDEVCF 私用 \_ LASTACCESS 旗標，如此一來，就只會考慮未存取14天以上的檔案。 此外， \_ 也會設定 DDEVCF DONTSHOWIFZERO 旗標，讓處理常式不會出現在清單中，除非它找到清除候選項目。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     The Phone Company Files
                        (Default) = {the CLSID GUID}
                        AdvancedButtonText = &View Files
                        CleanupString = c:\tpc.exe
                        CSIDL = 0x00000026
                        Description = Old temporary files.
                        Display = The Phone Company Files
                        FileList = *.tmp|*.tpc
                        Flags = 0x10000021
                        Folder = \The Phone Company\Temp
                        IconPath = c:\Program Files\The Phone Company\tpc.dll,2
                        LastAccess = 0x0000000e
                        Priority = 200
                        PropertyBag = {Property Bag CLSID GUID}
```

 

