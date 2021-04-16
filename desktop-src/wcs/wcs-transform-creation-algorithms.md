---
title: WCS 轉換建立演算法
description: WCS 轉換建立演算法
ms.assetid: 526bbbfc-fb60-415d-b4f0-6a44a5d11a55
keywords:
- Windows Color System (WCS) 、轉換建立
- WCS (Windows 色彩系統) ，轉換建立
- 影像色彩管理、轉換建立
- 色彩管理，轉換建立
- 色彩，轉換建立
- 轉換建立
- WCS 轉換建立
- 演算法，轉換建立
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418596c0e57571f3e504727d4606921d36ff9461
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104571500"
---
# <a name="wcs-transform-creation-algorithms"></a>WCS 轉換建立演算法

[建立轉換](#creation-of-transforms)

 

[順序轉換執行](#sequential-transform-execution)

 

[建立優化的轉換](#creation-of-optimized-transforms)

 

[ICCProfileFromWCSProfile](#iccprofilefromwcsprofile)

 

[黑色保留和黑色世代](#black-preservation-and-black-generation)

 

[檢查 Gamut](#checkgamut)

## <a name="creation-of-transforms"></a>建立轉換

若要適當地說明色彩轉換的運作方式，請透過 ICM 2.0 和 CTE 的內部說明完整的處理路徑。 ICM 2.0 [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) 函式會建立應用程式可用來執行色彩管理的色彩轉換。 此函式會從 [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) 和意圖輸入建立色彩內容。 這些意圖會對應至基準 ICC gamut 對應演算法相互關聯。 然後，此函式會呼叫 ICM 2.0 函式 [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/) ，以進行一致的色彩處理。 **CreateColorTransform** 函數通常會將資料複製到內部優化的轉換結構。

ICM 2.0 CreateMultiProfileTransform 函式會接受設定檔陣列和意圖陣列，或單一裝置連結設定檔，並建立應用程式可用來執行色彩對應的色彩轉換。 它會處理這些輸入設定檔和意圖，以建立裝置模型、色彩外觀模型、gamut 界限描述和範圍對應模型。 做法如下：

-   裝置模型會直接從 DM 設定檔初始化。 在 [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)的呼叫中，會為每個設定檔建立一個裝置模型。
-   色彩外觀模型會直接從 CAM 設定檔初始化。 [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)呼叫中的每個設定檔都有一個 CAM 設定檔。 不過，您可以為一個以上的設定檔指定相同的 CAM 設定檔。
-   範圍界限描述是從裝置模型物件和凸輪物件初始化。 在 [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)的呼叫中，每個設定檔都有一個 gamut 界限描述。
-   Gamut 對應模型會從兩個範圍界限和意圖初始化。 您必須在從呼叫 [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)所建立的每一對裝置模型之間建立 gamut 對應模型。 請注意，這表示您使用的 gamut 地圖模型比裝置模型少一個。 由於意圖的數目符合裝置型號的數目，因此還有一個意圖比所需的還要多。 會略過清單中的第一個意圖。 您將逐步解說裝置模型和意圖的清單，並建立 gamut 對應模型。 挑選第一個和第二個裝置模型和第二個意圖，然後初始化第一個 gamut 對應模型。 挑選第二個和第三個裝置模型和第三個意圖，然後初始化第二個 gamut 對應模型。 以這種方式繼續進行，直到您已建立所有範圍對應模型為止。

當設定檔已正確處理，而且所有中繼物件都已建立並初始化之後，您就可以使用下列呼叫來建立引用轉換。 *PDestCAM* 和 *PDestDM* 是與 [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)的呼叫中最後一個設定檔相關聯的。


```C++
HRESULT CreateCITEColorTransform(
 __inout     IDeviceModel          *pSourceDM,
 __inout     IColorAppearanceModel *pSourceCAM,
 __in        GamutMapArray         *pGamutMapArray,
 __inout     IColorAppearanceModel *pDestCAM,
 __inout     IDeviceModel          *pDestDM,
             EColorTransformMode    eTransformMode,
 __deref_out IColorTransform      **ppCTS
 );
```



## <a name="support-for-plug-ins"></a>支援外掛程式

設定轉換清單的其中一個問題是驗證是否有必要的外掛程式可供使用。 下列模型參數提供此原則來控制這項行為。 此轉換清單的管理是內部優化轉換結構中的方法，但每個模型方法會提供其本身及其本身參數值集的指標。

此模式必須是下列其中一項。

-   TfmRobust：如果測量設定檔指定慣用外掛程式，且外掛程式無法使用，則新的 CTE 系統將會使用基準外掛程式。 如果沒有可用的外掛程式，轉換將會報告錯誤。
-   TfmStrict：如果 ColorCoNtext 指定慣用的外掛程式，就必須可以使用外掛程式。 如果找不到任何慣用外掛程式，則會使用基準外掛程式。 如果沒有可用的外掛程式，轉換將會報告錯誤。
-   TfmBaseline：只有基準外掛程式可以在 AddMeasurementStep 中使用。 如果 ColorCoNtext 指定慣用外掛程式，將會忽略外掛程式。 如果無法使用基準外掛程式，轉換將會報告錯誤。

## <a name="transform-execution"></a>轉換執行

ICM 2.0 API [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) 函式會將色彩的陣列從來源 [色彩空間](c.md) 轉譯為目的色彩空間，如色彩轉換所定義。 此函式會在內部檢查快取色彩的陣列，以便立即符合常用的轉換色彩。 這種轉換支援每個通道位元組陣列8位，每個通道的 float 陣列都有32位。 所有其他格式將會在傳遞至新的 CTE 之前轉換。

ICM 2.0 API [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) 函式會轉譯具有所定義格式之點陣圖的色彩，以產生所要求格式的另一個點陣圖。 此函式會在內部檢查快取色彩的陣列，以便立即符合常用的轉換色彩。 為了避免太多程式碼路徑、支援和測試複雜度，轉換和插補引擎實際上只支援有限數目的點陣圖格式。 此函式必須將非原生傳入和傳出點陣圖格式轉譯成原生支援的格式，才能進行處理。 此轉換只支援每個通道的8位點陣圖，以及每個通道的 float 點陣圖32位。 所有其他格式將會在傳遞至新的 CTE 之前轉換。

 

### <a name="sequential-transform-execution"></a>順序轉換執行

如果 \_ 呼叫 ICM 函數 [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw)或 **CreateMultiProfileTransform** 時，dwFlags 參數已設定順序轉換位，則會循序執行轉換步驟。 這表示程式碼會依 **CreateColorTransform** 或 **CreateMultiProfileTransform** 呼叫所指定，分別逐步執行每個裝置模型、色彩外觀模型，以及 gamut 對應模型。 這可能有助於偵測外掛程式模組，但速度會比透過優化轉換執行慢很多。 因此，不建議在生產環境軟體中以連續模式執行。 此外，在連續模式和優化模式中取得的結果可能會有些微差異。 這是因為函數串連在一起時所引進的變化。

### <a name="creation-of-optimized-transforms"></a>建立優化的轉換

優化的轉換是一種多維度的查閱資料表。 資料表可以透過將輸入色彩套用至轉換的多維度插補引擎（例如 tetrahedral 插補）來處理。 下一節將說明如何建立優化的查閱資料表。 後面的區段描述如何在優化的查閱資料表中插入。

## <a name="sparse-lookup-tables"></a>稀疏查閱資料表

傳統印表機具有 CMYK 墨水。 若要延伸範圍，其中一個方法是將新的墨水加入系統中。 通常會加入的墨水是 CMYK 油墨難以重現的色彩。 常見的選項為橙色、綠色、紅色、藍色等等。若要增加「明顯的解析度」，可使用具有不同色調的油墨，例如淺青、淺洋紅色等等。 實際上，印表機裝置有四個以上的通道。

雖然印表機是輸出裝置，但它們也會執行從裝置空間到另一個色彩空間的色彩轉換。 在 CMYK 印表機的情況下，這會是從 CMYK 到 XYZ 的轉換，或印表機的「轉寄模型」。 藉由結合轉寄模型與其他轉換，您可以在另一部裝置上模擬 CMYK 列印。 例如，印表機 CMYK 到監視器 RGB 可能會有一個可在監視器上模擬該 CMYK 印表機列印的校對機制。 同樣地，也適用于 wi-fi 印表機。 CMYKOG 至 RGB 轉換可讓您在監視器上進行 CMYKOG 印表機的校對。

執行這類色彩轉換的傳統方法是使用統一的 LUT。 例如，在 CMYKOG 印表機的 ICC 設定檔中，ICC 規格會要求 A2B1 標記，此標記會在轉寄模型的 CMYKOG 裝置空間中儲存統一的 LUT，以從 CMYKOG 至 ICC 設定檔連線空間， (CIELAB 或 CIEXYZ) 。 ICC 裝置連結設定檔可讓您直接從 CMYKOG 裝置空間轉換成任何色彩空間，包括裝置空間，也就是在 CMYKOG 空間中一致取樣的 LUT 形式。 因為 LUT 會產生很大的，所以不會對256層級進行取樣， (位深度 8) ，但在單色裝置 (1 個通道) 時除外。 相反地，會使用使用較低位深度的取樣;有些典型選項是 9 (位深度 3) 、17 (位深度 4) 、33 (位深度 5) 。 如果每個通道中的層級數目小於256，則 LUT 會搭配插補演算法使用，以在層級介於兩個取樣層級之間產生結果。

雖然統一的 LUT 在概念上很容易執行，而且統一 LUT 上的插補通常是有效率的，但 LUT 的大小會隨著輸入維度以指數方式增加。 事實上，如果 *d* 是在統一 LUT 中使用的步驟數目，而 *n* 是來源色彩空間中的通道數目，則 LUT 中的節點數目會 ![ 顯示 LUT 中節點數目的變數 ](images/transformcreation-image002.gif) 。 很明顯地，節點數目很快就需要在記憶體中儲存太多儲存體，即使是頂尖的運算系統也難以處理需求。 若為具有六個或八個通道的裝置，則裝置設定檔的 ICC 執行需要使用 LUT 中的幾個步驟，有時甚至是 A2B1 資料表中的五個步驟，以將設定檔保留為 mb （而非 gb）。 很明顯地，使用較少的步驟會增加插補誤差，因為現在有較少的範例。 由於 LUT 必須是一致的，因此即使在裝置值的小型變更可能造成顯著色彩差異的空間區域中，整個色彩空間的精確度也會降低。

在四個以上 colorants 的裝置中，整個裝置空間的特定 subspaces 比其他空間更重要。 例如，在 CMYKOG 空間中，不常使用青色和綠色油墨，因為它們的色調大多互相重迭。 同樣地，黃色和橙色的油墨大多互相重迭。 您可以在整個色彩空間中，以整體品質的整體效能降低來查看步驟數的整體降低程度，這是您可以為未必筆跡組合提供的功能，但不適合可能或重要的組合。

雖然一致取樣的 LUT 是簡單且有效率的插補，但它會在維度增加時產生龐大的記憶體需求。 實際上，雖然裝置可能會有六個或八個通道，但很少會同時使用它們。 在大部分的情況下，[色彩轉換] 的輸入色彩只有一些「作用中」的 colorants，因此位於較低的維度色彩空間中。 這也表示可以更有效率地在較低的維度空間中完成插補，因為當維度較低時，插補會更快。

因此，其方法是將整個裝置空間分層依據至各種維度的 subspaces。 此外，由於較低的維度 (結合三或四個 colorants) 更重要的是，藉由 stratifying 空間，您也可以套用不同的取樣率;也就是不同的步驟數，也就是各項：針對較低的維度增加取樣率，將它們縮減為較高的維度。

為了修正標記法， *n* 是您想要取樣之色彩轉換來源色彩空間中的通道數目。 您也可以將 *n* 參考為輸入維度，並 ![ 顯示 n 大於或等於5。](images/transformcreation-image004.gif) 除非另有指定，否則為。

基本組建區塊是各種輸入 *維度* 和大小的 LUTs，而不是一個具有輸入維度 *n* 的統一 LUT。 為了更加精確，*LUT* 是對單位 cube 施加的矩形 >lattice;也就是說，所有裝置座標都會正規化至範圍 \[ 0、1 \]) 。 如果是 lut 的輸入維度 (請注意，它不一定等於 *n*，不過會 ![ 顯示 V 小於或等於 n。](images/transformcreation-image006.gif) 是必要的) ，它是由ν一維的取樣方格所組成：

Samp *i*： ![ 顯示一維取樣方格。](images/transformcreation-image008.gif)

其中所有 *x <sub>j</sub>s* 都必須在範圍 \[ 0 （1）中 \] ， ![ 顯示 (我) 的上標 d。](images/transformcreation-image010.gif) 這是 *我* 第一次通道取樣的步驟數，其必須至少為1，並 ![ 顯示 X (注標) d (我) 的 spuperscript。](images/transformcreation-image012.gif) 必須是1。 另一方面，會 ![ 顯示上標 X (注標 1) 。](images/transformcreation-image014.gif) 不需要是0。

只會定義下列兩個特殊的 LUT 案例。

*封閉式 LUT*：這是一個 LUT，其中包含每個 Samp *<sub>i</sub>* 的額外需求， ![ 顯示上標 X (注標 1) 等於0。](images/transformcreation-image016.gif) ，並 ![ 顯示 (i) 大於或等於2的上標 d。](images/transformcreation-image018.gif) . 統一封閉的 LUT 是一種封閉的 LUT，其 ![ 顯示的是上標 d (我) 。](images/transformcreation-image010.gif) 針對每個通道，而節點會在0和1之間保持一致。

*開啟 LUT*：這是一個 LUT，其中包含每個 Samp *i* 的額外需求， ![ 顯示上標 X (注標 1) 大於0。](images/transformcreation-image020.gif) . 好的，它可以 ![ 顯示上標 d (我) 等於1。](images/transformcreation-image022.gif) .

其目標是要將單元 cube \[ 0、1 \] *n* 分層依據至封閉式 LUTs 和 open LUTs 的集合，讓整個集合都涵蓋單元 cube。 概念上，您可以根據維度的維度來整理這些「LUT 分層」，以便在最上層：

![顯示依據維度來組織 L U T 階層式最上層。](images/transformcreation-image024.png)

其中 ![ 顯示 sigma 注標 k。](images/transformcreation-image026.gif) 這是「*k* 維度的分層集合」。 請注意，分層維度的開頭是3，而不是 0;也就是說，由於三 colorant 組合的插補可以處理，而不需要太多記憶體需求。

## <a name="description-of-the-lut-strata"></a>LUT 階層式描述

在此執行中：

1. ![顯示 sigma 注標3。](images/transformcreation-image028.gif) 是由具有三個輸入的封閉式 LUTs 所組成，這是從 *n* colorants 選擇的三個 colorants 的每個可能組合所組成。

2. ![顯示 sigma 注標4。](images/transformcreation-image030.gif) 包含組合 CMYK (或前四個 colorants) 的一個封閉 LUT，以及 ![顯示 (n 超過 4) 減1。](images/transformcreation-image032.png) 針對所有其他四 colorant 組合開啟 LUTs。 藉由 singling CMYK 組合，您就可以確認它是一項重要的組合。

3. 若為， ![ 則顯示 k 等於5、...、n。](images/transformcreation-image034.gif) ， ![ 顯示 sigma 注標 k。](images/transformcreation-image026.gif) 包含 ![ (n 超過 k) 的顯示。](images/transformcreation-image037.gif) 開啟 LUTs，每個可能的組合，從 *n* 個 colorants 的總計選擇 *k* colorants。

它仍會指定 LUTs 的大小。 Open 和 closed LUTs 之間的主要差異在於，開啟的 LUTs 不會重迭，而封閉的 LUTs 可能會在界限面重迭。 在開啟的 LUT 中，一維取樣不包含0，基本上表示開啟的 LUT 遺失邊界臉部的一半，因此名稱為 "open"。 如果兩個 LUTs 不重迭，您可以在每個通道中使用不同數目的步驟或節點位置。 如果兩個 LUTs 重迭，就不會發生這種情況。 在這種情況下，如果步驟數目或節點位置不同，則在兩個 LUTs 的交集處，將會根據在插補中使用的 LUT 來接收不同的插補值。 解決此問題的一個簡單解決方案，是在兩個 LUTs 重迭時，使用相同數目的步驟進行統一取樣。 換句話說：

所有封閉的 LUTs (此實) 中的所有三 colorant LUTs 和 CMYK LUT 都必須一致，且具有相同數目的步驟（以 *d* 表示）。

您可以使用下列兩種演算法來判斷已關閉 LUTs 的步驟 *d* 數目，以及開啟 LUTs 的步驟數目。

## <a name="algorithm-1"></a>演算法 \# 1

此演算法不需要外部輸入。

所有關閉的 LUTs 都會與 *d* 個步驟一致。

維度 *k* 的所有開啟 LUTs 都會有相同數目的步驟 ![ 顯示 d (k) 。](images/transformcreation-image039.gif) 在每個輸入通道中，節點的間距也相同;也就是說，每個 ![ 節目都等於1，2，...，k。](images/transformcreation-image041.gif) .

Samp *i*： ![ 顯示 Samp i 演算法。](images/transformcreation-image043.png)

最後，在下表1中指定 *d* 和 *d* (*k* ) 。 三種模式「證明」、「正常」和「最佳」是 ICM 2.0 品質設定。 在這個執行中，證明模式具有最小的記憶體使用量，而最佳模式的記憶體使用量最大。

若要執行此演算法，您必須呼叫下列演算法 \# 2。 使用者可以使用資料表做為指南，來指定自己的取樣位置。

## <a name="algorithm-2"></a>演算法 \# 2

此演算法需要以「重要」取樣位置清單形式的外部輸入，但它更適合調整，而且可能會節省記憶體空間。

必要的輸入是使用者提供的裝置值陣列。 這些裝置值會指出裝置色彩空間的哪個區域很重要;亦即，應更多取樣的區域。

所有關閉的 LUTs 都會與 *d* 個步驟一致，如演算法1中所述 \# 。 [表 1] 提供 *d* 的值。

*() 的統一封閉 LUT*



|         | 證明模式 | 標準模式 | 最佳模式 |
|---------|------------|-------------|-----------|
| ***d*** | 9          | 17          | 33        |



 

*(b) 開啟 LUT*



| 輸入維度 | 證明模式 | 標準模式 | 最佳模式 |
|-----------------|------------|-------------|-----------|
| 4               | 5          | 7           | 9         |
| 5               | 2          | 3           | 3         |
| 6               | 2          | 3           | 3         |
| 7               | 2          | 2           | 2         |
| 8或更多       | 2          | 2           | 2         |



 

**表1：** 演算法中使用的 LUT 大小

每個開啟的 LUT 在每個輸入通道中可能會有不同數目的步驟，而取樣位置不需要相同的間距。 針對指定的 open LUT 層次，有一個相關聯的 colorant 組合，例如， ![ 顯示 c 注標1、...、c 注標 k。](images/transformcreation-image045.gif) ，其中 ![ 顯示 C 注標 i。](images/transformcreation-image047.gif) s 是1到 *n* 之間的相異整數。 它們是對應至此分層中「作用中」 colorants 的通道索引。

步驟1：篩選出未包含在此分層中之裝置值的輸入陣列。 裝置值 ![ 顯示 x 注標1、x 注標2、...、x 注標 n。](images/transformcreation-image049.gif) 只有在 ![ 顯示通道的一組值時，才會包含在分層中。](images/transformcreation-image051.gif) 和所有其他通道都是0。 如果篩選的集合有 *N* 個專案，請讓

![顯示篩選的集合有 N 個專案時所要使用的方程式。](images/transformcreation-image053.png)

針對每個 ![顯示我等於1，2，...，k。](images/transformcreation-image041.gif) ，重複執行下列步驟2-5：

步驟2：如果 ![ 顯示 d 注標暫時 (k) 等於1。](images/transformcreation-image055.gif) ，Samp *i* 只有1個點，其必須為1.0。 *繼續下一* 步。 否則，請繼續進行步驟3。

步驟3：在中以遞增順序排序篩選的範例 ![顯示 C 注標 i。](images/transformcreation-image047.gif) 通道。

步驟4：使用節點定義「暫時性」取樣方格

![顯示用來定義「暫時」取樣方格的節點。](images/transformcreation-image057.png)

其中 ![顯示 j 等於1、2、...、d 注標暫時 (k) 。](images/transformcreation-image059.gif) .

步驟5： Regularize 暫時性方格，以確定它符合嚴格的單一性，而且其結尾為1.0。 因為陣列已經過排序，所以暫時性方格中的節點已經單純 nondecreasing。 不過，相鄰節點可能會完全相同。 如有必要，您可以移除相同的節點來修正此問題。 最後，在此程式之後，如果結束點小於1.0，請將它取代為1.0。

請注意，步驟5是 LUT 分層在每個通道中的步驟數目可能不同的原因。 正規化之後，通道中的步驟數目可能會小於 ![顯示 d 注標暫時 (k) 。](images/transformcreation-image061.gif) .

## <a name="interpolation"></a>插 值

您可以藉由 open LUT 分層和 closed LUT 分層來建立 unit cube 的分層。 若要使用這個「稀疏 LUT 結構」執行插補，請遵循下列步驟。 假設指定的輸入裝置值 ![顯示 (X 注標1，X 注標2，...，X 注標 n) 。](images/transformcreation-image049.gif) .

步驟1：決定「作用中」通道的數目。 這是非零的通道數目。 這會決定要搜尋包含層次的分層維度 *k* 。 更精確地說，如果使用中通道的數目 ![ 顯示小於或等於3，分層維度就會是3。](images/transformcreation-image063.gif) 否則，分層維度與使用中通道的數目相同。

步驟2：內部 ![顯示 sigma 注標 k。](images/transformcreation-image026.gif) 搜尋包含的層次。 如果對應至層次的所有通道都有非零值，而且所有其他通道都是零，則裝置值會包含在開放式層次中。 如果層次未表示的每個通道都是零，則裝置值會包含在封閉的層次中。 如果找不到包含的層次，則會發生錯誤狀況。 取消和報告失敗。 如果找到包含的層次，請繼續進行下一個步驟。

步驟3：如果包含的層次已關閉，則任何已知的插補演算法都可以完成層次內的插補。 在此執行中，演算法的選擇是 tetrahedral 插補。 如果包含的層次是開啟的，且裝置值嚴格位於層次內，也就是

![顯示 X 注標 i 大於或等於 ... ](images/transformcreation-image065.gif)*第一個通道中的* 第一個節點

如果 *我* 是層次的通道索引，則標準插補演算法（例如 tetrahedral 插補）可以運作。

如果 ![ 某些 i 的第 i 個頻道顯示 [X 注 i 小於 ... ](images/transformcreation-image067.gif) ] 第一個節點，則裝置值會落在層次與較低維度 subspaces 之間的「間距 」。 這項 MOI 與每個 se 的插補演算法無關，因此任何插補演算法都可以用來在此「間距」內插補，雖然慣用的演算法是下列 transfinite 插補。

[圖 1] 的兩個部分說明插補模組的架構。

![此圖顯示插補模組架構的第一部分。](images/transformcreation-image068.png)

![顯示插補模組架構第二部分的圖表。](images/transformcreation-image070.png)

**圖1：** Intepolation 模組架構

如先前所述，此演算法能夠在包含 colorants 重要組合的裝置空間區域中達到相當密集的取樣，同時將所需的 LUTs 大小總計降至最低。 下表顯示使用演算法 \# 1 和一般模式) 和對應的統一 LUT 實 (，進行稀疏 LUT 實所需的節點數目比較。



| **輸入通道的數目** | **稀疏 LUT** | **統一 LUT** |
|------------------------------|----------------|-----------------|
| 5                            | 142498         | 1419857         |
| 6                            | 217582         | 24137567        |
| 7                            | 347444         | 410338673       |
| 8                            | 559618         | 6975757441      |



 

## <a name="interpolation-within-a-unit-cube"></a>單位 cube 內的插補

矩形方格的基本步驟是在封閉儲存格內的插補。 針對輸入點，您可以輕鬆地判斷封閉資料格。 在矩形方格中，會指定每個頂點的輸出值 (角落點) 的封閉儲存格。 它們也是 interpolant 必須滿足的唯一 (BCs) 的界限條件： interpolant 必須通過所有這些點。 請注意，這些界限條件是在「離散」點上，在此案例中是資料格的2n 角落點，其中 n 是色彩空間的維度。

在繼續進行之前，先將界限條件的概念正規化會很有用。 針對封入資料格界限界限的任何子集 (在 n 維度) 的單位 cube，S 的界限條件是函數 BC： S → Rm 的規格，其中 m 是輸出維度。 換句話說，interpolant，其可能表示 Interp： \[ 0，1 \] n → Rm，必須滿足下列條件： Interp (x) = BC (x) 適用于所有 x。

在單元 cube 的插補的標準案例中，S 是 cube 的2n 頂點的離散點集合。

您現在可以將界限條件一般化，以解決稍早所述的問題，並在單元 cube 內提供新的插補演算法。 界限條件可以強加于 cube 的整個界限面，而不只允許離散界限點。 確切的假設如下：

 () point vn = (1，1,..., 1) 是特殊的，而且只允許離散界限條件。 換句話說，沒有任何連續界限條件可以強加于 n 界限，也就是 xi = 1 (i = 1,..., n) 。

針對其餘 n 個界限的每個)  (b (i = 1,..., n) ，界限條件可以強加于整個臉部，以及如果兩個臉部交集，則臉部上的界限條件應該同意交集。

 (c) 具有界限條件之臉部內未包含的任何頂點都會有個別的 (離散) 界限條件。

您可以將離散界限條件稱為有限資料，並將連續界限條件視為 transfinite 資料，以討論有限和 transfinite 資料的插補。

首先，請參閱標準 tetrahedral 插補 (（例如 Sakamoto 的) 專利中所使用的），這可協助您針對此問題的特殊形式來設定標記法。 已知單位 cube \[ 0，1 \] n 可以細分為 n！ tetrahedra，以 n 符號上的排列集合參數化。 更具體來說，每個這類四面體是由到差異所定義

![顯示 tetrahedrons inequalites 的公式。](images/transformcreation-image073.gif)

其中σ： {1，2,.., n} → {1，2,..., n} 是 "符號" 1，2，...，n，也就是一組 n 符號的 bijective 對應。 例如，如果 n = 3 和σ = (3，2，1) ，表示σ (1) = 3，σ (2) = 2，σ (3) = 1，則對應的四面體是由 z ≥ y ≥ x 定義，其中的一般標記法 x、y、z 用於 x1、x2、x3。 請注意，這些 tetrahedrons 不會彼此相交。 基於插補的目的，在兩個不同 tetrahedrons 的共通點上，會有相同的插補值（不論在插補中使用哪一個四面體）。 同樣地，在有限點上插入的標準案例中，針對給定的輸入點 (x1、...、xn) ，先判斷它所在的四面體（或同等的對應排列σ），然後將 tetrahedral interpolant 定義為

![顯示定義 tetrahedral interpolant 的方程式。](images/transformcreation-image075.png)

其中 ![顯示標準基礎向量的方程式。](images/transformcreation-image077.png) 針對 i = 1、...、n 和 e1，...，en 是標準的基礎向量。 在繼續進行一般化之前，請注意 v0、v1、...、vn 是四面體的頂點，而 ![顯示 barycentric 座標。](images/transformcreation-image079.png) 是「barycentric 座標」。

對於在邊界臉部上的 BCs 的一般情況，您可以使用 barycentric 投影的概念。 如同之前，針對指定的輸入點 (x1、...、xn) ，請先判斷它所在的四面體，或等同于對應的排列σ。 然後執行一系列的 barycentric 投影，如下所示。 第一個投射 ![顯示 BProj 的注標 1 (x) 。](images/transformcreation-image081.gif) 將點傳送至平面 ![顯示 X 注標差異 (1) 等於0。](images/transformcreation-image083.gif) 除非 ![顯示 X 等於 V 注標 n。](images/transformcreation-image085.gif) 在這種情況下，它不會變更。 地圖 BProj 的精確定義定義如下：

![顯示地圖 BProj 精確定義的方程式。](images/transformcreation-image087.png)

取代為 ![顯示 P 注標 k 的方程式。](images/transformcreation-image089.png) 和 k = 1、2、...、n。

在案例中 ![顯示 X 等於 V 注標 n。](images/transformcreation-image085.gif) ，您可以停止，因為 BC 是在 vn 中定義的，並假設 () 。 在案例中 ![顯示 X 不等於 V 注標 n。](images/transformcreation-image091.gif) ，顯然 ![顯示 BProj 的注標 1 (X) 。](images/transformcreation-image081.gif) 具有σ (1) 第一個元件的 annihilated。 換句話說，它是在其中一個界限面上。 可能是在定義 BC 的臉部上，您可以停止，或執行另一個 barycentric 投影 ![顯示 BProj 的注標 2 (X ' ) 。](images/transformcreation-image093.gif) 其中 ![顯示 X 等於 BProj 的注標 1 (X) 。](images/transformcreation-image095.gif) . 如果 ![顯示 X ' ' = Bproj 下標 1 (X ' ) 。](images/transformcreation-image097.gif) 在定義 BC 的臉部上，您可以停止;否則，請執行另一個投射 ![顯示 BProj 的注標 3 (X ' ' ) 。](images/transformcreation-image099.gif) . 因為每個投射都 annihilates 一個元件，所以有效的維度會減少，因此您知道進程最後必須停止。 在最糟的情況下，您會對維度0（也就是 cube 上的頂點，根據假設 (c) ）執行 n 預測，您知道 BC 將會定義在上。

假設已執行 K 個預測，

![顯示假設已執行 K 投射時要使用的方程式。](images/transformcreation-image101.png)

x (0) = x、輸入點和 BC 定義于 x (k) 。 然後藉由定義一連串的輸出向量來回溯投影：

![顯示一連串輸出向量的方程式。](images/transformcreation-image103.png)

其中 ![顯示 Y 上標 (K) 的方程式。](images/transformcreation-image105.gif) ，最後取得答案

![顯示 Interp (x) 等於 y 上標 (0) 。](images/transformcreation-image107.gif)

## <a name="worked-example"></a>作用中範例

![此圖顯示使用單元 cube 的插補範例。](images/transformcreation-image108.png)

**圖2：** 作用中範例

請考慮 [圖 2] 中所描述的情況，其中 n = 3、m = 1，而且您有下列的 BCs：

在頂點上 () 四個離散的 BCs

 (0、0、1) ：β001

 (0，1，1) ：β011

 (1、0、1) ：β101

 (1，1，1) ：β111

 (b) 在臉部 x3 = 0 上的持續 BC = 0： F (x1、x2) 

計算 \# 1：輸入點 x = (0.8、0.5、0.2) 。 封閉的四面體與排列 &lt; 1、2、3相關聯 &gt; 。

第1個投射： ![顯示第一個投射的方程式。](images/transformcreation-image110.png)

這已在臉部 x3 = 0 上，因此您可以停止。 回溯替代，然後提供

![顯示第一個投射的答案。](images/transformcreation-image112.png) 這就是答案。

計算 \# 2：輸入點 x = (0.2、0.5、0.8) 。 封閉的四面體與排列 &lt; 3、2、1相關聯 &gt; 。

第1個投射： ![顯示第一次投影計算2的方程式。](images/transformcreation-image113.png)

第2個投射： ![顯示運算2的第二個投射的方程式。](images/transformcreation-image115.png)

第三個投射： ![顯示計算2的第三個投影的方程式。](images/transformcreation-image117.png) ，位於臉部 x3 = 0。 回溯替代，然後提供

![顯示後向替代的前兩個方程式。](images/transformcreation-image119.png)

![顯示反向替代的第三個方程式。](images/transformcreation-image123.png)，這是最後的答案。

## <a name="applications"></a>應用程式

*() 順序 Tetrahedral 插補*

![顯示連續 tetrahedral 插補的圖表。](images/transformcreation-image124.png)

**圖3：** 順序 tetrahedral 插補

請參閱 [圖 3]。 若要在兩個不相容格線的平面之間進行插入，請考慮將圖中所示的指定點 P 括住的儲存格。 儲存格的「頂端」頂點直接來自于頂端平面的方格。 底部臉部中的頂點與底部平面中的方格不相容，因此整個臉部會被視為具有 BC，其值是由底平面方格中的插補所取得。 然後，這項設定會明確指出此設定符合假設 () 、 (b) 和上述 (c) ，而且您可以套用插補演算法。

此外，演算法也會將插補問題的維度縮減1，因為結果是在上方格頂點的線性組合，以及較低平面中的插補，其維度較少1。 如果較低的平面中有類似的將平面設定，您可以在該平面中套用程式，進一步將維度縮減1。 此程式可繼續進行，直到您到達維度0為止。 這個投射和插補可以稱為「連續 Tetrahedral 插補」。

*(b) 間隙插補*

![顯示間隙插補的圖表。](images/transformcreation-image126.jpg)

**圖4：** 間隙插補

這是在正面象限中嚴格放置的 cube 上所強加的方格。 Cube 本身具有方格，而且每個座標平面都有不一定相容的格線。 Cube 和座標平面之間的「間距」具有「L 形」的跨區段，而且不會適合至標準技術。 不過，在這裡引進的技術，您可以輕鬆地導入涵蓋此間距的儲存格。 [圖 4] 描繪其中一種。 座標平面上的方格支援插補，為數據格的所有最下方臉部提供必要的 BC，還有一個剩餘的頂點，而該頂點的 BC 是由 cube 的右下角提供。

## <a name="final-note-on-implementation"></a>執行的最終注意事項

在實際的應用程式中，會從較大的 lattices 中解壓縮演算法基本設定的「單位 cube」，而頂點上的值可能需要昂貴的計算。 另一方面，也可以明確地說，tetrahedral 插補只需要四面體頂點的值，也就是 unit cube 中所有頂點的子集。 因此，您可以更有效率地執行所謂的「延後評估」。 在上述演算法的軟體執行中，通常會有副程式接受單位 cube 和其頂點的值做為輸入。 延後評估表示不會在頂點上傳遞值，而是會傳遞評估頂點值所需的資訊，而不會實際執行評估。 在副程式中，在決定封入四面體之後，這些值的實際評估將只會針對屬於封閉四面體的頂點執行。

## <a name="lookup-table-for-use-with-high-dynamic-range-virtual-rgb-source-devices"></a>用於高動態範圍虛擬 RGB 來源裝置的查閱資料表

在使用模型化為虛擬 RGB 裝置的來源裝置來建立轉換的情況下，來源 colorant 值可能會是負數或大於 unity (1.0) 。 發生這種情況時，來源裝置會被稱為具有高動態範圍 (HDR) 。 在此情況下，會進行特別考慮。

在 HDR 轉換的情況下，每個 colorant 頻道的最小值和最大值都可以從裝置的範圍界限來決定。 藉由使用這些值，就會套用每個 colorant 通道的簡單縮放，讓等於最小 colorant 的 colorant 值會轉換為0.0，而等於最大 colorant 的 colorant 值會轉換為1.0，並以線性方式調整介於0.0 和1.0 之間的值。

### <a name="iccprofilefromwcsprofile"></a>ICCProfileFromWCSProfile

由於這項功能的主要目的是要支援 Windows Vista 之前的版本，因此您必須產生2.2 版的 ICC 設定檔（如 ICC 規格中所定義）。1： 1998-09。 在某些情況下 (請參閱下表「基準裝置至 ICC 設定檔類別對應」 ) ，您可以從 WCS 設定檔建立矩陣或 >FLIGHTRECORDERCURRENT.TRC 型的 ICC 設定檔。 在其他情況下，ICC 設定檔是由 LUTs 所組成。 下列程式說明如何建立 AToB 和 BToA LUTs。 當然，ICC 設定檔也有其他欄位。 某些資料可以衍生自 WCS 設定檔。 對於其他資料，您必須開發智慧型預設值。 系統會將著作權指派給 Microsoft;因為它是用來建立 LUTs 的 Microsoft 技術。

這項設計應該適用于所有類型的裝置模型，包括外掛程式。只要外掛程式有相關聯的基準裝置模型，就可以決定基礎裝置類型。

建立 ICC 設定檔的困難部分是建立 AToB 和 BToA 查閱資料表。 這些資料表會在裝置空間之間進行對應，例如 RGB 或 CMYK，以及設定檔連接空間 (電腦) ，也就是 CIELAB 的變化。 這基本上與在引用轉換中用來從裝置空間對應到裝置空間的色彩管理程式相同。 不過，您必須擁有下列資訊才能進行轉換。

1) 電腦的參考視圖條件。

2) 參考電腦的範圍。

3) 在電腦值和 colorimetry 之間轉換的裝置型號。

WCS 設定檔及其相關聯的凸輪會以參數形式提供。 Colorimetry 和電腦編碼之間有兩種基準裝置模型可進行轉換。 您需要兩個的原因，如下所述。

1) 您可以從「ICC 設定檔」格式規格取得電腦的參考視圖條件。 在 ICC 配置檔案格式規格中提供的資訊，足以計算將 CMS 所使用的凸輪初始化所需的所有資料。 基於一致性和彈性，此資訊會儲存在 WCS 色彩設定檔中。

2) 您也可以使用 WCS 設定檔來儲存定義電腦參考範圍的範例。 引用色彩管理系統 (CMS) 有兩種建立範圍界限的方式。 其中一個是將完整的裝置空間取樣，並使用裝置模型來建立測量值。 第二種方法是使用設定檔中的測量樣本來建立參考範圍界限。 由於 ICC 電腦的範圍太大而無法提供有用的參考範圍，因此第一個方法是不適當的。 但第二個方法是彈性、以設定檔為基礎的方法。 若要重新定義參照電腦範圍，您可以變更電腦裝置設定檔中的測量資料。

3) ICC 電腦是理想裝置的模型。 藉由將電腦的模型建立為真實裝置，您就可以利用智慧型 CMM 中所使用的色彩管理流程。 從 colorimetry 建立裝置型號至電腦編碼很簡單。 您只需在真正的色度值和電腦編碼值之間進行對應。 由於裝置型號的 CMS 介面僅支援 XYZ 值，您可能也必須在 XYZ 和 LAB 之間進行對應。 這是知名的轉換。 此模型會在7.9 和7.10 章節的 < 基準裝置模型2.2.02 檔中說明。

如果裝置的範圍大於電腦的範圍，您可能必須執行一些 gamut 對應。 基準 GMMs 可用於此用途。 請注意，已正確建立的 ICC 設定檔具有相對色度、感知和飽和度意圖的查閱資料表，不過它們在內部都可能指向相同的 LUT。

![此圖顯示如何建立 T o B L U T。](images/transformcreation-image128.png)

**圖5：** 建立 AToB LUT

[圖 5] 說明此進程。 首先，裝置模型會從 DM 設定檔中的資料初始化。 然後，依照下列方式來建立裝置範圍界限。 裝置模型的資料取樣是透過裝置模型執行，以取得色度資料。 色度資料是透過凸輪執行，以建立外觀資料。 外觀資料會用來建立裝置範圍界限。

接下來，使用參照電腦測量設定檔中的資料來建立電腦的範圍界限。

使用剛剛建立的兩個 gamut 界限來初始化 GMM。 然後，使用裝置型號、GMM 和電腦裝置模型來建立轉換。 透過轉換執行裝置空間的取樣，以建立 AToB LUT。

![此圖顯示如何使用 P C S 空間的取樣來建立 T o B L U T。](images/transformcreation-image130.png)

**圖6：** 建立 BToA LUT

圖6說明如何建立 BToA LUT。 這幾乎與建立 AToB LUT，並交換來源和目的地的角色相同。 此外，您必須將完整的電腦範圍取樣，才能建立 LUT。

請注意，由於 CIECAM02) 中的凸輪 (是在程式中進行，所以彩色會在媒體的白色點和電腦的白色 (點之間進行調整，而由 D50 所規定的) 會由凸輪透明地影響。

## <a name="hdr-virtual-rgb-devices"></a>HDR 虛擬 RGB 裝置

產生適用于 HDR 虛擬 RGB 裝置的設定檔時，必須提供特殊考慮;亦即，colorant 值可能小於0.0 或大於1.0 的裝置。 在產生 ATOB LUT 時，會建立一組較大的1D 輸入 LUTs。 Colorant 值會縮放並位移至範圍0。 1使用 WCS 設定檔中的最小和最大 colorant 值。

因為 HDR 裝置的 colorant 空間不太可能完全擴展，所以也會在 3D LUT 中針對標記提供特殊支援。 為了處理稀疏擴展區域中的色彩，colorants 會重新編碼，因此可以達成超過0.0 和1.0 的推斷。 使用的範圍為-1。 + 4。

由於適用于 3-d LUT 的重新調整已套用，因此會建立一組1D 輸出 LUTs，以將結果對應至範圍0。 1.

## <a name="more-than-one-pcs"></a>一部以上的電腦

ICC 發現一台電腦沒有足夠的彈性可符合 CMS 的所有用途。 在設定檔規格的第4版中，ICC 闡明瞭實際上有兩種電腦編碼。 一個用於色度意圖;另一個用於可感知意圖。  (飽和度意圖未指定任何電腦。 ICC 已將此部分省略。 ) 色度電腦的最小和最大亮度都已指定，但色度和色調值的範圍大約為±127。 這台電腦看起來像是一個矩形 prism。 如先前所述，可感知的電腦音量與噴墨印表機的範圍類似。

這兩個 ICC PCSs 也有兩種不同的數位編碼。 在感知電腦中，值為零表示亮度為零。 在色度電腦中，值為0代表電腦的最小亮度（大於零）。 您可以針對每部電腦編碼使用不同的裝置型號，以解決此問題。

## <a name="gamut-mapping"></a>Gamut 對應

若要在 ICC 設定檔中建立 AToB LUTs，您可以從裝置範圍對應到適當的電腦空間。 若要建立 BToA LUTs，您可以從 [電腦] 空間對應到裝置範圍。 AToB LUTs 的對應相當類似于以測量為基礎的 CMS 中所使用的對應。 針對可感知的電腦，使用任何超出範圍色彩的裁剪或壓縮，將裝置合理範圍對應到可感知的電腦範圍界限。 針對色度意圖，您可能必須裁剪亮度，但色度和色調值全都會放在色階電腦範圍內。

BToA LUTs 的對應有點不同。 色度意圖仍很簡單;您只需將電腦值裁剪到裝置範圍中。 但 ICC 要求所有可能的電腦值都必須對應至某些裝置值，而不只是在可感知電腦的參考範圍內的值。 因此，您必須確定 GMMs 可以處理位於參考範圍外的來源色彩。 將這些色彩裁剪至裝置範圍界限，即可處理此情況。

## <a name="baseline-device-to-icc-profile-class-mapping"></a>基準裝置與 ICC 設定檔類別的對應



| 基準裝置類型              | ICC 設定檔類別       | 備註                                                                      |
|-----------------------------------|-------------------------|-----------------------------------------------------------------------------|
| RGB 捕獲裝置                | 輸入裝置 ( "scnr" )    | 電腦 CIELAB。 AToB0Tag 是裝置到具有相對色度意圖的電腦。 |
| CRT、LCD 監視器                  | 顯示裝置 ( "mntr" )  | 電腦 CIEXYZ。 請參閱下列模型轉換。                      |
| RGB 投影機                     | 色彩空間 ( "spac" )     | 電腦 CIELAB。                                                              |
| RGB 和 CMYK 印表機              | 輸出裝置 ( "prtr" )   | 電腦 CIELAB。                                                              |
| RGB 虛擬裝置 (非 HDR 案例)  | 顯示裝置 ( "mntr" )  | 電腦 CIEXYZ。                                                              |
| RGB 虛擬裝置 (HDR 案例)      | 色彩空間 ( "spac" )     | 電腦 CIELAB。                                                              |



 

監視設定檔的轉換不牽涉到建立 LUTs，而是包含建立矩陣或 >FLIGHTRECORDERCURRENT.TRC 模型。 在 ICC 中使用的模型與 WCS CRT 或 LCD 模型中使用的模型略有不同，因為缺少「黑色更正」詞彙。 具體而言，

WCS 模型： ![顯示 W C S 模型。](images/transformcreation-image132.png)

ICC 模型： ![顯示 I C C 模型。](images/transformcreation-image134.png)

從 WCS 模型到 ICC 模型的轉換如下所示。

定義新曲線：

![顯示定義新曲線的矩陣。](images/transformcreation-image136.png)

這些都不是音訊複製曲線，因為它們不會將1對應至1。 正規化將達成此目標。 ICC 模型的最終定義如下：

![顯示 I C C C 模型的最後定義。](images/transformcreation-image138.png)

![顯示 C # c C 模型的最終矩陣。](images/transformcreation-image140.png)

針對非 HDR RGB 虛擬裝置，您也會產生顯示的 ICC 設定檔以取得空間效率。 在此情況下，您可以直接從 WCS 設定檔的主要複本取得 tristimulus 矩陣 *M ICC* ，而不需要上述模型轉換。 最後一點要注意的是，這個 tristimulus 矩陣必須 chromatically 調整成 D50，才能符合電腦的 ICC 規格。 換句話說，要在 ICC 設定檔中編碼之矩陣的每個資料列上的專案，必須分別加總為96.42、100和82.49。 在目前的執行中，彩色的調整是由 CAT02 完成，也就是 CAM02 中使用的彩色調整轉換。

## <a name="black-preservation-and-black-generation"></a>黑色保留和黑色世代

黑色保留的執行會與支援黑色通道的裝置產生黑色通道相關聯。 為了達成此目的，會收集每個來源色彩的相關資訊，以允許支援黑色頻道的裝置型號判斷輸出上的黑色通道的最佳設定。 雖然黑色保留適用于將一個黑色通道裝置轉換成另一個黑色通道裝置的色彩轉換，但是針對所有涉及黑色通道目的地裝置的轉換，都會實行黑色世代。

黑色通道資訊會記錄在名為 [**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)的資料結構中。 **BlackInformation** 結構包含布林值，指出色彩是否只包含黑色 colorant，以及表示 "blackness" 角度的數值（稱為黑色權數）。 針對支援黑色通道的來源裝置，黑色權數是來源色彩中黑色 colorant 的百分比。 如果來源裝置不包含黑色通道，則會使用其他 colorants 和外觀值來計算黑色權數。 名為 "color 純度" 的值是藉由讓最大 colorant 值與最小 colorant 值之間的差異除以最大 colorant 值來計算。 稱為「相對亮度」的值是藉由讓色彩的亮度與目的地裝置的最小亮度之間的差異除以目的地裝置的最小和最大亮度之間的差異來計算。 如果來源裝置是 (監視器或投影機) 的加法裝置，則會將黑色權數判斷為1.0 減去色彩純度乘以相對亮度。 例如，如果來源裝置是 RGB 監視器，則會計算每個色彩的最大值和 R、G 和 B 的最大值，並以公式來決定黑色權數：

BW = (1.0 – (max (R、G、B) – min (R、G、B) ) /max (R、G、B) ) \* 相對亮度

如果來源裝置支援 subtractive 色彩（例如，CMY 印表機），則個別的 colorants 必須是在上述公式中使用之前，從 1.0) 減去 (。 因此，若是 CMY 印表機，R = 1.0 – C、G = 1.0 – M 和 B = 1.0 – Y。

色彩轉譯程式期間會決定色彩轉換所處理的每個色彩的黑色資訊。 只有在指定了黑色保留時，才會決定僅限黑色的資訊。 如果目的地裝置型號支援黑色 colorant，一律會決定黑色權數。 黑色資訊會透過 [**ColorimetricToDeviceColorsWithBlack**](/previous-versions/windows/desktop/api/WcsPlugIn/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack) 方法傳遞至目的地裝置模型，該方法會使用產生的 LUT。

請注意，由於色彩轉換優化，上述進程只會在建立優化的轉換 LUT 期間發生，而不是在 TranslateColors 方法執行期間發生。

## <a name="optimization-for-transforms-with-more-than-three-source-channels"></a>使用三個以上的來源頻道進行轉換的優化

優化轉換的大小取決於數個因素：來源裝置中的色彩頻道數目、每個來源色頻的表格步驟數目，以及輸出裝置中的色彩頻道數目。 判斷轉換資料表大小的公式如下：

大小 = 每個通道來源的步驟數 <sub>\ 裝置 (數目 \ 通道 \ in \ 來源 \ 裝置) </sub> x 輸出裝置中的通道數目

如您所見，資料表的大小會根據來源裝置中的通道數目以指數方式成長。 許多來源裝置都支援三色通道，例如紅色、綠色和藍色。 但是，如果來源裝置支援四個通道，例如 CMYK，則資料表的大小和建立資料表所需的時間會隨著步驟數目的因素成長。 在以度量為基礎的 CMS 中，轉換是「即時」的，這次可能無法接受。

若要減少建立色彩轉換表所需的時間，您可以利用兩個事實。 首先，雖然來源裝置可支援三個以上的色頻，但與中繼裝置無關的色彩空間 (CIECAM02 Ja-jp <sub>c</sub> b <sub>c</sub> ) 只有三個色頻。 其次，處理常式中最耗時的部分不是裝置模型 (從裝置色彩座標轉換成 tristimulus 值) ，但是範圍對應。 您可以使用這些事實來建立初步的色彩轉換表，以透過範圍對應步驟來轉換裝置獨立色彩空間中的色彩，最後再透過輸出裝置色彩模型來轉換。 此資料表的結構是三個維度。 接著，我們會藉由將來源色彩組合轉換成中繼裝置獨立空間，然後使用初稿的色彩轉換表，完成轉換輸出裝置色彩空間，來構成四個最終的色彩轉換表。 因此，您可以減少查閱資料表中的 (步驟數目，) <sub>number \ of \ 通道</sub> 範圍將計算對應到中繼資料表₃範圍對應計算中的步驟數目。 雖然您必須在 (查閱資料表中執行步驟的數目，) 裝置模型化和三維資料表查閱的 # \ <sub>通道計算數目</sub> ，但這仍比原始計算快得多。

上述程式可正常運作，因為不需要在來源裝置模型和色彩轉換中的任何其他元件之間傳遞資訊。 但是，如果輸出裝置和來源裝置都支援黑色 colorant，而來源黑色 colorant 用於判斷輸出黑色 colorant，則程式將無法正確地傳達來源黑色資訊。 替代程式是建立初步的色彩轉換表，只透過範圍對應步驟來轉換裝置獨立色彩空間中的色彩。 然後使用下列步驟來建立維度四個最終的色彩轉換表：) 將來源色彩組合轉換成與中繼裝置無關的空間，b) 執行範圍對應步驟，方法是在初步色彩表中進行插入，而不是套用實際的 gamut 對應進程，而 c) 使用範圍對應步驟中所產生的值和任何來源黑色通道資訊，使用輸出裝置模型來計算輸出裝置 colorants。 當來源和輸出裝置模型之間有資訊傳輸時，即使沒有黑色通道，也可以使用此程式。例如，如果兩個模組是使用允許在模組之間進行資料交換的外掛程式架構所執行。

先前的兩個處理常式可以用來有效地改善建立四維色彩轉換資料表所需的時間。

### <a name="checkgamut"></a>CheckGamut

ICM 呼叫 CreateTransform 和 **CreateMultiProfileTransform** 會取得旗標值的文字，其中一個是啟用範圍 \_ \_ 檢查。 當設定這個旗標時，引用必須以不同的方式建立轉換。 初始步驟相同：必須初始化來源和目的地攝影機，然後必須初始化來源和目的地範圍界限描述元。 無論指定的意圖為何，都必須使用 CheckGamut GMM。 CheckGamut GMM 應該使用來源和目的地裝置模型和範圍界限描述項進行初始化。 不過，轉換接著應建立截斷的轉換，其中包含來源裝置模型、來源凸輪、任何仲介 GMMs 和 CheckGamut GMM。 這可確保 CheckGamut CMM 輸出的 delta J、delta C 和 delta h 值會成為最後產生的值。

當轉換中只有兩個裝置設定檔時，CheckGamut 的意義很清楚。 當有兩個以上的裝置設定檔和兩個以上的 GMMs 時，CheckGamut 會報告是否已透過第一個裝置型號轉換的色彩，以及最後一個 GMM 以外的所有色彩是否落在目的地裝置的範圍內。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本色彩管理概念](basic-color-management-concepts.md)
</dt> <dt>

[Windows 色彩系統架構和演算法](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




