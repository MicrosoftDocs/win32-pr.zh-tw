---
description: YUV 混合模式
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: YUV 混合模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 957c5345eb80576ad0371558bb60d0b6651221bd98d7830cb968f39c16330fb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290748"
---
# <a name="yuv-mixing-mode"></a>YUV 混合模式

本主題適用于 Windows XP Service Pack 2 或更新版本。

從 Windows XP Service Pack 2 開始，VMR 支援稱為 YUV 混合模式的混合模式。 這種模式最適用于先進的電視或 DVD 應用程式。 它會在使用統一記憶體架構設計的低終端圖形硬體上，以更佳的效能來為 VMR 混音器提供更佳的效能。 VMR-7 和 VMR-9 都支援 YUV 混合模式。

**優點**

YUV 混合模式有幾個優點，與 VMR 所支援的原始 RGB 混合模式轉譯效能有關：

-   當 VMR 處於 YUV 混合模式時，所有的取消交錯和影片串流組合作業都會以 YUV 色彩空間來執行。 YUV 表面通常需要50% 到60% 的記憶體頻寬，比對等的 RGB 介面還要低。
-   去交錯和資料流程組合是由單一呼叫圖形驅動程式來執行。 此驅動程式可以使用圖形硬體的多重紋理功能，因而節省額外的記憶體頻寬。

雖然任何影片應用程式都可以使用 YUV 混合模式，但主要是用於兩種類型的影片播放應用程式：

1.  顯示隱藏式字幕或 teletext 的電視應用程式。
2.  DVD 應用程式會顯示 DVD 子圖片資料或隱藏式輔助字幕。

**限制**

當 VMR 進入 YUV 混合模式時，會強制執行一些限制：

-   Stream 0 (連接至輸入 Pin 0) 的資料流程可以是漸進式或交錯式;所有其他資料流程都必須是漸進式的。
-   \_不允許串流0使用 GUID Null (編織模式) 。
-   \_因為這可能會使非交錯裝置無法建立，所以無法使用 DeinterlacePref 的編織作為回溯模式。 因為連入的影片不是交錯式的，所以 YUV 混合模式需要經過隔行掃描裝置。
-   與每個 VMR 輸入資料流程相關聯的平面 Alpha 值都不會進行任何變更。
-   使用者無法改變連接的影片資料流程的迭置順序。 預設的 Z 順序是取自釘選順序。
-   不支援色彩加密。
-   輸入 pin 0 必須接收影片串流。
-   其他輸入的 pin 只能接收影片子資料流程資料，例如 DVD 子圖片、隱藏式輔助字幕或 teletext。
-   其他輸入釘選只能接受每圖元的 Alpha YUV 格式，例如 AYUV、AI44 和 IA44。
-   VMR 的輸入圖釘都不能接受任何 RGB 格式。
-   應用程式提供的點陣圖影像在呈現至顯示器之前，無法再與影片合併。
-   您無法使用 VMR 的混音器「輸出矩形」函式，以水準或垂直方式反轉個別的子資料流程。 支援「正常」的資料流程重新置放和調整大小。
-   [**IVMRMixerControl：： SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) 指定的混合背景色彩 (仍是在 rgb 色彩空間中指定，就像在 rgb 混合模式中一樣。

**Configuration**

應用程式必須明確設定 VMR，以利用 YUV 混合模式;原始 RGB 混合模式會維持預設的混合模式。 若要啟用 VMR-7 中的 YUV 混合模式，請使用 MixerPref RenderTargetYUV 旗標來呼叫 [**IVMRMixerControl：： SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) \_ 。 您必須在連接任何 VMR 的輸入圖釘之前進行此呼叫。 若要啟用 VMR-9 中的 YUV 混合模式，請使用 MixerPref9 RenderTargetYUV 旗標來呼叫 [**IVMRMixerControl9：： SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) \_ 。

判斷 VMR-7 是否支援新的 YUV 混合模式的唯一方式，就是嘗試將 VMR 設為該模式。 如果呼叫成功，您仍然可以視需要將 VMR 放回 RGB 混合模式。 在設定為 YUV 混合模式之後，VMR 只能在所有輸入接點都中斷連線之後，變更回 RGB 混合模式。

在 YUV 混合模式中，您可以在 **SetMixingPrefs** 方法中套用下列旗標，以降低圖形處理器 (GPU) 的負載：



| 旗標                                                                                 | 描述                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| VMR-7： MixerPref \_ DynamicSwitchToBOBVMR-9： MixerPref9 \_ DynamicSwitchToBOB<br/> | 切換至 bob 去交錯。                                     |
| VMR-7： MixerPref \_ DynamicDecimateBy2VMR-9： MixerPref \_ DynamicDecimateBy2<br/>  | 以水準和垂直比例刪減影像。 |



 

當篩選圖形正在執行時，您可以新增或移除這些旗標;當 VMR 混音器撰寫下一個影片畫面格時，就會套用變更。 旗標不是互斥的。 這些設定會降低影像的品質，因此通常只有當影片品質較不重要（例如，如果影片是在使用者介面的一小部分中播放）時才適用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VMR 混合模式](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




