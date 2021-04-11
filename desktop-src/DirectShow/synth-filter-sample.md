---
description: 合成濾波器範例
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: 合成濾波器範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852403"
---
# <a name="synth-filter-sample"></a>合成濾波器範例

## <a name="description"></a>Description

合成濾波器是產生音訊波形的來源篩選器。

此篩選器說明動態圖形建築物。 它可以在未壓縮的 PCM 音訊與壓縮的 MS ADPCM 之間切換 \_ (Microsoft 彈性 Delta 脈衝 Code 調製) 格式。

此篩選器會以「音訊合成器篩選」的形式出現在 GraphEdit 中。

如需動態圖形建築物的詳細資訊，請參閱 [動態圖形建築物](dynamic-graph-building.md)。

## <a name="usage"></a>使用方式

合成篩選器可讓使用者透過屬性頁設定波形、頻率、通道數目和其他屬性。 若要設定掃描頻率範圍的上方或較低端點，請按住 SHIFT 鍵，同時調整頻率滑杆。 篩選也支援自訂介面 ISynth2，以設定這些屬性。

若要示範動態圖形建立功能，請執行下列動作：

1.  建立篩選器，並使用 Regsvr32 公用程式進行註冊。
2.  啟動 GraphEdit。
3.  插入音訊合成器篩選器。 它會出現在 [DirectShow 篩選準則] 分類中。
4.  轉譯篩選的輸出圖釘。
5.  按一下 [ **播放** ] 按鈕。
6.  開啟篩選的屬性頁。
7.  在 [輸出格式] 區域中，選取 [PCM] 或 [Microsoft ADPCM]。

## <a name="programming-notes"></a>程式設計附注

此範例包含下列檔案：

-   Dynsrc .h （Dynsrc .cpp：）包含兩個來源篩選準則的基類，這些類別支援動態圖形建立、CDynamicSource 和 CDynamicSourceStream。
-   ISynth：宣告用來設定篩選準則屬性的自訂 ISynth2 介面。
-   資源 .h：包含資源常數。
-   .Def：匯出 COM 程式庫所需的 DLL 函式。
-   CAudioSynth 類別會產生音訊資料，而 CSynthFilter 類別則是用來執行此篩選器。
-   合成 .rc：包含篩選所使用的資源。
-   Synthprp .h、Synthprp .cpp：執行篩選的屬性頁。

CDynamicSource 類別是從 [**CSource**](csource.md) 基類進行調整。 它會使用一個或多個衍生自 CDynamicSourceStream 類別的輸出圖釘。 CDynamicSourceStream 類別是從 [**CSourceStream**](csourcestream.md) 類別進行調整，但衍生自 [**CDynamicOutputPin**](cdynamicoutputpin.md) 類別，而不是 [**CBaseOutputPin**](cbaseoutputpin.md) 類別。

CDynamicSource 類別在 [**CSource**](csource.md)中找不到下列方法：

-   停止：發出停止事件 ([**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) ，然後關閉背景工作執行緒以取得所有未連接的 pin。 在連接的釘選上，pin 的非使用中方法會關閉背景工作執行緒。
-   Pause：重設停止事件。
-   JoinFilterGraph：呼叫每個 pin 的 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) 方法。

CDynamicSourceStream 類別在 [**CSourceStream**](csourcestream.md)中找不到下列方法：

-   DestroySourceThread：關閉背景工作執行緒。
-   FatalError：對篩選圖形管理員發出錯誤信號。
-   OutputPinNeedsToBeReconnected：表示輸出 pin 應重新連接。 當呼叫這個方法時，背景工作執行緒會呼叫 [**CDynamicOutputPin：:D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) 方法來重新連接釘選。

## <a name="downloading-the-sample"></a>下載範例

若要下載 DirectShow SDK 範例，請安裝最新版本的 [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。

此範例安裝在下列路徑下： *\[ SDK \] 根* \\ 範例 \\ 多媒體 \\ DirectShow \\ 濾波器 \\ 合成。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 範例](directshow-samples.md)
</dt> </dl>

 

 



