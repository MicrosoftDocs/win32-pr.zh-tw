---
description: 討論新的工作列功能，包括合併啟動與切換、工作列按鈕的增強功能，例如單鍵存取檔和應用程式特定的工作、傳輸控制項和狀態通知、縮圖標記法，以及根據索引標籤式應用程式中的個別索引標籤來重新排列工作列按鈕的功能。
ms.assetid: cbf2b07d-d67c-4755-888c-d40692d13cae
title: 工作列擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92cb8f100da2c7b5173319c25369a0ada7284b2ff5f4adbfe9b519c0ee96485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773748"
---
# <a name="taskbar-extensions"></a>工作列擴充功能

從 Windows 7 開始，在讓使用者以快速且有效率的方式進行的指導準則下，已大幅擴充工作列。 為了達到這個目的，使用者需要完成的應用程式視窗、檔案和命令現在會集中到單一工作列按鈕，以合併先前散佈的資訊來源和控制項。 使用者現在可以在單一位置尋找個別檔或索引標籤的一般工作、最近和頻繁的檔案、警示、進度通知和縮圖。

-   [整合啟動和切換](#unified-launching-and-switching)
-   [跳躍清單](#jump-lists)
-   [目的地](#destinations)
-   [工作](#tasks)
-   [自訂跳躍清單](#customizing-jump-lists)
-   [縮圖工具列](#thumbnail-toolbars)
-   [圖示重迭](#icon-overlays)
-   [進度列](#progress-bars)
-   [Deskbands](#deskbands)
-   [通知區域](#notification-area)
-   [縮圖](#thumbnails)
-   [相關主題](#related-topics)

## <a name="unified-launching-and-switching"></a>整合啟動和切換

從 Windows 7 工作列，快速啟動不再是個別的工具列。 通常包含快速啟動的啟動器快速鍵現在已釘選到工作列本身，並以目前正在執行之應用程式的按鈕混合。 當使用者從已釘選的啟動器快速鍵啟動應用程式時，只要應用程式正在執行，圖示就會轉換成應用程式的工作列按鈕。 當使用者關閉應用程式時，按鈕會還原為圖示。 但是，執行中應用程式的啟動程式快捷方式和按鈕只是 Windows 7 工作列按鈕的不同形式。

![windows 7 工作列](images/taskbar/taskbar.png)

預設會針對新的安裝釘選一組小型應用程式。 除了上述以外，只有使用者可以釘選更多應用程式;不允許應用程式以程式設計方式釘選。

快速啟動的顯示桌面功能現在位於工作列最右邊。 將滑鼠停留在此區域，會使所有作用中視窗變成透明，顯示桌面。 按一下該區域會執行將所有視窗最小化並切換至桌面的熟悉動作。

當應用程式正在執行時，其工作列按鈕會變成可存取下列所有功能的單一位置，以下將詳細討論。

-   工作[：即使](#tasks)應用程式不在執行中，也會出現一般的應用程式命令。
-   [目的地](#destinations)：最近和經常存取的應用程式特定檔案。
-   [縮圖](#thumbnails)：視窗切換，包括個別索引標籤和檔的切換目標。
-   [縮圖工具列](#thumbnail-toolbars)：來自縮圖本身的基本應用程式控制。
-   [進度](#progress-bars) 列和 [圖示](#icon-overlays)重迭：狀態通知。

工作列按鈕可以代表啟動器、單一應用程式視窗或群組。 稱為「應用程式使用者模型識別碼」的識別碼 (AppUserModelID) 會指派給每個群組。 您可以指定 AppUserModelID 來覆寫標準工作列群組，讓 windows 成為相同群組的成員，但在其他情況下可能不會看到。 群組的每個成員都會在縮圖飛出視窗中提供個別的預覽，當滑鼠停留在群組的工作列按鈕上時，就會顯示此圖表。 請注意，群組本身仍是選擇性的。

從 Windows 7 開始，使用者現在可以透過拖放作業來重新排列工作列按鈕。

> [!Note]  
> 快速啟動資料夾 ([* * * * FOLDERID \_ 快速啟動 *](knownfolderid.md) * *) 仍可提供回溯相容性，但不再有快速啟動的 UI。 不過，新的應用程式應該不會要求在安裝期間將圖示新增至快速啟動。

 

如需詳細資訊，請參閱 [應用程式使用者模型識別碼 (AppUserModelIDs) ](appids.md)。

## <a name="jump-lists"></a>跳躍清單

使用者通常會以存取檔或在程式中執行工作的意圖來啟動程式。 遊戲程式的使用者可能想要取得已儲存的遊戲或啟動為特定字元，而不是從頭重新開機遊戲。 為了讓使用者更有效率地達成最終目標，會 [將與應用程式相關聯](#tasks)的 [目的地](#destinations)清單和一般工作附加至該應用程式的工作列按鈕 (以及對等的 [**開始**] 功能表項目) 。 這是應用程式的捷徑清單。 您可以使用捷徑清單 (應用程式未執行) 或是否代表一或多個視窗時，工作列按鈕是否處於啟動器狀態。 以滑鼠右鍵按一下工作列按鈕，就會顯示應用程式的捷徑清單，如下圖所示。

![具有釘選、經常性和工作類別的跳躍清單](images/taskbar/jumplist.png)

根據預設，標準捷徑清單包含兩個類別：最近的專案和釘選的專案，但因為只有具有內容的類別會顯示在 UI 中，所以不會在第一次啟動時顯示這些類別。 永遠存在的應用程式啟動圖示 (啟動應用程式的更多實例) 、從工作列釘選或取消釘選應用程式的選項，以及任何開啟視窗的 **關閉** 命令。

## <a name="destinations"></a>目的地

**最近** 和 **頻繁** 的類別會被視為包含目的地。 目的地（通常是檔案、檔或 URL）可以編輯、流覽、查看等等。 請將目的地視為某件事，而不是動作。 通常，目的地是 Shell 命名空間中的專案，以 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) 或 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)表示。 目的地清單的這些部分類似于 [ **開始** ] 功能表的 [最近使用的檔] 清單 (預設不會再顯示) 和常用的應用程式清單，但它們是應用程式特有的，因此更準確且更適合使用者使用。 目的地清單中使用的結果是透過呼叫 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)來計算。 請注意，當使用者從 Windows 檔案總管開啟檔案，或使用 [一般檔案] 對話方塊來開啟、儲存或建立檔案時，系統會自動為您呼叫 **SHAddToRecentDocs** ，這會導致許多應用程式取得目的地清單中顯示的最新專案，而不會有任何動作。

啟動目的地就像使用 [ **開啟方式** ] 命令來啟動專案一樣。 應用程式隨即啟動，且該目的地已載入並準備就緒可供使用。 目的地清單中的專案也可以從清單拖曳至放置目的地，例如電子郵件訊息。 藉由將這些專案集中在目的地清單中，就能讓使用者以較快的速度執行，也就是目標。

當專案出現在 [最近] 清單中的 [ **最近** ] 類別 (或 [ **常用** ] 分類或 [自訂類別](#customizing-jump-lists) 時，) 稍後章節中所討論的專案，使用者可能會想要確保專案一律在清單中，以供快速存取。 若要完成這項工作，可以將該專案釘選到清單，將專案加入至已 **釘** 選的類別。 當使用者主動使用目的地時，他或她希望能夠輕鬆地將它釘選到應用程式的目的地清單。 在使用者完成工作之後，他或她只是取消固定專案。 此使用者控制項可讓清單保持整齊且相關。

目的地清單可視為應用程式特定版本的 [ **開始** ] 功能表。 目的地清單不是快捷方式功能表。 目的地清單中的每個專案都可以用滑鼠右鍵按一下它自己的快捷方式功能表。

### <a name="apis"></a>API

-   [**IApplicationDestinations::RemoveDestination**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination)
-   [**IApplicationDestinations::RemoveAllDestinations**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations)
-   [**IApplicationDocumentLists::GetList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)
-   [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

## <a name="tasks"></a>工作

捷徑清單的另一個內建部分 **是 [工作** ] 類別。 雖然目的地是一件事，但是工作是一項動作，而在此情況下，它是應用程式特定的動作。 以另一種方式，目的地是名詞，而工作則是動詞。 一般情況下，工作是具有命令列引數的 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 專案，表示應用程式可以觸發的特定功能。 同樣地，概念是盡可能將與應用程式相關的資訊集中在一起。

應用程式會根據程式的功能以及使用者預期使用的重要事項來定義工作。 工作應該是無內容的，因為應用程式不需要執行，就能運作。 它們也應該是一般使用者在應用程式中執行的統計最常見動作，例如撰寫電子郵件訊息或在郵件程式中開啟行事曆、在文字處理器中建立新檔、在特定模式中啟動應用程式，或啟動其中一個子命令。 應用程式應該不會讓功能表與標準使用者不需要或單次動作（例如註冊）的先進功能產生混亂。 請勿將工作用於促銷專案，例如升級或特殊優惠。

強烈建議工作清單是靜態的。 無論應用程式的狀態或狀態為何，都應該維持不變。 雖然您可以動態地變更清單，但您應該考慮這樣做可能會讓不希望目的清單的部分變更的使用者混淆。

### <a name="apis"></a>API

-   [**ICustomDestinationList::AddUserTasks**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)

## <a name="customizing-jump-lists"></a>自訂跳躍清單

應用程式可以定義自己的類別，並在捷徑清單中新增或取代標準 **最新** 且 **經常** 分類的類別。 應用程式可以根據應用程式的架構和預定用途，在這些自訂類別中控制自己的目的地。 下列螢幕擷取畫面顯示具有歷程記錄類別的自訂捷徑清單。

![自訂跳躍清單](images/taskbar/customjumplist.png)

如果應用程式決定提供自訂類別，則該應用程式會負責填入它。 類別目錄內容仍然應該是使用者特定的，而且會根據使用者的歷程記錄、動作或兩者，但透過自訂類別，應用程式可以決定要追蹤的內容，以及它想要忽略的內容（也許是根據應用程式選項）。 例如，音訊程式可能會選擇只包含最近播放的專輯，並忽略最近播放的個別曲目。

如果使用者已從清單中移除專案，這一律是使用者選項，則應用程式必須接受該專案。 應用程式也必須確保清單中的專案有效，或如果已刪除，則會正常地失敗。 您可以透過程式設計方式移除個別專案或清單的整個內容。

目的地清單中的專案數目上限是由系統根據各種因素（例如顯示解析度和字型大小）來決定。 如果沒有足夠的空間可容納所有類別目錄中的所有專案，則會從底部截斷。

### <a name="apis"></a>API

-   [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)
-   [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)
-   [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)

## <a name="thumbnail-toolbars"></a>縮圖工具列

若要在不讓使用者還原或啟動應用程式視窗的情況下，提供特定視窗主要命令的存取權，您可以將現用的工具列控制項內嵌在該視窗的縮圖預覽中。 例如，Windows Media Player 可能會提供標準媒體傳輸控制項，例如播放、暫停、靜音及停止。 UI 會在縮圖正下方顯示此工具列，如下圖所示，它並不涵蓋任何部分。

![windows media player 的縮圖工作列，具有三個按鈕： [上一頁]、[播放] 和 [轉寄]](images/taskbar/thumbbar.png)

這個工具列只是熟悉的標準工具列通用控制項。 最多有七個按鈕。 每個按鈕的識別碼、影像、工具提示和狀態都是在結構中定義，然後再傳遞至工作列。 應用程式可以顯示、啟用、停用或隱藏縮圖工具列上的按鈕，如其目前的狀態所要求。

因為顯示縮圖的空間有限，以及要顯示的可變動縮圖數目，所以不保證應用程式具有指定的工具列大小。 如果空間有限，工具列中的按鈕會由右至左截斷。 因此，當您設計工具列時，您應該設定與按鈕相關聯之命令的優先順序，並確保最重要的是最重要的，而且最不可能因為空間問題而卸載。

> [!Note]  
> 當應用程式顯示視窗時，系統會建立其工作列按鈕。 當按鈕已就緒時，工作列會將 **TaskbarButtonCreated** 訊息傳送至視窗。 其值是藉由呼叫 [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) (L ( "TaskbarButtonCreated" ) ) 來計算。 在呼叫任何 [**ITaskbarList3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3) 方法之前，您的應用程式必須先接收該訊息。

 

### <a name="api"></a>API

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ITaskbarList3::ThumbBarUpdateButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons)
-   [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="icon-overlays"></a>圖示重迭

應用程式可以透過其工作列按鈕，在按鈕上顯示小重迭，以將特定通知和狀態傳達給使用者。 這些重迭類似于快速鍵或安全性通知所使用的現有覆迭類型，會顯示在按鈕的右下角。 若要顯示重迭圖示，工作列必須是預設的大型圖示模式，如下列螢幕擷取畫面所示。

![具有重迭的 windows messenger 工作列按鈕，表示可用的狀態](images/taskbar/taskbaroverlay.png)

圖示重迭可作為狀態的內容通知，其目的是要讓個別通知區域狀態圖示的需求不會與使用者傳達該資訊。 比方說，Microsoft Outlook 中目前顯示在通知區域中的新郵件狀態，現在可透過工作列按鈕上的重迭來指出。 同樣地，您必須在開發週期中決定哪一個方法最適合您的應用程式。 重迭圖示的目的是要提供重要、長期的狀態或通知，例如網路狀態、messenger 狀態或新郵件。 使用者不應該看到不斷變化的重迭或動畫。

由於單一重迭會在工作列按鈕上重迭，而不是在個別視窗縮圖上，因此這是每個群組的功能，而不是每個視窗。 您可以從工作列群組中的個別視窗接收覆迭圖示的要求，但不會將它們排入佇列。 最後收到的重迭是所顯示的重迭。

### <a name="apis"></a>API

-   [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon)

## <a name="progress-bars"></a>進度列

工作列按鈕可以用來顯示進度列。 這可讓視窗提供進度資訊給使用者，使用者不需要切換至視窗本身。 使用者可以在另一個應用程式中保持生產力，同時查看在其他視窗中發生的一或多個作業進度。 它的目的是工作列按鈕的進度列會在視窗本身反映更詳細的進度指標。 這項功能可用來追蹤檔案複製、下載、安裝、媒體燒錄或任何即將花費一段時間的作業。 這項功能不適用於一般的周邊動作，例如載入網頁或列印檔案。 該進度類型應該會繼續顯示在視窗的狀態列中。

工作列按鈕的進度列與熟悉的進度列控制項的體驗類似。 它可以根據作業的完成百分比顯示確定進度，或使用不定的天棚樣式進度來表示作業正在進行中，而不會有剩餘時間的預測。 它也會顯示作業已暫停或發生錯誤，且需要使用者介入。

### <a name="apis"></a>API

-   [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate)
-   [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue)

## <a name="deskbands"></a>Deskbands

在 Windows 7 之前的 Windows 版本中，與縮圖工具列功能類似的內容，可以透過 deskband （在工作列中裝載的工具列）來達成。 比方說，Windows Media Player 可以將工作列最小化為一組傳輸控制項，而不是標準按鈕。 在 Windows 7 中，仍可執行 deskbands，而且縮圖工具列不打算全部取代。 並非所有的應用程式都能成為縮圖工具列，而另一個解決方案（例如 deskband 或目的地清單中的工作）可能是您的應用程式的正確答案;您必須決定哪一個解決方案最適合您的應用程式，做為開發週期的一部分。 不過，請注意，deskbands 必須支援啟用半透明度 ( 「玻璃」 ) 的 Windows Aero 和 [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)介面。

### <a name="apis"></a>API

-   [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

## <a name="notification-area"></a>通知區域

通知區域已有變更，可讓使用者更充分掌控工作列上所顯示的圖示。 所有通知圖示現在都會預設為隱藏，而且無法以程式設計方式控制其可見度。 只有使用者可以選擇要出現在工作列上的通知圖示。 顯示通知氣球時，圖示會暫時顯示出來，但使用者也可以選擇將其解除回應。 因此，當您想要讓應用程式將該資訊傳達給您的使用者時，工作列按鈕上的圖示重迭會成為很好的選擇。

## <a name="thumbnails"></a>縮圖

在 Windows Vista 中，將滑鼠停留在應用程式的工作列按鈕上，會顯示表示執行中視窗的縮圖。 如果工作列已折迭應用程式的視窗，縮圖會顯示為堆疊來呈現，但縮圖本身只會顯示使用中視窗。

在 Windows 7 中，群組的每個成員都會顯示為個別的縮圖，而且現在也是切換目標。 應用程式可以定義其子系 (例如真正的子視窗、個別檔或索引標籤) 並且針對每個視窗提供相對應的縮圖，即使它們通常不會出現在工作列中。 這可讓使用者直接切換到他們想要的應用程式，而不是切換至應用程式，然後切換到其目的地。 例如，多重文件介面 (MDI) /tabbed-document 介面 (TDI) 應用程式可讓每個檔或索引標籤顯示為個別的縮圖，並在滑鼠停留在群組的工作列按鈕時切換目標。

![代表 windows internet explorer 中個別索引標籤的三個工作列縮圖](images/taskbar/taskbarthumbnails.png)

> [!Note]  
> 如同 Windows Vista 中，Aero 必須為作用中，才能查看縮圖。

 

### <a name="api"></a>API

-   [**ITaskbarList3::RegisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab)
-   [**ITaskbarList3::SetTabActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive)
-   [**ITaskbarList3::SetTabOrder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder)
-   [**ITaskbarList3::UnregisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab)
-   [**ITaskbarList4::SetTabProperties**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties)

Windows 的縮圖表示通常是自動的，但在結果不是最佳的情況下，可以明確指定縮圖。 依預設，只有最上層視窗會自動產生縮圖，而子視窗的縮圖會顯示為一般標記法。 這可能會導致不理想的 (，甚至讓終端使用者的) 體驗感到混淆。 例如，每一個子視窗的特定切換目標縮圖，可提供更好的使用者體驗。

### <a name="api"></a>API

-   [**DwmSetWindowAttribute**](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
-   [**DwmSetIconicThumbnail**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticonicthumbnail)
-   [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap)
-   [**DwmInvalidateIconicBitmaps**](/windows/win32/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
-   [**WM \_ DWMSENDICONICTHUMBNAIL**](../dwm/wm-dwmsendiconicthumbnail.md)
-   [**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**](../dwm/wm-dwmsendiconiclivepreviewbitmap.md)

您可以選取視窗的特定區域以做為縮圖。 當應用程式知道其檔或索引標籤在縮圖大小觀看時看起來很類似時，這會很有用。 然後，應用程式可以選擇只顯示其工作區的一部分，讓使用者可以用來區分縮圖。 不過，將滑鼠游標停留在任何縮圖上，會顯示其背後的完整視窗，讓使用者也可以快速流覽它們。

如果縮圖超過可顯示的數目，則預覽會還原為舊版的縮圖或標準圖示。

### <a name="api"></a>API

-   [**ITaskbarList3::SetThumbnailClip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip)

若要將 [ **釘選到工作列** ] 新增至專案的快捷方式功能表（通常只需要包含 [IsShortCut](./links.md) 專案的檔案類型），請註冊適當的內容功能表處理常式。 這也適用于 [ **釘選到開始] 功能表**。 如需詳細資訊，請參閱 [註冊 Shell 延伸模組處理常式](reg-shell-exts.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作列](taskbar.md)
</dt> <dt>

[應用程式使用者模型識別碼 (AppUserModelIDs) ](appids.md)
</dt> <dt>

[通知和通知區域](notification-area.md)
</dt> </dl>

 

 
