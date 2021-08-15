---
description: 直接操作會使用 [內容] 和 [連絡人] 來描述 UI 的互動元素。
ms.assetid: 1564F6F2-844F-4392-9EB5-AA46059D514C
title: 區和內容
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a103df916e5880380064250d05806169ff4187e6a8be0b22d2dd72d92343f38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787077"
---
# <a name="viewports-and-content"></a>區和內容

[直接操作](direct-manipulation-portal.md) 會 *使用*[ *內容* ] 和 [ *連絡人* ] 來描述 UI 的互動元素。

- [設定視口](#configuring-a-viewport)
- [對齊點和界限](#snap-points-and-boundaries)
- [貼齊點位移和 RTL 情節](#snap-point-offset-and-rtl-scenarios)
- [行為](#behaviors)
- [座標系統](#coordinate-system)
- [轉換](#transforms)
- [視窗區狀態](#viewport-state)
- [相關主題](#related-topics)

*區* 是視窗內的區域，可接收和處理使用者互動的輸入。 此區代表使用者在指定時間可以看到的內容區域 (也稱為內容剪輯) 。 此區有數個函數：

- 它會管理互動狀態 (例如，當內容已準備好進行操作時、內容正在進行操作時、內容處於慣性動畫) ，以及將輸入對應至輸出轉換時。
- 它包含可移動以回應使用者互動的內容。 這可能是 HTML div 元素 (滾動) 、 (Windows 8 開始畫面) 的平移清單，或選取控制項的快顯功能表。

您可以藉由呼叫 [**CreateViewport**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport)來建立一個視口。 您可以在單一視窗中建立多個區，以產生豐富的 UI 體驗。

*內容* 代表為了回應互動而轉換的元素。 換句話說，內容是隨著使用者移動或 pinches 而移動或調整的內容。 內容有兩種類型：

- *主要內容* 是在回應輸入操作和慣性之視口內的單一內建函式專案。 主要內容會與區在相同時間建立，且無法從區中新增或移除。 您可以使用 (稍後) 討論的貼齊點來自訂主要內容的行為。
- *次要內容* 會相對於主要內容的移動而移動。 次要內容是與區分開建立的，而且可以從視口中新增或移除。 所有次要內容轉換都是根據主要內容的轉換進行計算。 您可以套用特定規則來變更轉換的計算方式，方法是根據專案的預定用途（由其 CLSID 在建立期間識別）。

在此圖表中顯示平移前後的位置，使用了單一連絡人來平移主要內容。 雖然使用者不會直接與 (次要內容) 的移動流覽指標互動，但次要內容會隨著主要內容移動流覽而移動。 這可提供視覺提示給使用者移動流覽的程度。

![顯示平移前後的圖表](images/dm-art-2.png)

## <a name="configuring-a-viewport"></a>設定視口

建立了視口之後。 使用 *互動* 設定來設定其行為。 互動設定會指定支援哪些操作（例如移動流覽）。

*移動* 流覽會將內容的位置變更為水準或垂直軸，或同時變更為使用者的移動。 當您在這兩個軸上設定轉譯時，內容會以任何方向自由地移動。

若要限制內容的動作，請設定 *滑軌*，通常在水準和垂直軸上。 如果使用者的互動主要沿著單一軸， (下圖中的藍色區域表示) ，則平移會變成 *railed* ，而且內容只會沿著 railed 軸移動。 如果使用者已移動流覽，且目前已 railed 並在內容為慣性時執行第二個平移，則會繼續 railed 新的平移。

![顯示 railed 移動區中的內容的圖表](images/dm-art-3.png)

範例：為水準和垂直移動設定的視口。 在第一個框架中，連絡人會關閉。 在第二個情況下，會起始垂直平移，並將連絡人鎖定至垂直滑軌。 最後，一旦 railed 平移，就只會使用對角平移的垂直元件來移動內容。

如果使用者以不在滑軌偵測區域中的方式來回移動 (白色區域) ，則會 *unrailed* 平移，而且內容將會在兩個軸中自由移動。

![顯示在 unrailed pan 中移動內容的圖表](images/dm-art-4.png)

當使用者 pinches 或伸展時，*縮放* 會變更內容的縮放比例。 將內容縮放 (稱為「縮放中心」的點) 是「連絡人」的中心。 如果您已設定水準或垂直對齊，縮放中心會變更以保持對齊。

![顯示已指定對齊之內容縮放的圖表](images/dm-art-5.png)

您可以藉由指定 [解除鎖定中心] 來覆寫此行為，這會設定連絡人中心的縮放中心。

![顯示縮放中心已解除鎖定之內容縮放的圖表](images/dm-art-6.png)

*慣性* 是在觸控) 或鍵盤/滑鼠輸入 (（例如，按一下捲軸或按下方向鍵) ）之後，操作的漸進速度（移動和 (縮放）。 當使用者操作內容時，此操作不會在連絡人被提起之後立即停止。 相反地，內容會以目前的方向和速度繼續進行，速度會逐漸降低。

## <a name="snap-points-and-boundaries"></a>對齊點和界限

當手指在觸控) 或鍵盤/滑鼠動作的結果 (例如方向鍵、page up/down、滑鼠滾輪滾動) 等的情況下，在操作結束之後，就會發生慣性動畫 (。

定義慣性動畫的資訊有兩個部分：

- 動畫的 rest 點–特定轉換元件的最終結束位置。
- 動畫持續時間（曲線、速度）–這些是由 rest 點的型別所決定。

慣性動畫會受到對齊點和界限的影響。 界限會指定內容的最大和最小 rest 點數。 如果內容在慣性期間到達界限，則會套用界限動畫。 在主要內容上定義對齊點，以修改 rest 點並修改慣性動畫曲線本身。

當內容的間距較近時，您會使用 [**SetSnapInterval**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval) 定義貼齊點，或在內容的間距間距時使用 [**SetSnapPoints**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints) 定義貼齊點。 以下是貼齊點的範例：

![圖表顯示內容中設定的貼齊點會如何影響移動](images/dm-snappoint-states-3.png)

在此圖中，有一系列的內容具有一系列的子內容區塊–新聞讀取器類型應用程式中的新聞專案，或在格線視圖中的專案。 其目的是在慣性結束之後，將專案的左邊緣貼齊至視口的左邊緣。

格線類型有兩個群組：

- *選擇性與強制性*：選擇性的貼齊點只會在慣性 rest 點接近對齊點時，才會貼上慣性動畫。 強制的貼齊點一律會將慣性動畫貼齊指定的貼齊點。
- *單一與多個*：多個貼齊點類型可讓內容移動超過許多貼齊點，然後在靠近其自然 rest 點的貼齊點上移至其他貼齊點。 單一的貼齊點類型會選擇下一個最接近的貼齊點，作為慣性動畫的 rest 點。

下圖將示範對齊點類型如何修改慣性動畫的其餘位置。

![顯示慣性和貼齊點如何互動的圖表](images/dm-snappoint-states-1.png)

在此圖中，慣性起點會標示為「開始」，而在沒有貼齊點為 ' End ' 的情況下，則會有自然慣性結束位置。 垂直線會標示不同的貼齊點。 下表說明每種類型的貼齊點將如何影響動畫的結束位置。

| 點類型         | Description                                                                                |
|--------------------|--------------------------------------------------------------------------------------------|
| 強制單一   | 因為貼齊點 P1 是慣性方向的第一個貼齊點，所以已選擇     |
| 強制多重 | 因為貼齊點 P2 最接近慣性方向的結束點，所以已選擇 |
| 選擇性單一    | 因為貼齊點 P1 是慣性期間遇到的第一個貼齊點，所以已選擇      |
| 選用多重  | 因為貼齊點 P2 接近自然結束點，所以已選擇                           |

## <a name="snap-point-offset-and-rtl-scenarios"></a>貼齊點位移和 RTL 情節

![顯示 rtl 貼齊點使用的圖表](images/dm-snappoint-states-2.png)

您可以使用 [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) API 來套用貼齊點位移和座標系統，這會使用指定的位移/座標系統來位移所有的貼齊點或貼齊間隔。

座標系統在 RTL 情節中非常有用，您想要從內容的左邊緣描述反向方向的貼齊點。 在上圖中， [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) 是與 **DIRECTMANIPULATION \_ 運動 \_ TRANSLATEX** 和 **DIRECTMANIPULATION \_ 座標 \_ 鏡像** 旗標搭配使用，此旗標會自動從內容的左邊位移貼齊點，並以由右至左的順序提供： S1 位於0px，S2 是在 50px (等) 。 任何使用 **SetSnapCoordinate** 設定的位移都會自動從內容的左邊緣位移，包括正確的縮放因數。

您幾乎一律會使用 [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) 搭配 *原始* 參數設定，以避免設定內容區域以外的貼齊點。

例如，如果200x200 的視口和內容是1000x200 的，且介面是 RTL，則在第一次顯示區時，此介面的左邊緣會是 x = 800。 使用呼叫 [**SetSnapCoordinate**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate) ， `SetSnapCoordinate(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_COORDINATE_MIRRORED, 1000.0)` 以指定從內容的右邊緣開始，從右至左的順序計算對齊點。

## <a name="behaviors"></a>行為

*行為* 是一個物件，可以附加至一個物件區，以修改 [直接操作](direct-manipulation-portal.md)如何處理其主要或次要內容的輸出轉換。 行為物件可能會影響操作的一或多個層面，例如輸入的處理方式或套用慣性動畫的方式。 例如，autoscroll 行為會藉由在主要內容的一端執行滾動動畫來影響慣性動畫。 跨幻燈片設定行為會影響直接操作輸入處理，以偵測何時執行跨幻燈片動作。

藉由呼叫 [**CreateBehavior**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager2-createbehavior)來建立行為物件，並將其加入至物件區，然後以非同步方式設定其行為。 從區中移除行為會移除其效果。

## <a name="coordinate-system"></a>座標系統

[直接操作](direct-manipulation-portal.md)採用三種主要座標系統：

- 用戶端座標系統-描述用戶端視窗的矩形。 單位是以圖元為單位。
- 區座標系統-描述用戶端中可以處理輸入之區域的矩形。 單位是使用 [**SetViewportRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportrect)) 的應用程式定義 (。
- 內容座標系統-描述主要內容的矩形或大小。 單位是使用 [**SetContentRect**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-setcontentrect)) 的應用程式定義 (。

對於這三個系統而言，座標是相對於其各自的左上原點所定義，而且正向右和向下遞增。 下圖說明這些座標系統。 只有在 [區域] 矩形內的內容區段可以由終端使用者看見或操作。

![顯示內容、用戶端和視口如何協調互動的圖表](images/dm-art-7.png)

## <a name="transforms"></a>轉換

[直接操作](direct-manipulation-portal.md) 會維護數個會對整體顯示輸出造成影響的不同轉換。

- *內容轉換* –以操作或慣性為基礎的 [直接操作](direct-manipulation-portal.md) 所計算的初始轉換。 它會捕捉貼齊點、railing、預設 overpan (操作) 、預設 overbounce (慣性) 和 ZoomToRect 動畫的效果。
- *輸出轉換* -最後的視覺效果或輸出轉換。 它是內容和同步轉換的組合。
- *同步轉換* –在您呼叫 [**SyncContentTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-synccontenttransform)時計算。 它可協助 [直接操作](direct-manipulation-portal.md) 套用應用程式所提供的新內容轉換，同時也能維護現有的輸出轉換。
- *顯示轉換* –應用程式在後置處理過程中套用。 如需詳細資訊，請參閱 [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform) 。

因為輸出轉換的目的是要在螢幕上以視覺化方式呈現介面，所以 [直接操作](direct-manipulation-portal.md) 會在輸出轉換元件上執行必要的舍入，讓文字和其他內容一律在整數圖元界限轉譯/合成。 舍入機制取決於多個因素，包括動作速度以及遠端桌面是否存在。 次要內容的舍入機制符合主要內容，同時考慮兩者之間的動作差異。 [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform)的用戶端不應該相依于輸出轉換的確切舍入機制，因為有各種因素會影響它。

> [!Note]
>
> 這表示內容轉換的元件可能不是整數，而且可能包含子圖元位移。 建議您使用 [直接操作](direct-manipulation-portal.md) 的用戶端，以在使用手動更新模式時，使用 [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform) 來計算要套用至內容的正確視覺效果轉換。 使用內建的組合器來使用自動更新模式時，直接操作會自動代表用戶端套用此轉換。 這項轉換是由直接操作所產生，以確保在撰寫視覺效果輸出時能以視覺化的方式呈現結果。

## <a name="viewport-state"></a>視窗區狀態

處理輸入時，此區會管理互動狀態以及輸入對應至輸出轉換。 藉由呼叫 [**GetStatus**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-getstatus)來檢查視口的互動狀態。

![顯示 directmanipulation 互動狀態的圖表](images/dm-states-diagram.png)

- 建築物-正在建立此區，而且還無法處理輸入。 為了處理輸入，請呼叫 [**IDirectManipulationViewport：： Enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable)。 如果未呼叫 **Enable** ，則此區會進入停用狀態。

    > [!Note]  
    > 這是互動的初始狀態。

- 已啟用-此區已準備好處理輸入。 當連絡人關機時 (會呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)) 並偵測到操作，然後將此視口轉換成正在執行。

- 正在執行-此區目前正在處理輸入和更新內容。 當連絡人被提起時，如果已設定，則會轉換成慣性。

- 慣性–內容正在慣性動畫中移動。 一旦慣性完成，區將會轉換為就緒。 如果已在功能區上設定自動停用，它會從慣性轉換為就緒，然後再轉換為停用。

- 就緒–此區已準備好處理輸入。 當連絡人關機時 (會呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)) 並偵測到操作，然後將此視口轉換成正在執行。

- 已暫止–當此區的輸入已升級為 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) 鏈中的父系時，可能會暫停。 這會在多個資料區中更詳細地討論 [：點擊測試和視口](directmanipulation-multiple-vieports.md)階層。

- 停用-此區將不會處理輸入或進行回呼。 您可以藉由呼叫 [**IDirectManipulationViewport：:D isable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-disable)，從各種狀態中停用視口。 如果已在功能區上設定自動停用，則在處理操作之後，它會自動轉換為停用。 若要重新啟用已停用的區式，請呼叫 [**IDirectManipulationViewport：： enable**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-enable)。

## <a name="related-topics"></a>相關主題

[多個視窗區：點擊測試和視口](directmanipulation-multiple-vieports.md)階層、 [**ActivateConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration)、 [**GetOutputTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationcontent-getoutputtransform)、 [**SyncDisplayTransform**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform)
