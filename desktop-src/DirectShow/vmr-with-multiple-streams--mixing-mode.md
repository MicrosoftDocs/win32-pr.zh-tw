---
description: '具有多個資料流程 (混合模式的 VMR) '
ms.assetid: 053edb70-8631-4fe4-a137-2fe54e02ab9e
title: '具有多個資料流程 (混合模式的 VMR) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21a954b0ad78afbceabf0fde493f920961b90dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984587"
---
# <a name="vmr-with-multiple-streams-mixing-mode"></a>具有多個資料流程 (混合模式的 VMR) 

VMR 可以呈現多個輸入資料流程。 在此設定中，稱為混合模式，VMR 會載入其混音器和組合器，以在轉譯之前執行混合和混合。 當 VMR 處於視窗模式或無視窗模式時，可以使用混合模式。

混合模式需要圖形驅動程式支援 DDCAPS \_ BLTFOURCC 和 DDCAPS \_ BLTSTRETCH 功能旗標 (色彩空間轉換和延展 blitting，分別) 。 幾乎所有新的圖形驅動程式都具有這些功能。 此外，驅動程式必須支援為目前的顯示圖元深度建立 Direct3D 轉譯目標。 當顯示器設為每圖元24位時，某些裝置不支援 Direct3D 作業。 如需詳細資訊，請參閱 DirectX 圖形 SDK 檔。

> [!Note]  
> 當 VMR 混合多個影片串流時，不會正確搜尋篩選圖形。 如果您需要搜尋多個影片串流，您必須建立個別的篩選圖形，以共用相同的自訂配置器呈現者物件。

 

**針對多個資料流程設定 VMR-7**

若要使用 VMR-7 轉譯多個輸入資料流程，請執行下列動作：

1.  在連接任何 VMR 的輸入圖釘之前，請以資料流程的數目呼叫 [**IVMRFilterConfig：： SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) 方法。 這會導致 VMR 載入混音器和組合器，並建立指定數目的輸入圖釘。
2.  呼叫 [**IVMRFilterConfig：： SetRenderingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) 來指定各種轉譯喜好設定。
3.  將釘選到上游篩選器。 最簡單的方法是針對每個輸入資料流程呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 。 如果上游篩選器上的輸出 pin (通常是) 的解碼器，而且 VMR 上的輸入 pin 不能同意連接，則會建立具有預設設定的 VMR 實例。 這會導致標題列中有 "ActiveMovie" 的新視窗。 為了避免發生這種情況，應用程式應該一律透過呼叫方法（例如 [**IPin：： ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto)）來確認 VMR 的正確實例正在使用中。 另一個選項是新增來源篩選器，然後使用 **IGraphBuilder：： connect** 連接 pin。
4.  使用 VMR 上的 [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) 介面來控制每個資料流程的參數，例如 Alpha 值、Z 順序和輸出矩形。
5.  執行篩選圖形。

**針對多個資料流程設定 VMR-9**

根據預設，VMR-9 會建立四個輸入圖釘。 如果您想要混合四個以上的影片串流，請先呼叫 [**IVMRFilterConfig9：： SetNumberOfStreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) ，然後再連接任何輸入 pin。 您可以使用 [**IVMRMixerControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) 介面來設定資料流程參數，例如 Alpha、Z 順序和位置。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VMR 混合模式](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



