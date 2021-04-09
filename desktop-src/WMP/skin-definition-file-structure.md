---
title: 外觀定義檔案結構
description: 外觀定義檔案結構
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- 面板定義檔 Windows Media Player 的外觀
- 外觀、面板定義檔
- 面板的檔案、外觀定義
- 外觀定義檔，結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021715"
---
# <a name="skin-definition-file-structure"></a>外觀定義檔案結構

外觀定義檔必須遵循特定的結構。 您可以從 **主題** 專案開始，建立一個或多個 **view** 元素，然後使用適合您要使用之檢視類型的使用者介面元素，來定義每個 **view** 元素。

## <a name="theme-elements"></a>主題元素

在最上層，您必須以 **主題** 元素啟動面板定義檔，並將其關閉。


```C++
<THEME>
    ...
</THEME>

```



**主題** 元素是面板的根項目。 面板定義檔中只能有一個 **主題** 元素，而且它必須位於最上層。 **主題** 元素有特定和環境屬性，不過大部分的情況下，您不需要使用它們。 如需這些屬性的詳細資訊，請參閱 [外觀程式設計參考](skin-programming-reference.md)。

## <a name="view-elements"></a>VIEW 元素

每個 **主題** 都必須至少有一個 **VIEW** 元素。 **VIEW** 元素會控制您在螢幕上看到的特定影像。 您可能會想要有一個以上的視圖，讓您可以來回切換。 例如，您可能想要有很大的觀點來使用播放清單、觀看視覺效果的中型視圖，以及適合螢幕角落的小視野。

如果您要建立多個視圖，您會想要確定每個視圖都具有唯一的 **識別碼** 屬性值，以用來識別此視圖。 您必須定義 **backgroundImage** 屬性，否則您的視圖將不會有起始影像。 如果您不想要顯示矩形影像，您可能會想要使用 **clippingColor** 屬性來定義不會顯示的面板區域，而且您可能會想要設定 **VIEW** 元素的 **標題列** 屬性。

每一個 **VIEW** 專案也可以有一或 **多個子視圖元素** 。 子 **視圖元素類似** 于 **視圖** ，可用於您想要四處移動、隱藏或顯示的部分面板。 例如，子 **視圖** 元素可用來建立滑出面板的滑動紙匣，以顯示圖形等化器。 子 **視圖專案** 可以與 **視圖** 對齊，並與該 **視圖** 具有其他特殊關聯性。

## <a name="initializing-windows-media-player"></a>正在初始化 Windows Media Player

您可以使用 [ **播放** 程式]、[ **設定**] 和 [ **控制項** ] 元素，設定 Windows Media Player 的特定初始屬性。 例如，您可以將磁片區設定為初始層級，或指定檔案名的預設值。

下列程式碼顯示如何在面板中設定 **URL** 值：


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



如果您想要將 [**設定**] 的 [**自動啟動**] 屬性設定為 False，您可以使用下列程式碼：


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



請注意， **SETTINGS** 元素是在 **PLAYER** 專案內進行嵌套。

您可以使用這些元素，在設計階段指定下列屬性和事件：

**PLAYER 元素屬性**

-   **url**
-   **緩衝處理**
-   **Currentitemchange**
-   **Currentplaylistchange**
-   **錯誤**
-   **Markerhit**
-   **Mediachange**
-   **Mediacollectionchange**
-   **Modechange**
-   **Mpenstatechange**
-   **Mlaylistchange**
-   **Mlaystatechange**
-   **Mositionchange**
-   **Mcriptcommand**
-   **Mtatuschange**

**SETTINGS 元素屬性**

-   **啟動**
-   **平衡**
-   **baseURL**
-   **defaultFrame**
-   **enableErrorDialogs**
-   **invokeURLs**
-   **靜音**
-   **playCount**
-   **率**
-   **體積**

## <a name="controls-element-attributes"></a>CONTROLS 元素屬性

-   **currentMarker**
-   **currentPosition**

## <a name="other-user-interface-elements"></a>其他消費者介面元素

一旦定義您的 **主題** 和 **VIEW** 專案之後，您必須使用特定的使用者介面元素來填入您的 **視圖** 。 您不需要在面板中使用所有可用的專案，只是您需要的專案。

如果使用者可以看到某個元素，則會呼叫控制項。 下列控制項適用于下列的外觀：

-   按鈕
-   滑杆、自訂滑杆和進度列
-   文字方塊
-   影片視窗
-   視覺效果視窗
-   播放清單視窗
-   子視圖視窗

此外，您還可以使用數個元素來進一步定義 Windows Media Player 動作，但它們需要視覺元素，例如按鈕或滑杆：

-   影片設定
-   等化器設定
-   視覺效果設定

## <a name="buttons"></a>按鈕

按鈕是外觀最受歡迎的部分。 您可以使用按鈕來觸發動作，例如播放、停止、結束、最小化，以及切換至不同的視圖。 Windows Media Player 提供具有兩種按鈕元素的外觀建立者： **button** 元素和 **BUTTONGROUP** 元素。 此外，還有數個預先定義的按鈕類型。

-   **BUTTON 元素。** **按鈕** 元素用於個別按鈕。 如果您使用 **button** 元素，您必須為每個按鈕提供影像，並定義您希望按鈕顯示在相對於背景影像的確切位置。 **按鈕** 元素的優點之一，就是您可以動態變更按鈕影像。
-   **BUTTONGROUP 元素。** **BUTTONGROUP** 元素用於按鈕群組。 事實上，您必須將每個 **BUTTONGROUP** 元素與一對 **BUTTONGROUP** 標記括住。 使用按鈕群組比使用個別按鈕更簡單，因為您不需要為每個按鈕指定確切的位置。 相反地，您會提供個別的影像地圖，以定義當滑鼠停留在背景上或按一下某個區域時將會發生的動作。 使用影像地圖很容易，因為您可以將所建立的圖案帶到您的背景，並將其複製到圖形編輯程式中的地圖圖層。 使用您的圖形編輯程式比起嘗試明確定義應在背景上放置個別按鈕的位置更快且更精確。
-   **預先定義的按鈕。** 有幾個預先定義的按鈕。 例如，您可以使用 [PLAYELEMENT] 按鈕來播放數位媒體檔案，以及使用 STOPELEMENT 來停止播放。 請參閱面板程式設計參考中的 [BUTTONGROUP](buttongroup-element.md) 元素和 [按鈕](button-element.md) 專案。 [IMAGEBUTTON](imagebutton.md)可以用來顯示可變更以回應特定事件的影像。

## <a name="sliders"></a>滑桿

滑杆適用于使用隨時間變化的資訊。 例如，您可以使用滑杆來指出已針對特定媒體檔案播放的音樂數量。 滑杆可以是水準或垂直、線性或圓形，或是您可以想像的任何圖形。 滑杆分為三種：滑杆、進度列和自訂滑杆。

-   **滑 塊。** 您可以使用 **滑杆** 元素進行音量控制項，或讓使用者移至媒體內容的不同部分。
-   **進度列。** 進度列類似滑杆。 進度列的設計目的是要以圖形方式顯示已完成之特定進程的百分比，而不是使用者會想要與之互動的進程。 例如，您可能想要使用進度列來指出緩衝進度。
-   **自訂滑杆。** 提供自訂滑杆功能，因此您可以建立旋鈕之類的控制項，或進行不尋常的控制機制。 例如，如果您想要建立在您的面板周圍換行的音量控制項，可以使用自訂滑杆來進行。 若要設定自訂滑杆，您必須建立包含灰階影像的影像地圖，以定義滑杆上值的位置。 這與支援圖層的圖形編輯程式相當簡單。

## <a name="text"></a>Text

您可以使用 **文字** 專案在面板上顯示文字，例如歌曲標題。

## <a name="video"></a>影片

您可以在面板中顯示影片。 **影片** 元素可讓您設定影片視窗的大小和位置。

您也可以允許使用者使用 **VIDEOSETTINGS** 元素來變更影片設定。 例如，您可以建立控制項來調整影片的亮度。

如果您未提供影片元素，且內容包含影片，Windows Media Player 將會回到 [完整] 模式，且不會顯示您的面板。

## <a name="equalizer-settings"></a>等化器設定

您可以使用 **EQUALIZERSETTINGS** 元素來設定特定音訊頻率群組的篩選。 您可以提高低音、調整高音，以及設定音效以符合您的耳或客廳。

## <a name="visualizations"></a>視覺效果

您可以在面板中顯示視覺效果。 視覺效果是一段時間的視覺效果，會隨著音訊透過 Windows Media Player 播放。 **效果** 元素會決定視覺效果的播放位置、視窗的大小，以及要播放的視覺效果。

## <a name="playlists"></a>播放清單

您可以使用 **播放清單** 元素，讓使用者從特定的播放清單中選取專案。

## <a name="subviews"></a>子檢視

您可以使用 [子 **視圖** ] 元素來顯示介面控制項的次要集合，例如播放清單或影片控制項。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**面板檔案**](skin-files.md)
</dt> </dl>

 

 




