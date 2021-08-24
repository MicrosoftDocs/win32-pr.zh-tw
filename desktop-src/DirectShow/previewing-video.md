---
description: 此範例會在 DirectShow 中使用 ICaptureGraphBuilder2：： RenderStream 方法來建立影片預覽圖形。
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: '預覽影片 (DirectShow) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92a6fd3f34a6b2678f41f95a80caca64e47adcc62cbeb6c37f2ed7b71f8d947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748281"
---
# <a name="previewing-video-directshow"></a>預覽影片 (DirectShow) 

若要建立影片預覽圖形，請呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法，如下所示：


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



此範例假設下列各項：

-   *pBuild* 已初始化，如 [關於 Capture Graph Builder](about-the-capture-graph-builder.md)中所述。
-   *pCap* 已初始化，方法是建立 capture 篩選器的實例，並將它新增至篩選圖形（如 [選取捕獲裝置](selecting-a-capture-device.md)所述）。

[**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法的第一個參數會指定釘選類別。針對預覽圖形，請使用 **PIN \_ 類別 \_ 預覽**。 第二個參數會將媒體類型指定為主要類型 GUID。 如需影片，請使用 **媒體媒體的 \_ 影片**。 DV 裝置提供交錯的音訊和影片，媒體類型是媒體類型 **的 \_ 交錯**。  (如需 DV capture 的詳細資訊，請參閱[DirectShow 中的數位影片](digital-video-in-directshow.md)) 。

第三個參數是捕獲篩選器 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 介面的指標。 在此範例中，不需要接下來的兩個參數。 它們可用來指定轉譯資料流程時可能需要的其他篩選。 將最後一個參數設定為 **Null** ，會讓 Capture Graph Builder 根據媒體類型選取資料流程的預設轉譯器。 針對影片，Capture Graph Builder 一律會使用[影片](video-renderer-filter.md)轉譯器篩選器作為預設轉譯器。

> [!Note]  
> 在 Windows XP 和更新版本中，雖然混合轉譯器 (VMR) 是 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)方法的預設影片轉譯器，但它並不是 [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法的預設轉譯器。 在任何平臺上，除非您另外指定，否則 Capture Graph Builder 一律會使用舊的影片轉譯器篩選器。

 

雖然 pin 類別是以釘選 **\_ 類別 \_ 預覽** 的形式提供，但篩選準則實際上是否有預覽釘選，但它可以有影片埠 pin 或只是捕捉 pin。 無論是哪一種情況，Capture Graph Builder 都會自動建立正確的圖形。

下圖顯示預覽影片的最簡單圖形。

![影片預覽圖形](images/vidcap01.png)

在此圖中，capture 篩選器具有預覽 pin，可直接連接到影片轉譯器。

如果「capture」篩選器只有一個「捕捉」（capture）釘選，「capture Graph 產生器會插入一個[智慧型](smart-tee-filter.md)指標篩選器，它會將資料流程分割成捕獲資料流程和預覽資料流程。 [結合影片捕獲和預覽](combining-video-capture-and-preview.md)會更詳細地說明這一點。

在某些情況下，影片串流必須經過重迭 Mixer 篩選。 如果是， [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法會自動將它新增至圖形。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[結合影片捕獲和預覽](combining-video-capture-and-preview.md)
</dt> <dt>

[影片捕獲](video-capture.md)
</dt> </dl>

 

 



