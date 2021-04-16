---
title: MCI 命令的分類
description: MCI 命令的分類
ms.assetid: e03edfab-06c9-4337-935b-9effd2996c2e
keywords:
- MCI 命令，分類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1524e6aa2094679e91acddb9dbfbb8cb480eb39f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507061"
---
# <a name="classifications-of-mci-commands"></a>MCI 命令的分類

MCI 定義四個命令分類： system、required、basic 和 extended。 下列清單描述這些命令分類：

-   *系統命令* 會由 MCI 直接處理，而不是由驅動程式來處理。
-   *必要的命令* 是由驅動程式處理。 所有的 MCI 驅動程式都必須支援必要的命令和旗標。
-   某些裝置使用的 *基本命令* (或選用的命令) 。 如果裝置支援基本命令，它必須支援該命令的一組已定義旗標。
-   *擴充命令* 是裝置類型或驅動程式專用的。 擴充的命令包括命令，例如 [**put**](put.md) ([**MCI \_ put**](mci-put.md)) ， [**以及 (的**](where.md) [**mci， \_ 其中**](mci-where.md) **digitalvideo** 和重迭裝置類型的) 命令，以及現有命令的延伸 (像是覆 **迭裝置類型** (之 [**狀態**](status.md)) [**MCI \_ 狀態**](mci-status.md)) 命令的「延展」旗標。

雖然系統和必要的命令是針對任何 MCI 驅動程式所設定的最小命令，但並非所有驅動程式都支援 basic 和 extended 命令。 您的應用程式一律可以使用系統和所需的命令及其旗標，但如果需要使用基本或擴充的命令或旗標，則應該先使用 ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) 命令的 [**功能**](capability.md)來查詢驅動程式。 下列各節摘要說明每個類別中的特定命令。

## <a name="system-commands"></a>系統命令

MCI 會直接處理下列系統命令，而不是將它們傳遞給 MCI 裝置。



| String                 | 訊息                             | 描述                            |
|------------------------|-------------------------------------|----------------------------------------|
| [**打破**](break.md) | [**MCI \_ 斷路**](mci-break.md)     | 設定 MCI 裝置的 break 鍵。    |
| [sysinfo](sysinfo.md) | [**MCI \_ SYSINFO**](mci-sysinfo.md) | 傳回 MCI 裝置的相關資訊。 |



 

## <a name="required-commands"></a>必要的命令

所有 MCI 裝置都支援下列必要的命令。



| String                           | 訊息                                   | 描述                                                                                                               |
|----------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**能力**](capability.md) | [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) | 取得裝置的功能。                                                                                     |
| [**關閉**](close.md)           | [**MCI \_ 關閉**](mci-close.md)           | 關閉裝置。                                                                                                        |
| [**資訊**](info.md)             | [**MCI \_ 資訊**](mci-info.md)             | 從裝置取得文字資訊。                                                                                |
| [**打開**](open.md)             | [**開啟的 MCI \_**](mci-open.md)             | 初始化裝置。                                                                                                   |
| [**地位**](status.md)         | [**MCI \_ 狀態**](mci-status.md)         | 取得裝置的狀態資訊。 此命令的部分旗標並非必要，因此它也是基本命令。 |



 

裝置也必須支援必要命令的一組標準命令旗標。

## <a name="basic-commands"></a>基本命令

下列清單摘要說明基本命令。 MCI 裝置使用這些命令是選擇性的。



| String                   | 訊息                           | 描述                                                                                                                                                                                                                             |
|--------------------------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**負荷**](load.md)     | [**MCI \_ 負載**](mci-load.md)     | 從檔案載入資料。                                                                                                                                                                                                                 |
| [**暫停**](pause.md)   | [**MCI \_ 暫停**](mci-pause.md)   | 停止播放。 您可以在目前的位置繼續播放或錄製。                                                                                                                                                            |
| [**玩**](play.md)     | [**MCI \_ 播放**](mci-play.md)     | 開始傳輸輸出資料。                                                                                                                                                                                                        |
| [**記錄**](record.md) | [**MCI \_ 記錄**](mci-record.md) | 開始記錄輸入資料。                                                                                                                                                                                                            |
| [**恢復**](resume.md) | [**MCI \_ 繼續**](mci-resume.md) | 在暫停的裝置上繼續播放或錄製。                                                                                                                                                                                        |
| [**救**](save.md)     | [**MCI \_ 儲存**](mci-save.md)     | 將資料儲存到磁片檔案。                                                                                                                                                                                                              |
| [**尋求**](seek.md)     | [**MCI \_ 搜尋**](mci-seek.md)     | 向前或向後搜尋。                                                                                                                                                                                                              |
| [**設置**](set.md)       | [**MCI \_ 組**](mci-set.md)       | 設定裝置的操作狀態。                                                                                                                                                                                                 |
| [**地位**](status.md) | [**MCI 狀態**](mci-status.md)  | 取得裝置的狀態資訊。 這也是必要的命令;由於某些旗標並非必要，因此也會列在這裡。  (選用專案支援使用具有可識別位置之線性媒體的裝置。 )  |
| [**停止**](stop.md)     | [**MCI \_ 停止**](mci-stop.md)     | 停止播放。                                                                                                                                                                                                                          |



 

如果驅動程式支援基本命令，它也必須支援一組標準的旗標，以供命令使用。

## <a name="extended-commands"></a>擴充的命令

某些 MCI 裝置有額外的命令，或將旗標新增至現有的命令。 雖然某些擴充的命令只適用于特定的設備磁碟機，但大部分都適用于特定裝置類型的所有驅動程式。 例如，針對 **sequencer** 裝置類型所設定的命令會將 [**set**](set.md) ([**MCI \_ SET**](mci-set.md)) 命令，以新增 MIDI sequencers 所需的時間格式。

您不應該假設裝置支援擴充的命令或旗標。 您可以使用 ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) 命令的 [**功能**](capability.md)來判斷是否支援特定功能，而且您的應用程式應該準備好處理「不支援的命令」或「不支援的函數」傳回值。

下列擴充命令適用于列出的裝置類型。



| String                         | 訊息                                 | 裝置類型            | Description                                                                                       |
|--------------------------------|-----------------------------------------|-------------------------|---------------------------------------------------------------------------------------------------|
| [**配置**](configure.md) | [**MCI \_ 設定**](mci-configure.md) | digitalvideo            | 顯示 [設定] 對話方塊。                                                              |
| [**提示**](cue.md)             | [**MCI \_ 提示**](mci-cue.md)             | digitalvideo, waveaudio | 準備播放或錄製。                                                                |
| [**刪除**](delete.md)       | [**MCI \_ 刪除**](mci-delete.md)       | waveaudio               | 從媒體檔案中刪除資料區段。                                                       |
| [逃脫](escape.md)           | [**MCI \_ ESCAPE**](mci-escape.md)       | videodisc               | 將自訂資訊傳送至裝置。                                                             |
| [**凍結**](freeze.md)       | [**MCI \_ 凍結**](mci-freeze.md)       | overlay                 | 停用框架緩衝區的影片捕獲。                                                   |
| [**把**](put.md)             | [**MCI PUT**](mci-put.md)              | digitalvideo，重迭   | 定義來源、目的地和框架視窗。                                               |
| [**實現**](realize.md)     | [**MCI \_ 意識**](mci-realize.md)     | digitalvideo            | 告知裝置在顯示的視窗中，選取並實現其調色板的裝置內容。 |
| [**setaudio**](setaudio.md)   | [**MCI \_ SETAUDIO**](mci-setaudio.md)  | digitalvideo            | 設定影片的音訊參數。                                                                  |
| [**setvideo**](setvideo.md)   | [**MCI \_ SETVIDEO**](mci-setvideo.md)  | digitalvideo            | 設定影片參數。                                                                            |
| [**signal**](signal.md)       | [**MCI \_ 信號**](mci-signal.md)       | digitalvideo            | 識別具有信號的指定位置。                                                    |
| [**自 旋**](spin.md)           | [**MCI \_ 旋轉**](mci-spin.md)           | videodisc               | 啟動光碟旋轉或停止光碟的旋轉。                                         |
| [**步**](step.md)           | [**MCI \_ 步驟**](mci-step.md)           | digitalvideo, videodisc | 逐步播放一或多個畫面格。                                             |
| [**解凍**](unfreeze.md)   | [**MCI \_ 解除凍結**](mci-unfreeze.md)   | overlay                 | 讓框架緩衝區取得影片資料。                                                   |
| [**更新**](update.md)       | [**MCI \_ 更新**](mci-update.md)       | digitalvideo            | 將目前的框架重新繪製到裝置內容中。                                               |
| [**其中**](where.md)         | [**MCI，其中**](mci-where.md)          | digitalvideo，重迭   | 取得指定來源、目的地或框架區域的矩形。                          |
| [**視窗**](window.md)       | [**MCI \_ 視窗**](mci-window.md)       | digitalvideo，重迭   | 控制顯示視窗。                                                                      |



 

 

 




