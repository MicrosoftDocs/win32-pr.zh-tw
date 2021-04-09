---
description: 本節包含 DXGI 所提供介面的相關資訊。
ms.assetid: b561b26b-961c-4d5e-8483-56b51b989bf7
title: DXGI 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33be25d16998b7bae1f69da0b6d7fd885ab3a514
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935713"
---
# <a name="dxgi-interfaces"></a>DXGI 介面

本節包含 DXGI 所提供介面的相關資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                               | 描述                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDXGIAdapter**](/windows/desktop/api/DXGI/nn-dxgi-idxgiadapter)<br/>                     | [**IDXGIAdapter**](/windows/desktop/api/DXGI/nn-dxgi-idxgiadapter)介面代表顯示子系統 (包括一或多個 Gpu、dac 和影片記憶體) 。 <br/>                                                                                                                            |
| [**IDXGIAdapter1**](/windows/desktop/api/DXGI/nn-dxgi-idxgiadapter1)<br/>                   | [**IDXGIAdapter1**](/windows/desktop/api/DXGI/nn-dxgi-idxgiadapter1)介面代表顯示子系統 (，包括一或多個 GPU 的 dac 和 video 記憶體) 。 <br/>                                                                                                                        |
| [**IDXGIAdapter2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2)<br/>                   | [**IDXGIAdapter2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2)介面代表顯示子系統，其中包含一或多個 Gpu、dac 和 video 記憶體。 <br/>                                                                                                                     |
| [**IDXGIAdapter3**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3)<br/>                   | 此介面會新增一些記憶體常駐方法，以供預算和保留實體記憶體。<br/>                                                                                                                                                                    |
| [**IDXGIAdapter4**](/windows/desktop/api/DXGI1_6/nn-dxgi1_6-idxgiadapter4)<br/>                   | 此介面代表顯示子系統，並擴充此系列的介面，以公開方法來檢查介面卡與任意程式碼防護的相容性 (ACG) 。<br/>                                                                                   |
| [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug)<br/>                         | 這個介面會控制偵錯工具設定，而且只有在開啟 debug 圖層時才能使用。<br/>                                                                                                                                                                      |
| [**IDXGIDebug1**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug1)<br/>                       | 控制 Microsoft DirectX Graphic Infrastructure (DXGI) 的偵錯工具設定。 您可以在 Windows Store 應用程式中使用 [**IDXGIDebug1**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug1) 介面。 <br/>                                                                                                 |
| [**IDXGIDecodeSwapChain**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain)<br/>     | 代表桌面媒體應用程式用來解碼影片資料並顯示在 [DirectComposition](/windows/desktop/directcomp/reference) 介面上的交換鏈。 <br/>                                                                                                               |
| [**IDXGIDevice**](/windows/desktop/api/DXGI/nn-dxgi-idxgidevice)<br/>                       | [**IDXGIDevice**](/windows/desktop/api/DXGI/nn-dxgi-idxgidevice)介面會針對產生影像資料的 DXGI 物件，執行衍生類別。 <br/>                                                                                                                                              |
| [**IDXGIDevice1**](/windows/desktop/api/DXGI/nn-dxgi-idxgidevice1)<br/>                     | [**IDXGIDevice1**](/windows/desktop/api/DXGI/nn-dxgi-idxgidevice1)介面會針對產生影像資料的 DXGI 物件，執行衍生類別。 <br/>                                                                                                                                            |
| [**IDXGIDevice2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgidevice2)<br/>                     | [**IDXGIDevice2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgidevice2)介面會為產生影像資料的 DXGI 物件，實作為衍生類別。 介面會公開方法，以封鎖 CPU 處理，直到 GPU 完成處理，並提供資源給作業系統。 <br/> |
| [**IDXGIDevice3**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgidevice3)<br/>                     | [**IDXGIDevice3**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgidevice3)介面會為產生影像資料的 DXGI 物件，實作為衍生類別。 介面會公開方法，以修剪 DXGI 裝置的圖形記憶體使用量。 <br/>                                                          |
| [**IDXGIDevice4**](/windows/desktop/api/dxgi1_5/nn-dxgi1_5-idxgidevice4)<br/>                     | 此介面提供提供和回收資源的更新方法。<br/>                                                                                                                                                                                            |
| [**IDXGIDeviceSubObject**](/windows/desktop/api/DXGI/nn-dxgi-idxgidevicesubobject)<br/>     | 繼承自系結至裝置的物件，使其可以取出指標。<br/>                                                                                                                                                                      |
| [**IDXGIDisplayControl**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgidisplaycontrol)<br/>       | [**IDXGIDisplayControl**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgidisplaycontrol)介面會公開方法，以指出作業系統 stereoscopic 3d 顯示行為的使用者喜好設定，以及將 stereoscopic 3d 顯示狀態設定為 [啟用] 或 [停用]。 <br/>                          |
| [**IDXGIFactory**](/windows/desktop/api/DXGI/nn-dxgi-idxgifactory)<br/>                     | [**IDXGIFactory**](/windows/desktop/api/DXGI/nn-dxgi-idxgifactory)介面會將用來產生 DXGI 物件的方法， (處理全螢幕轉換) 。 <br/>                                                                                                                          |
| [**IDXGIFactory1**](/windows/desktop/api/DXGI/nn-dxgi-idxgifactory1)<br/>                   | [**IDXGIFactory1**](/windows/desktop/api/DXGI/nn-dxgi-idxgifactory1)介面會實行產生 DXGI 物件的方法。<br/>                                                                                                                                                               |
| [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2)<br/>                   | [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2)介面包含的方法可建立比 [**IDXGISwapChain**](/windows/desktop/api/DXGI/nn-dxgi-idxgiswapchain)更多功能的較新版本交換鏈，並監視 stereoscopic 3d 功能。 <br/>                                          |
| [**IDXGIFactory3**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)<br/>                   | 啟用建立 DXGI 物件。 <br/>                                                                                                                                                                                                                                    |
| [**IDXGIFactory4**](/windows/desktop/api/DXGI1_4/nn-dxgi1_4-idxgifactory4)<br/>                   | 啟用建立 DXGI 物件。 <br/>                                                                                                                                                                                                                                    |
| [**IDXGIFactory5**](/windows/desktop/api/DXGI1_5/nn-dxgi1_5-idxgifactory5)<br/>                   | 此介面可讓單一方法支援變數重新整理率的顯示。<br/>                                                                                                                                                                                  |
| [**IDXGIFactory6**](/windows/desktop/api/dxgi1_6/nn-dxgi1_6-idxgifactory6)<br/>                   | 此介面可讓單一方法根據指定的 GPU 喜好設定來列舉圖形介面卡。<br/>                                                                                                                                                          |
| [**IDXGIFactoryMedia**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgifactorymedia)<br/>           | 為桌面媒體應用程式建立交換鏈，以使用 [DirectComposition](/windows/desktop/directcomp/reference) 表面來解碼和顯示影片。 <br/>                                                                                                                               |
| [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)<br/>                 | 這個介面會控制 debug 資訊佇列，而且只有在開啟 debug 圖層時才能使用。<br/>                                                                                                                                                         |
| [**IDXGIKeyedMutex**](/windows/desktop/api/DXGI/nn-dxgi-idxgikeyedmutex)<br/>               | 代表索引 mutex，允許對多個裝置使用的共用資源進行獨佔存取。<br/>                                                                                                                                                     |
| [**IDXGIObject**](/windows/desktop/api/DXGI/nn-dxgi-idxgiobject)<br/>                       | [**IDXGIObject**](/windows/desktop/api/DXGI/nn-dxgi-idxgiobject)介面是所有 DXGI 物件的基底介面;**IDXGIObject** 支援將呼叫端定義的 (私用資料) 與物件建立關聯，並將介面抓取至父物件。 <br/>                                   |
| [**IDXGIOutput**](/windows/desktop/api/DXGI/nn-dxgi-idxgioutput)<br/>                       | [**IDXGIOutput**](/windows/desktop/api/DXGI/nn-dxgi-idxgioutput)介面代表 (的介面卡輸出，例如監視器) 。<br/>                                                                                                                                                                  |
| [**IDXGIOutput1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutput1)<br/>                     | [**IDXGIOutput1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutput1)介面代表 (的介面卡輸出，例如監視器) 。<br/>                                                                                                                                                                |
| [**IDXGIOutput2**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgioutput2)<br/>                     | 表示介面卡輸出 (例如監視器) 。 [**IDXGIOutput2**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgioutput2)介面會公開方法，以檢查主要輸出介面卡上的 multiplane 重迭支援。<br/>                                                                       |
| [**IDXGIOutput3**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgioutput3)<br/>                     | 表示介面卡輸出 (例如監視器) 。 [**IDXGIOutput3**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgioutput3)介面會公開一個方法來檢查是否有重迭的支援。<br/>                                                                                                                |
| [**IDXGIOutput4**](/windows/desktop/api/DXGI1_4/nn-dxgi1_4-idxgioutput4)<br/>                     | 表示介面卡輸出 (例如監視器) 。 [**IDXGIOutput4**](/windows/desktop/api/DXGI1_4/nn-dxgi1_4-idxgioutput4)介面會公開方法，以檢查是否有重迭的色彩空間支援。<br/>                                                                                                    |
| [**IDXGIOutput5**](/windows/desktop/api/DXGI1_5/nn-dxgi1_5-idxgioutput5)<br/>                     | 表示介面卡輸出 (例如監視器) 。 [**IDXGIOutput5**](/windows/desktop/api/DXGI1_5/nn-dxgi1_5-idxgioutput5)介面會公開單一方法，以指定適用于全螢幕表面的支援格式清單。<br/>                                                                       |
| [**IDXGIOutput6**](/windows/desktop/api/DXGI1_6/nn-dxgi1_6-idxgioutput6)<br/>                     | 表示介面卡輸出 (例如監視器) 。 [**IDXGIOutput6**](/windows/desktop/api/DXGI1_6/nn-dxgi1_6-idxgioutput6)介面會公開方法，以提供特定的監視器功能。<br/>                                                                                                     |
| [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication)<br/> | [**IDXGIOutputDuplication**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication)介面會存取並操作重複的桌面映射。 <br/>                                                                                                                                     |
| [**IDXGIResource**](/windows/desktop/api/DXGI/nn-dxgi-idxgiresource)<br/>                   | [**IDXGIResource**](/windows/desktop/api/DXGI/nn-dxgi-idxgiresource)介面允許資源分享，並識別資源所在的記憶體。 <br/>                                                                                                                                 |
| [**IDXGIResource1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiresource1)<br/>                 | [**IDXGIResource1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiresource1)介面會藉由新增建立 subresource 介面物件的支援，以及建立共用資源的控制碼，來擴充 [**IDXGIResource**](/windows/desktop/api/DXGI/nn-dxgi-idxgiresource)介面。 <br/>                                    |
| [**IDXGISurface**](/windows/desktop/api/DXGI/nn-dxgi-idxgisurface)<br/>                     | [**IDXGISurface**](/windows/desktop/api/DXGI/nn-dxgi-idxgisurface)介面會為影像資料物件實作為方法。<br/>                                                                                                                                                                      |
| [**IDXGISurface1**](/windows/desktop/api/DXGI/nn-dxgi-idxgisurface1)<br/>                   | [**IDXGISurface1**](/windows/desktop/api/DXGI/nn-dxgi-idxgisurface1)介面會將使用 Windows 圖形裝置介面 (GDI) 的支援轉譯成 DXGI 介面，藉此擴充 [**IDXGISurface**](/windows/desktop/api/DXGI/nn-dxgi-idxgisurface) 。<br/>                                                             |
| [**IDXGISurface2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgisurface2)<br/>                   | [**IDXGISurface2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgisurface2)介面會藉由新增 subresource 介面的支援並取得共用資源的控制碼，來擴充 [**IDXGISurface1**](/windows/desktop/api/DXGI/nn-dxgi-idxgisurface1)介面。<br/>                                                            |
| [**IDXGISwapChain**](/windows/desktop/api/DXGI/nn-dxgi-idxgiswapchain)<br/>                 | [**IDXGISwapChain**](/windows/desktop/api/DXGI/nn-dxgi-idxgiswapchain)介面會先執行一個或 [**多個**](/windows/desktop/api/DXGI/nn-dxgi-idxgisurface)介面，以儲存轉譯的資料，然後再呈現給輸出。<br/>                                                                                         |
| [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1)<br/>               | 提供從 [**IDXGISwapChain**](/windows/desktop/api/DXGI/nn-dxgi-idxgiswapchain)增強的呈現功能。 這些呈現功能是由指定中途矩形和滾動矩形來優化簡報所組成。<br/>                                      |
| [**IDXGISwapChain2**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2)<br/>               | 使用方法擴充 [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1) ，以支援交換後緩衝區調整和較低延遲的交換鏈。<br/>                                                                                                                                 |
| [**IDXGISwapChain3**](/windows/desktop/api/DXGI1_4/nn-dxgi1_4-idxgiswapchain3)<br/>               | 使用方法擴充 [**IDXGISwapChain2**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2) ，以支援取得交換鏈目前背景緩衝區的索引和色彩空間的支援。<br/>                                                                                                  |
| [**IDXGISwapChain4**](/windows/desktop/api/dxgi1_5/nn-dxgi1_5-idxgiswapchain4)<br/>               | 此介面會公開用於設定影片中繼資料的單一方法。<br/>                                                                                                                                                                                                 |
| [**IDXGISwapChainMedia**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchainmedia)<br/>       | 此交換連結口可讓桌面媒體應用程式要求順暢變更特定的重新整理頻率。<br/>                                                                                                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DXGI 參考](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

