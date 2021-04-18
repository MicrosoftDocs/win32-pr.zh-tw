---
title: 從 MCI 裝置串流捕獲
description: 從 MCI 裝置串流捕獲
ms.assetid: 44cbf375-f97e-426a-a703-dfb1b1933138
keywords:
- MCI (媒體控制介面) 、串流捕獲
- WM_CAP_SET_MCI_DEVICE 訊息
- capSetMCIDeviceName 宏
- WM_CAP_GET_MCI_DEVICE 訊息
- capGetMCIDeviceName 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8cf358a87a812024328abf7fc1aae0509a126f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507373"
---
# <a name="streaming-capture-from-an-mci-device"></a>從 MCI 裝置串流捕獲

MCI 裝置會在即時捕捉和逐步執行框架捕獲中增強捕獲作業。 您可以使用 [ [**WM \_ CAP \_ SET \_ MCI \_ 裝置**](wm-cap-set-mci-device.md) 訊息] (或 [ [**capSetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capsetmcidevicename) ] 宏) 並指定裝置的名稱，指定 MCI 裝置，例如 videodisc 或攝影機 (VCR) ，作為您的捕獲操作影片來源。 您也可以使用 [ [**WM \_ CAP \_ 取得 \_ MCI \_ 裝置**](wm-cap-get-mci-device.md) 訊息 (] 或 [ [**capGetMCIDeviceName**](/windows/desktop/api/Vfw/nf-vfw-capgetmcidevicename) 宏) ，來取出目前設定的裝置名稱。

在即時捕捉中，[捕獲] 視窗會同步處理捕獲作業，並補償與放置 MCI 影片來源和初始化 (資源相關的延遲（例如捕獲資料時所需的擷取緩衝區) ）。 [Capture （capture）] 視窗預期在系統中安裝有效的 MCI video 裝置，以透過這種方式來捕捉資料。

控制 MCI 裝置的規格會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) 結構的成員中。 MCI 相容的影片來源包含 Vcr 和 laserdiscs。 如果此結構的 **fMCIControl** 成員設定為 **TRUE**，則 [捕獲] 視窗會協調 MCI 作業。 [捕獲] 視窗會使用 **dwMCIStartTime** 和 **dwMCIStopTime** 成員中指定的參數，來取得序列的開始和停止位置（以毫秒為單位）。 如果 **fMCIControl** 的值為 **FALSE**，則不會將影片來源視為 MCI 裝置，而且會忽略 **dwMCIStartTime** 和 **dwMCIStopTime** 的內容。

您可以使用 Media Player 快速確認 MCI video 裝置已正確連接至系統。 使用 Media Player 播放裝置會確認裝置的 MCI 設定是否正確。 如果影像顯示在影片顯示器上，則影片來源會正確地連接到「捕獲硬體」。

在 [逐步執行] 視窗中，[捕獲] 視窗會同步處理捕獲作業，並補償與放置 MCI 影片來源和初始化所需資源的相關延遲。 此外，[capture （capture）] 視窗可確保不會卸載任何框架;它會個別逐步執行影片畫面，以確保在影片串流中的下一個畫面格之前，會先捕捉並儲存畫面格。

控制步驟框架捕獲的規格會儲存在 [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) 結構的成員中。 除了用於即時捕捉的成員之外，步驟框架捕獲還會使用下列成員： **fStepMCIDevice**、 **fStepCaptureAt2x** 和 **wStepCaptureAverageFrames**。 如果 **fStepMCIDevice** 成員設定為 **TRUE**，則 [捕獲] 視窗會協調步驟框架捕獲。 [捕獲] 視窗會使用 **dwMCIStartTime** 和 **dwMCIStopTime** 成員中指定的參數，來進行序列的開始和停止位置（以毫秒為單位）。 [Capture （capture）] 視窗會使用 **fStepCaptureAt2x** 來判斷捕獲硬體是否應該以一般解析度的兩倍來捕獲影片畫面，並使用 **wStepCaptureAverageFrames** 來指定取樣的每個畫面格所經過的次數。

如果 **fStepMCIDevice** 為 **FALSE**，則會使用即時捕捉，而不是逐步執行框架捕獲和 **fStepCaptureAt2x** 的內容，而且會忽略 **wStepCaptureAverageFrames** 。

如果指定了步驟框架捕獲，且 **fStepCaptureAt2x** 設定為 **TRUE**，則捕獲硬體會以指定的解析度兩倍來捕捉。  (高度和寬度的解析度加倍。 ) 軟體會將圖元插在較高解析度的影像中，以指定的解析度產生映射。 這種形式的平均可以改善框架中影像的邊緣定義。 如果硬體不支援以硬體為基礎的減去，而且您是以 RGB 格式進行捕捉，則可以啟用此選項。

> [!Note]  
> 如果您的硬體支援以硬體為基礎的減去，它可以以比指定更高的速率來捕捉範例，並使用這些額外的範例來取得與原始影像更一致的色彩定義。 使用之後會捨棄額外的範例，而硬體會以指定的速率將範例傳至 capture 驅動程式。

 

如果指定了步驟框架捕獲， **wStepCaptureAverageFrames** 成員會指定根據平均範例建立框架時，所取樣的框架次數。 這種平均技術可減少出現在框架中的亂數字化雜訊。 平均值的一般值為5。

如需 MCI 的詳細資訊，請參閱 [mci](mci.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[捕捉變化](capture-variations.md)
</dt> </dl>

 

 




