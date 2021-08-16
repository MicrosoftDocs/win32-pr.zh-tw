---
description: 查看隱藏式輔助字幕
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: 查看隱藏式輔助字幕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f52288b1c4fa5c43f7e0419d81bd9727a4db86848d368b600e1d713c53dc1593
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903424"
---
# <a name="viewing-closed-captions"></a>查看隱藏式輔助字幕

為了支援類比電視中的隱藏式輔助字幕，「捕捉」篩選器會公開提供 VBI 或隱藏式輔助字幕資料的 pin。 Pin 會有下列其中一個 pin 類別：

-   VBI pin (釘選 \_ 類別 \_ VBI) 。 傳遞 VBI 波形範例的資料流程。 這些會傳遞至解碼篩選器，以解壓縮隱藏式輔助字幕資料。
-   CC pin (釘 \_ 選 \_ cc) 。 傳遞已關閉的標題位元組組（從第21行資料解壓縮）。
-   硬體切割 CC pin (PINNAME \_ 影片 \_ 副本 \_) 。

若要預覽隱藏式輔助字幕，請使用 VBI 釘選類別來呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，如果失敗，請使用 CC 類別再次呼叫它。


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



下圖顯示用來顯示隱藏式輔助字幕的一般篩選圖形。

![隱藏式輔助字幕預覽圖形](images/vidcap08.png)

此圖表會使用下列篩選器來顯示隱藏式輔助字幕：

-   [T/接收到接收的轉換器](tee-sink-to-sink-converter.md)。 接受 capture 篩選器中的 VBI 資訊，並將其分割為信號上的每個資料服務的個別資料流程。 Microsoft 針對隱藏式標題、NABTS 和全球標準 Teletext 提供 VBI 編解碼器 (WST) 。
-   [CC 解碼器](cc-decoder-filter.md)。 從 capture 篩選器所提供的取樣 VBI 波形中解碼 CC 資料。
-   [第21行的解碼器](line-21-decoder-filter.md)。 轉譯副本的位元組配對，並將標題文字繪製到點陣圖。 下游篩選 (在此案例中，重迭 Mixer) 將點陣圖重迭到影片。

Capture Graph Builder 的 [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法會自動加入這些篩選器。 如果捕捉篩選具有 CC pin，而不是 VBI pin，則副本 pin 會直接連接到第21行的解碼篩選器。

> [!Note]  
> 如果您使用影片混合轉譯器 (VMR) 篩選器進行轉譯，請使用第21行的解碼器篩選器2。 此篩選器的功能與第21行的解碼器相同，但 CLSID 是 CLSID \_ Line21Decoder2。

 

> [!Note]  
> Windows Vista 中已移除 CC 解碼器篩選。 新的應用程式應該使用 VBICodec 篩選器，其記載于 Microsoft 電視技術檔中。

 

如果捕捉裝置使用影片埠，則 capture 篩選器可能會有影片埠 VBI 釘選， (PIN \_ 類別 \_ VIDEOPORT \_ VBI) 。 此 pin 必須連接到 [VBI Surface](vbi-surface-allocator.md) 配置器篩選器，這會配置用來保存所捕捉 VBI 資料的表面。 [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法會在需要時加入此篩選準則。 下圖顯示具有 VBI Surface 配置器的篩選圖形。

![隱藏式輔助字幕預覽圖形與 vbi surface 配置器](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>啟用和停用標題

若要控制字幕顯示，請使用第21行的 [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) 介面。 例如，您可以使用 [**IAMLine21Decoder：： SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) 方法關閉字幕顯示，如下所示：


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



這個範例會使用 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法來尋找 [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) 介面。 要 **FindInterface** 的第一個參數是 **&\_ \_ 僅供下游參考**，這會指定從 capture 篩選器 (*pCap*) 搜尋下游。

### <a name="capturing-closed-caption-bitmaps"></a>捕獲隱藏式輔助字幕點陣圖

您可以將標題點陣圖捕捉到檔案中。 若要這樣做，請新增篩選圖形的檔案寫入區段，如將 [影片捕獲到](capturing-video-to-a-file.md)檔案中所述。 然後，將 CC 或 VBI 釘轉譯至 mux 篩選器：


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



如果您也要捕獲影片，這將會建立具有兩個不同影片串流的檔案。 它不會使用在圖片上方重迭的標題來捕獲影片。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[隱藏式輔助字幕和 Teletext](closed-captions-and-teletext.md)
</dt> </dl>

 

 



