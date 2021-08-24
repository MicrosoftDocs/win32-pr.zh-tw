---
description: 影片埠釘選
ms.assetid: a6be24e5-7937-48f1-abeb-3f29c3deeafd
title: 影片埠釘選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94202e05cc467eabb77719a145a77310a62482e6f82772261b57e5ff544d2b63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696780"
---
# <a name="video-port-pins"></a>影片埠釘選

具有硬體視訊連接埠的 capture 裝置，可能會在 Microsoft® DirectX®中使用 (VPE) 的影片埠擴充功能。 如果是的話，capture 篩選器將會有一個影片埠 (VP) pin。 從 VP 釘選到篩選圖形都沒有影片資料。 相反地，會在硬體中產生影片畫面，並直接傳送至視訊記憶體。 VP pin 允許將控制訊息傳送至硬體。

即使您的應用程式只執行沒有預覽的檔案捕獲，也請務必連接 VP pin 碼。 如果您讓 pin 不連線，圖形將無法正確執行。 這與不需要連線的預覽 pin 不同。

不同的 DirectShow 影片轉譯器提供了 VP 釘選的不同支援：

-   影片轉譯器：在重迭[Mixer](overlay-mixer-filter.md)篩選器上連線 VP 釘選至 pin 0，並將重迭 Mixer 篩選器連線到影片轉譯器。
-   VMR-7：連線 VP 釘選到[影片埠管理員](video-port-manager.md)篩選器，並將影片埠管理員連接到 VMR-7。
-   VMR-9：如果裝置具有 VP 釘選，您就無法使用 VMR-9，因為 Direct3D 9 不支援影片埠。 請使用影片轉譯器或 VMR-7。

針對影片埠案例，建議您在影片埠管理員和 VMR 7 上使用重迭 Mixer 和影片轉譯器，因為並非所有驅動程式都支援影片埠管理員。 一般而言，重迭 Mixer 是影片埠最可靠的選項。

[**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法會自動插入重迭 Mixer 如果有 VP 的 pin。 如果您要在不使用這個方法的情況下建立圖形，您應該檢查 capture 篩選器上是否有影片埠 pin，如果有的話，請將它連接到覆迭 Mixer 篩選器，如下圖所示。

![將影片埠 pin 連接到重迭混音器篩選器。](images/vidcap11.png)

您可以使用 [**ICaptureGraphBuilder2：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) 方法，在 capture 篩選器上搜尋 VP 釘選：


```C++
hr = pBuild->FindPin(
    pCap,                    // Pointer to the capture filter.
    PINDIR_OUTPUT,           // Look for an output pin.
    &PIN_CATEGORY_VIDEOPORT, // Look for a video port pin.
    NULL,                    // Any media type.
    FALSE,                   // Pin can be connected.
    0,                       // Retrieve the first matching pin.
    &pVPPin                  // Receives a pointer to the pin.
);
```



將重迭 Mixer 新增至圖形後，再次呼叫 **FindPin** ，以在重迭 Mixer 上找出 pin 0。 Pin 0 一律是篩選上的第一個輸入 pin。


```C++
pBuild->FindPin(pOvMix, PINDIR_INPUT, NULL, NULL, TRUE, 0, &pOVPin);
```



藉由呼叫 [**IGraphBuilder：：連線**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)連線兩個 pin。


```C++
pGraph->Connect(pVPPin, pOvPin);
```



然後將重迭 Mixer 的輸出釘選到影片轉譯器篩選器。 您可以藉由呼叫 [**IVideoWindow：:p 內容 \_**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow)自動 [**顯示和 IVideoWindow：:p 篩選 Graph 管理員上的 \_ 顯示**](/windows/desktop/api/Control/nf-control-ivideowindow-put_visible)方法，來隱藏影片。

針對 TV 調諧器，capture 篩選器可能也會有影片埠 VBI 釘選 [ \_ \_ VIDEOPORT) VBI] (釘選類別 \_ 。 若是如此，請將該釘選到 [VBI Surface](vbi-surface-allocator.md) 配置器篩選器。 如需詳細資訊，請參閱 [觀看隱藏](viewing-closed-captions.md)式輔助字幕。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Advanced Capture 主題](advanced-capture-topics.md)
</dt> <dt>

[在影片捕獲中使用重迭 Mixer](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



