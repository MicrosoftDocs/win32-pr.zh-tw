---
description: 本主題說明媒體基礎轉換 (MFT) 應該如何處理串流期間的格式變更。
ms.assetid: b0a94760-b4dd-4e50-a5ce-a1f674dde156
title: 處理資料流程變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2adf3cbc0504a37fe611b77047c73f85b9d1e742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191711"
---
# <a name="handling-stream-changes"></a>處理資料流程變更

本主題說明媒體基礎轉換 (MFT) 應該如何處理串流期間的格式變更。

> [!IMPORTANT]
>
> 本主題不適用於編碼器。 編碼器不應傳播格式變更，如本主題中所述。 編碼器應該只接受符合目前設定之輸出類型的輸入類型。

 

## <a name="overview-of-format-changes"></a>格式變更總覽

一般來說，在串流處理期間可能會變更格式的兩個原因。

-   用戶端可能會切換至具有新格式的資料流程。 例如，在數位電視中，這可能是因為通道變更所造成。
-   在某些影片格式（例如 h.264）中，位流可以指示格式變更。 這類變更可能包括欄位支配、視頻解析度或圖元外觀比例的變更。

如果編碼類型變更，用戶端可能需要從管線中移除 MFT，並將它取代為另一個 MFT。  (例如，用戶端可能需要換成新的解碼器。 ) 本主題未涵蓋這種情況。 本主題僅涵蓋目前的 MFT 可以處理新格式的情況。

如果格式有所變更，則 MFT 可能需要新的輸入類型、新的輸出類型或兩者。

-   輸入類型的變更是由用戶端所起始。 MFT 絕不會變更自己的輸入類型。
-   對輸出類型所做的變更是由 MFT 所起始。 MFT 表示它需要新的輸出類型，而且用戶端會以 MFT 協商新的輸出類型。

因此，可能有三種不同的案例：

-   用戶端會設定新的輸入類型。 MFT 會取用新的格式，而不會變更其輸出類型。
-   用戶端會設定新的輸入型別，而這會觸發輸出型別中的變更。
-   輸入類型不會變更，但 MFT 會偵測到位流中的格式變更，這需要新的輸出類型。

## <a name="implementing-format-changes"></a>執行格式變更

本主題的其餘部分將說明用戶端應該如何處理格式變更，以及如何在 MFT 中執行格式變更。

### <a name="output-type"></a>輸出類型

任何 MFT 都可以起始其輸出類型的變更，如下所示：

1.  用戶端會呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。 MFT 會以下列方式回應：
    1.  MFT 不會在 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)中產生輸出範例。
    2.  MFT 會在 [**mft \_ 輸出 \_ 資料 \_ 緩衝區**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer)結構的 **dwStatus** 成員中設定 **mft \_ 輸出 \_ 資料 \_ 緩衝區 \_ 格式 \_ 變更** 旗標。
    3.  [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)方法會傳回錯誤碼 **MF \_ E \_ 轉換 \_ 資料流程 \_ 變更**。
2.  用戶端會呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)。 這個方法會傳回一組更新的輸出類型。
3.  用戶端會呼叫 [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定新的輸出類型。
4.  用戶端會繼續呼叫 [**ProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) / [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。

### <a name="input-type"></a>輸入類型

輸入類型的變更是由用戶端所起始，而不是由 MFT 所起始。 如果輸入類型變更，它可能會觸發輸出類型的變更。

確切的事件順序取決於 [**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md) 屬性的值。



| 值     | 描述                                                     |
|-----------|-----------------------------------------------------------------|
| **FALSE** | 在用戶端設定新的輸入類型之前，必須先清空 MFT。 |
| **TRUE**  | 用戶端可以設定新的輸入類型，而不需要清空 MFT。   |



 

MFT 會透過其 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法來公開這個屬性。 這個屬性的預設值為 **FALSE**;如果 MFT 未設定此屬性，請將值視為 **FALSE**。

**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更為 FALSE**

1.  用戶端傳送 [**MFT \_ 訊息 \_ 命令 \_ 清空**](mft-message-command-drain.md) 訊息。
2.  用戶端會藉由呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 來清空 MFT，直到 **ProcessOutput** 傳回 **MF \_ E \_ 轉換 \_ 需要 \_ 更多 \_ 輸入**。
3.  用戶端會呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 來設定新的輸入類型。
4.  MFT 會驗證輸入類型。 如果類型無效， [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 會傳回 **MF \_ E \_ INVALIDMEDIATYPE** 或其他錯誤碼。 否則， **SetInputType** 會傳回 S \_ OK。
5.  假設輸入類型有效，則 MFT 會評估輸出類型是否也會變更。 如果不是，則資料流程會繼續進行，不需要採取任何進一步的動作。
6.  如果輸出類型變更：
    1.  MFT 會使其目前的輸出媒體類型失效，並更新可用輸出媒體類型的清單。
    2.  [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)的下一個呼叫會傳回 **MF \_ E \_ 轉換 \_ 資料流程 \_ 變更**，如上一節中所述。
    3.  用戶端會呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 來取得更新的輸出類型清單。
    4.  用戶端會呼叫 [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)。

**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更為 TRUE**

1.  用戶端會呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 來設定新的輸入類型。
2.  MFT 會驗證輸入類型。 如果類型無效， [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 會傳回 **MF \_ E \_ INVALIDMEDIATYPE** 或其他錯誤碼。 否則， **SetInputType** 會傳回 S \_ OK。
3.  假設輸入類型有效，則 MFT 會評估輸出類型是否也會變更。 如果不是，則資料流程會繼續進行，不需要採取任何進一步的動作。
4.  在輸出類型變更之前，MFT 必須處理任何快取的輸入範例，如下所示：
    1.  MFT 不會使其目前的輸出類型無效。
    2.  從快取的輸入範例中，MFT 產生的輸出越多。
    3.  無論是在處理快取的範例時，MFT 是否接受新的輸入範例都是選擇性的。 如果是，新的輸入範例將會使用新的輸入格式，因此 MFT 必須在格式變更時追蹤點。
5.  在 MFT 處理輸入類型變更之前所收到的所有範例之後， [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 會傳回 **MF \_ E \_ 轉換 \_ 資料流程 \_ 變更**。
6.  MFT 會使其目前的輸出類型失效，並更新可用輸出媒體類型的清單。
7.  如先前所述，用戶端會協商新的輸出類型。

針對 [**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md)屬性，[非同步 MFTs](asynchronous-mfts.md)必須傳回 **TRUE** 值。 使用非同步 MFT 時，用戶端可以假設 [ **MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更** ] 屬性設定為 [ **TRUE**]。

當 [**MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md) 為 **TRUE** 時，主要的差異在於，用戶端不需要在設定新的輸入類型之前清空 MFT。 因此，當 MFT 在輸入範例上時，輸入類型可能會變更。 請務必不要只卸載這些範例。 此外，在 MFT 處理其所有快取的資料之前，輸出類型無法變更。

先前的段落特別適用于影片解碼器，它可以從時態順序接收程式碼框架，因此需要加以快取。 如果 MFT 未快取輸入範例，則清空其實是無作業。 在此情況下，MFT 可以將 [**(\_ \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md) 為 **FALSE** ，或將屬性保留為未設定) 。

此外，請注意，在清空之後，每個 MFT 都應該正確地處理格式變更。 [**Mft \_ 支援 \_ 動態 \_ 格式 \_ 變更**](mft-support-dynamic-format-change-attribute.md)屬性指出 mft 是否支援格式變更，而不需要清空。

## <a name="change-in-interlace-mode"></a>以交錯模式變更

影片交錯模式中的變更是特殊案例，因為它們不會使目前的媒體類型無效。 相反地，您可以藉由設定媒體範例上的屬性，為每個影片框架指定交錯模式。 影片 MFT 應檢查每個輸入範例是否有這些旗標。

當欄位支配從最上層欄位切換至底部欄位，或影片在漸進式和交錯式圖片之間切換時，交錯模式可能會變更。

如需詳細資訊，請參閱 [在範例上交錯旗標](video-interlacing.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫自訂的 MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



