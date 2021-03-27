---
description: 當 Shell 偵測到插入新媒體或熱插即用裝置的附件時，會決定裝置或媒體的內容。 [自動播放] （視其目前的設定而定）會執行下列其中一項動作。
title: 使用和設定自動播放
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689828"
---
# <a name="using-and-configuring-autoplay"></a>使用和設定自動播放

當 Shell 偵測到插入新媒體或熱插即用裝置的附件時，會決定裝置或媒體的內容。 [自動播放] （視其目前的設定而定）會執行下列其中一項動作。

-   自動播放內容。
-   顯示對話方塊，提示使用者選擇單一內容類型的預設處理常式。
-   顯示混合內容的情況下，要啟動的可用處理程式應用程式清單。 然後，選擇的處理常式會自動播放其相關聯的內容類型。
-   顯示檔案的標準資料夾查看。
-   如果之前使用者選擇的內容類型 **不採取任何動作** ，而且指定的 **一律執行選取的動作**，就不會執行任何動作。

如果內容不符合自動播放的準則，則會將事件傳遞至 Windows 映像取得 (WIA) 。

下列主題討論自動播放的設定和使用。

-   [準備搭配自動播放使用的硬體和軟體](#preparing-hardware-and-software-for-use-with-autoplay)
-   [自動播放如何搜尋媒體](#how-autoplay-searches-media)
-   [定義單一和混合內容類型](#defining-single-and-mixed-content-types)
-   [範例案例](#sample-scenarios)
    -   [使用圖片媒體自動播放存放裝置](#autoplay-for-storage-devices-with-picture-media)
    -   [自動播放音樂檔案播放裝置，以及包含音樂媒體的儲存裝置](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [初次簡報時播放影片播放](#autoplay-for-video-playback-on-first-presentation)
-   [指派預設處理常式應用程式](#assigning-default-handler-applications)
-   [處理包含混合內容類型的媒體](#handling-media-containing-mixed-content-types)
-   [自動播放使用者介面](#autoplay-user-interfaces)
    -   [單一內容類型對話方塊](#single-content-type-dialog-box)
    -   [混合媒體對話方塊](#mixed-media-dialog-box)
    -   [屬性頁面](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a>準備搭配自動播放使用的硬體和軟體

有幾項資訊需要出現在登錄中，才能讓播放程式正常運作。 這些資訊片段會彼此互動並互相參考，以形成完整的自動播放環境。 本檔將每一項資訊的設定以個別獨立程式的形式提供。

如需其他指示，請參閱下列主題。

-   [如何將裝置處理常式指派給裝置](how-to-assign-a-device-handler-to-a-device.md)
-   [如何使用裝置群組來指定裝置的圖示、標籤或裝置處理常式](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [如何使用裝置類別指定裝置的圖示、標籤或裝置處理常式](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [如何防止元件的自動播放](how-to-prevent-autoplay-for-a-component.md)
-   [如何註冊裝置事件的處理常式](how-to-register-a-handler-for-a-device-event.md)
-   [如何在執行中的應用程式中使用自動播放事件](how-to-use-autoplay-events-in-running-applications.md)
-   [如何註冊事件處理常式](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a>自動播放如何搜尋媒體

自動播放會搜尋根目錄下方的媒體四個目錄層級，以找出已知的檔案類型。 它會使用與登錄中的副檔名相關聯的 PerceivedType 值，來判斷檔案類別目錄，不論是影像、音訊檔案或影片檔案。 透過此資訊，自動播放會針對該裝置和檔案類型啟動適當的處理常式。 如需詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。

## <a name="defining-single-and-mixed-content-types"></a>定義單一和混合內容類型

自動播放定義三個主要內容類別別。

-   圖片
-   音樂
-   影片

如果媒體上的所有檔案只屬於這三種類別的其中一種，則會將媒體視為包含單一內容類型。 請注意，這並不表示檔案必須是相同的 *檔* 類型，.jpg、.gif 和 .bmp 都是不同的檔案類型，但 (圖片) 一個內容類型。

如果媒體上有支援的內容類型，但沒有單一內容類型可考慮總計的100%，則會將媒體視為包含混合的內容類型，並據以處理。 如需詳細資訊，請參閱 [處理包含混合內容類型的媒體](#handling-media-containing-mixed-content-types)。

## <a name="sample-scenarios"></a>範例案例

下列案例可讓您對預期的自動播放功能有基本的瞭解。

### <a name="autoplay-for-storage-devices-with-picture-media"></a>使用圖片媒體自動播放存放裝置

1.  使用者會將已經插入媒體的 USB SanDisk CompactFlash reader 裝置，以 .jpg 檔案的形式附加到包含 100% picture 內容類型的媒體。
2.  通知會顯示 **找到新的硬體 SanDisk ImageMate**。
3.  自動播放會啟動適當的映射應用程式。

同樣地，當讀取器已附加到系統時，當使用者將該相同的 CompactFlash 媒體插入讀取器時，media insert 事件也會導致自動播放啟動影像投影片放映應用程式。 使用者可以選擇前往 SanDisk 媒體裝置的 [內容] 頁面，將預設值變更為另一個已註冊的自動播放應用程式，例如掃描器和攝影機的 [播放程式] 或圖片！。

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a>自動播放音樂檔案播放裝置，以及包含音樂媒體的儲存裝置

1.  使用者連接 USB 鑽石 Rio MP3 播放機。
2.  通知會顯示 **找到新的硬體鑽石 RIO MP3 播放機**。
3.  自動播放會使用其註冊的預設處理常式（例如 Windows Media Player）來播放這些檔案。

同樣地，如果使用者插入包含 mp3 檔案的任何媒體 (例如，CompactFlash、SmartMedia、記憶杆或 CD-ROM) 將總支援內容的100% 儲存到儲存裝置，media insert 事件也會導致自動播放使用 Windows Media Player 播放檔案。 使用者可以存取儲存裝置的屬性工作表，並將預設動作變更為另一個已註冊的自動播放應用程式，例如說明或 Real Player。

### <a name="autoplay-for-video-playback-on-first-presentation"></a>初次簡報時播放影片播放

1.  使用者第一次插入1394數位攝影機。
2.  使用者會看到一個簡單的對話方塊，詢問要執行哪個應用程式。 選擇是執行其中一個已註冊的自動播放應用程式，或開啟資料夾以查看檔案。 使用者可以將選取的行為設定為要儲存為稍後數位攝影機熱插即用事件的預設動作。

## <a name="assigning-default-handler-applications"></a>指派預設處理常式應用程式

全新安裝的 Windows 會使用一組已註冊的處理常式應用程式來尋找 [自動播放]。 依預設，在 Windows 安裝期間註冊的應用程式如下所示。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>媒體類型</th>
<th>應用程式</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>圖片</td>
<td><ul>
<li>投影片放映 (預設) </li>
<li>相機和掃描器的 Wizard</li>
<li>列印嚮導</li>
<li>開啟資料夾</li>
</ul></td>
</tr>
<tr class="even">
<td>音樂</td>
<td><ul>
<li>Windows Media Player (預設) </li>
<li>開啟資料夾</li>
</ul></td>
</tr>
<tr class="odd">
<td>影片</td>
<td><ul>
<li>Windows Media Player (預設) </li>
<li>開啟資料夾</li>
</ul></td>
</tr>
</tbody>
</table>



 

如果是不支援的類型，系統會要求使用者在第一次的系統簡介中，為與每個存放裝置相關聯的 [自動播放] 動作指派預設設定。 屆時，系統會提示使用者從提供的已註冊應用程式清單中選擇動作，或顯示列出媒體內容的資料夾檢視。 使用者也可以選擇在每一次偵測到媒體類型時收到提示，而不是將任何特定的應用程式儲存為預設值。

> [!Note]  
> 裝置製造商可以選擇註冊和指派預設應用程式，以搭配其特定產品使用。 在這些情況下，不會顯示為使用者提供選擇的對話方塊。

 

新安裝的應用程式必須在登錄中自行註冊，才能以自動播放的形式提供給處理常式選項。 如需詳細資訊，請參閱 [準備搭配自動播放使用的硬體和軟體](#preparing-hardware-and-software-for-use-with-autoplay)。

使用者一律可以變更任何儲存裝置或內容類型的預設自動播放處理常式。 在 **我的電腦** 的儲存裝置的屬性工作表中，[自動播放] 屬性頁可供變更。

如需使用者提示和屬性頁的範例，請參閱 [自動播放使用者介面](#autoplay-user-interfaces)。

## <a name="handling-media-containing-mixed-content-types"></a>處理包含混合內容類型的媒體

當自動播放顯示混合的內容媒體時，需要使用者輸入才能執行動作。 在此情況下，使用者會看到一個對話方塊，其中包含媒體上存在之內容類型可用的所有適當註冊應用程式篩選清單。 使用者可以選擇其中一個應用程式來自動播放特定的內容類型，而其餘部分則保持不變。 由於混合內容媒體的組合因每個個別光碟而異，因此沒有任何選項可將此選項儲存為預設值。

如需使用者提示的範例，請參閱 [自動播放使用者介面](#autoplay-user-interfaces)。

## <a name="autoplay-user-interfaces"></a>自動播放使用者介面

有三個可能的使用者介面。

-   此對話方塊會提示使用者輸入單一內容類型的動作
-   提示使用者輸入混合內容類型之動作的對話方塊
-   屬性頁

### <a name="single-content-type-dialog-box"></a>單一內容類型對話方塊

當任何尚未指派預設 [自動播放] 動作的支援媒體呈現給系統時，會顯示類似下面的對話方塊。

![[單一內容類型] 對話方塊的螢幕擷取畫面](images/pix.png)

使用者可以執行下列其中一項動作。

-   從已註冊的應用程式清單中選擇動作。
-   以一般資料夾檢視列出媒體上的檔案。
-   不採取任何動作。

使用者也可以按一下 [ **永遠執行選取的動作** ] 方塊，將選擇儲存為此媒體的預設動作。 完成此選擇之後，對話方塊就不會再次顯示。 不過，在 Windows XP Service Pack 1 (SP1) 中，如果可處理特定媒體類型的新應用程式已新增至電腦，則會再次向使用者顯示對話方塊，讓他們有機會選取新的應用程式做為預設的 [自動播放] 動作。 應用程式安裝時，也可以將自己設定為預設選項。

Windows XP SP1 也加入了一項功能，可保留使用者選擇的 [自動播放] 動作（如果沒有按一下 [ **永遠執行選取的動作** ] 方塊）。 如果使用者選擇單一實例的 [自動播放] 動作，則下次顯示該媒體類型的對話方塊時，相同的動作就是預設選項。

若要將應用程式包含在可能的動作清單中，則必須使用 [自動播放] 來註冊該應用程式。 如需詳細資訊，請參閱 [準備搭配自動播放使用的硬體和軟體](#preparing-hardware-and-software-for-use-with-autoplay)。

### <a name="mixed-media-dialog-box"></a>混合媒體對話方塊

當包含支援檔案類型混合的任何媒體呈現給系統時，會顯示下列對話方塊。 這基本上與單一 [內容媒體] 對話方塊相同，但是有兩個重要的差異。 首先，可用的動作選項包含與媒體上所有內容類型相關的應用程式篩選清單。 其次，沒有選擇永久預設動作的選項，因為混合內容媒體的內容類型和百分比太無法預期。

![[混合媒體] 對話方塊的螢幕擷取畫面](images/mix.png)

若要將應用程式包含在可能的動作清單中，則必須使用 [自動播放] 來註冊該應用程式。 如需詳細資訊，請參閱 [準備搭配自動播放使用的硬體和軟體](#preparing-hardware-and-software-for-use-with-autoplay)。

### <a name="property-page"></a>屬性頁面

以下是 DVD/CD-ROM 裝置的 [自動播放] 屬性頁範例。

![屬性頁的螢幕擷取畫面](images/apdlg.png)

每種裝置類型都提供適當的內容類型子集，以供自動播放設定使用。 接著，每個內容類型在選取時，會在清單方塊中提供適當的動作選項清單。 您可以為每個內容類型選擇不同的動作。

 

 



