---
description: 本主題說明如何撰寫媒體基礎轉換 (MFT) ，作為硬體編碼器、解碼器或數位訊號處理器 (DSP) 的 proxy。
ms.assetid: 9922d403-5d0d-433f-ad9f-c86142ac0f46
title: 硬體 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5ce05b4fdad6040b51f66f543c1737fc3918d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191710"
---
# <a name="hardware-mfts"></a>硬體 MFTs

> [!Note]  
> 本主題適用于 Windows 7 或更新版本。

 

本主題說明如何撰寫媒體基礎轉換 (MFT) ，作為硬體編碼器、解碼器或數位訊號處理器 (DSP) 的 proxy。

> [!IMPORTANT]
> 如果硬體編解碼器使用 AVStream 多媒體類別驅動程式，則不需要自訂的 MFT。 媒體基礎為此用途提供 AVStream proxy。 本主題中的資訊僅適用于硬體編解碼器未使用 AVStream 的特殊情況。 如需詳細資訊，請參閱 [AVStream 中的硬體編解碼器支援](https://msdn.microsoft.com/library/dd568169.aspx)。

 

本主題包含下列幾節：

-   [簡介](#introduction)
-   [硬體 MFT 屬性](#hardware-mft-attributes)
-   [硬體交握順序](#hardware-handshake-sequence)
-   [資料處理](#data-processing)
-   [配對的解碼器/編碼器](#paired-decoderencoder)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

任何不是以 AVStream 為基礎的硬體編解碼器都必須提供自己的 MFT 作為驅動程式的 proxy。 硬體編解碼器可能包含數個不同的功能區塊：

-   編碼器
-   解碼器
-   框架縮放/格式轉換

這些函式都應該由個別的 MFT 管理。 硬體 MFT 絕對不能做為多用途的「轉碼程式」。 相反地，請將編碼函式放入編碼器 MFT，然後將函式解碼成解碼器 MFT。 如果硬體提供畫面縮放和格式轉換，請將這些函式放在個別的視頻處理器中，並在 [ **MFT \_ 類別的 \_ 視頻 \_ 處理器** ] 類別中註冊。 如果硬體不支援框架縮放或格式轉換，媒體基礎提供軟體視頻處理器。

硬體 MFTs 具有下列一般需求：

-   硬體 MFTs 必須使用新的非同步處理模型，如 [非同步 MFTs](asynchronous-mfts.md)中所述。
-   硬體 MFTs 必須支援動態格式變更，如 [動態格式變更](basic-mft-processing-model.md)中所述。

## <a name="hardware-mft-attributes"></a>硬體 MFT 屬性

硬體 MFT 必須執行下列與屬性相關的方法：

-   [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)：傳回全域 MFT 屬性的屬性存放區。
-   [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes)：傳回輸入資料流程的屬性存放區。
-   [**IMFTransform：： GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes)：傳回輸出資料流程的屬性存放區。

第一次建立 MFT 時，它必須在自己的全域屬性存放區上設定下列屬性 (也就是 [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)) 所傳回的屬性存放區。



| 屬性                                                                                    | 描述                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ 轉換 \_ 非同步](mf-transform-async.md)                                               | 必須設定為 **TRUE**。 指出 MFT 會執行非同步處理。                                                                                                      |
| [MFT \_ 列舉 \_ 硬體 \_ URL \_ 屬性](mft-enum-hardware-url-attribute.md)                   | 包含硬體裝置的符號連結。<br/> 拓撲載入器會使用此屬性的存在，來測試 MFT 是否代表硬體裝置。<br/> |
| [**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md) | 必須設定為 **TRUE**。 指出此 MFT 支援動態格式變更。                                                                                                       |



 

## <a name="hardware-handshake-sequence"></a>硬體交握順序

如果兩個 MFTs 代表相同的實體裝置，則它們可以交換硬體內的資料（例如，透過硬體匯流排）。 不需要將資料複製到系統記憶體中，然後再複製到裝置上。

在下圖中，標示為 "A" 和 "B" 的 MFTs 代表相同硬體內的功能區塊。 例如，在轉碼案例中，「A」可能代表硬體解碼，而「B」可能代表硬體編碼器。 "A" 和 "B" 之間的資料流程發生于硬體內。 標示為 "C" 的 MFT 是軟體 MFT。 從 "B" 到 "C" 的資料流程會使用系統記憶體。

![圖表顯示標示為 a 到 c 的方塊，以及硬體編解碼器：指向 b 和編解碼器的點、編解碼器指向 b，而 b 指向 c](images/proxy-mft.png)

若要建立硬體連線，這兩個硬體 MFTs 必須使用私用通道。 此連接是在格式協商期間建立，在設定媒體類型之前，以及在第一次呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)之前建立。 連接程式的運作方式如下：

1.  拓撲載入器會檢查兩個 MFTs 是否有 [MFT \_ 列舉 \_ 硬體 \_ URL \_ 屬性](mft-enum-hardware-url-attribute.md) 屬性。 請注意，它不會檢查這個屬性的值。
2.  如果兩個 MFTs 都有 [MFT \_ 列舉 \_ 硬體 \_ URL \_ 屬性](mft-enum-hardware-url-attribute.md) ，拓撲載入器會執行下列動作：
    1.  拓撲載入器會在上游 MFT 上呼叫 [**IMFTransform：： GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) () 。 這個方法會傳回 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。 讓此指標以 *pUpstream* 表示。
    2.  拓撲載入器會在下游 MFT (B) 上呼叫 [**IMFTransform：： GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) 。 此呼叫也會傳回 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。 讓此指標以 *pDownstream* 表示。
    3.  拓撲載入器會藉由呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)，在 *PDownstream* 上設定 [MFT \_ 連線 \_ 資料流程 \_ 屬性](mft-connected-stream-attribute.md)屬性。 屬性的值是 *pUpstream* 指標。
    4.  拓撲載入器會在 *pDownstream* 和 *pUpstream* 上將 [ \_ 連接 \_ 至 \_ HW \_ STREAM](mft-connected-to-hw-stream.md)屬性的 MFT 設定為 **TRUE** 。
3.  此時，下游 MFT 具有上游 MFT 屬性存放區的指標，如下圖所示。

    ![每個 mfts 指向其資料流程、指向其存放區的每個資料流程，以及輸出存放區中有虛線的輸入存放區的圖表](images/proxy-mft2.png)

    > [!Note]  
    > 為了清楚起見，此圖表會將資料流程和屬性存放區顯示為不同的物件，但不需要執行這項工作。

     

4.  下游 MFT 會使用 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標來建立與上游 mft 之間的私人通道。 因為通道是私用的，所以確切的機制是由實作為定義。 例如，MFT 可能會查詢私用 COM 介面。

在步驟4中，下游 MFT 必須確認兩個 MFTs 是否共用相同的實體裝置。 如果沒有，則必須切換回使用系統記憶體進行資料傳輸。 這可讓 MFT 在軟體 MFTs 和其他硬體裝置上正確運作。

如果交握成功，而且兩個 MFTs 共用私用資料通道，則不會使用標準資料處理模型 (下一節) 在連接點中所述。 具體而言，下游 MFT 不會傳送 [METransformNeedInput](metransformneedinput.md) 事件;如需詳細資訊，請參閱本主題的下一節。

## <a name="data-processing"></a>資料處理

當硬體 MFT 使用系統記憶體進行資料傳輸時，此程式的運作方式如下：

1.  為了要求更多輸入，MFT 會傳送 [METransformNeedInput](metransformneedinput.md) 事件。
2.  [METransformNeedInput](metransformneedinput.md)事件會導致管線呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)。
3.  當 MFT 有輸出資料時，MFT 會傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件。
4.  [METransformHaveOutput](metransformhaveoutput.md)事件會導致管線呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。

如需詳細資訊，請參閱 [非同步 MFTs](asynchronous-mfts.md)。

但是，如果 MFT 使用硬體通道，它就不會在硬體連接點傳送這些事件，因為所有資料傳輸都是在硬體內部發生。 因此，管線不會在連接點呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 或 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。

例如，請考慮本主題中的第一個圖表。 在此設定中，資料處理會如下所示：

1.  「A」會傳送 [METransformNeedInput](metransformneedinput.md) 來要求資料。
2.  管線會在 "A" 上呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 。
3.  "A" 和 "B" 處理硬體中的資料。
4.  當處理完成時，"B" 會傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件。
5.  管線會在 "B" 上呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 。

## <a name="paired-decoderencoder"></a>配對的解碼器/編碼器

如果解碼器和編碼器都位於相同的硬體晶片上，則在轉碼時最好將它們一起使用。 也就是說，選取其中一個應該會導致在轉碼管線中選取另一個。 為了確保已選擇相符的硬體編解碼器，這兩個編解碼器 MFTs 應該提供自訂媒體類型。 若要建立自訂媒體類型：

-   視需要將 [ [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) ] 屬性設定為 **MFMediaType \_ 音訊** 或 **MFMediaType \_ 影片**。
-   將 [ [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) ] 屬性設定為自訂 GUID 值。

其他類型屬性是選擇性的。 此解碼器會從其 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)傳回自訂類型，而編碼器會從其 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) 方法傳回自訂類型。 在這兩種情況下，自訂類型都必須是清單中的第一個專案 (*dwTypeIndex* = 0) 。

若要使用軟體編解碼器，編解碼器應該也會傳回至少一個標準格式，例如影片的 NV12。 標準格式應出現在自訂類型 (*dwTypeIndex* > 0) 之後。 如果這兩個編解碼器必須永遠配對且無法與軟體編解碼器交互操作，則 MFTs 只會傳回自訂格式，而不會傳回任何標準格式。

> [!Note]  
> 如果解碼器沒有傳回任何標準格式，它就無法用於使用 [增強型影片](enhanced-video-renderer.md)轉譯器進行播放。 在此情況下，它應該註冊為僅限轉碼的解碼器。 請參閱 [僅限轉碼的解碼器](implementing-a-codec-mft.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫自訂的 MFT](writing-a-custom-mft.md)
</dt> <dt>

[執行編解碼器 MFT](implementing-a-codec-mft.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 




