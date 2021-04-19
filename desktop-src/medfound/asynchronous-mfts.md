---
description: 本主題說明 (MFTs) 之媒體基礎轉換的非同步資料處理。
ms.assetid: d438ffae-fc50-454f-8ce4-2d6676500fff
title: 非同步 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a16950cf431eff16f2befb382a77910c49ccb2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972362"
---
# <a name="asynchronous-mfts"></a>非同步 MFTs

本主題說明 (MFTs) 之媒體基礎轉換的非同步資料處理。

> [!Note]  
> 本主題適用于 Windows 7 或更新版本。

 

-   [關於非同步 MFTs](#about-asynchronous-mfts)
-   [一般需求](#general-requirements)
-   [事件](#events)
-   [ProcessInput](#processinput)
-   [ProcessOutput](#processoutput)
-   [排水](#draining)
-   [沖洗](#flushing)
-   [標記](#markers)
-   [格式變更](#format-changes)
-   [屬性](#attributes)
-   [解除鎖定非同步 MFTs](#unlocking-asynchronous-mfts)
-   [關閉 MFT](#shutting-down-the-mft)
-   [註冊和列舉](#registration-and-enumeration)
-   [相關主題](#related-topics)

## <a name="about-asynchronous-mfts"></a>關於非同步 MFTs

在 Windows Vista 中引進 MFTs 時，API 是針對 *同步* 資料處理而設計。 在該模型中，MFT 一律是等候取得輸入或等候產生輸出。

請考慮一般的影片解碼。 為了取得已解碼的框架，用戶端會呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。 如果此解碼器有足夠的資料來解碼框架， **ProcessOutput** 會在 MFT 解碼框架時區塊。 否則， **ProcessOutput** 會傳回 **MF_E_TRANSFORM_NEED_MORE_INPUT**，指出用戶端應該呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)。

如果解碼器在一個執行緒上執行所有的解碼作業，此模型就會順利運作。 但假設解碼器使用多個執行緒來平行解碼框架。 為了達到最佳效能，每當解碼執行緒變成閒置時，應該會收到新的輸入。 但是，執行緒完成解碼作業的速率不會與用戶端對 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 和 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)的呼叫完全一致，因而導致執行緒等待工作。

Windows 7 引進 MFTs 的事件驅動、 *非同步* 處理。 在此模型中，每當 MFT 需要輸入或有輸出時，它就會將事件傳送至用戶端。

## <a name="general-requirements"></a>一般需求

本主題說明非同步 MFTs 與同步的 MFT 有何不同。 除了本主題中注明的，這兩個處理模型是相同的。  (特別是，格式協商相同。 ) 

非同步 MFT 必須執行下列介面：

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)

## <a name="events"></a>事件

非同步 MFT 會使用下列事件來表示其資料處理狀態：



| 事件                                                    | 描述                                                       |
|----------------------------------------------------------|-------------------------------------------------------------------|
| [METransformNeedInput](metransformneedinput.md)         | 當 MFT 可以接受更多輸入時傳送。                          |
| [METransformHaveOutput](metransformhaveoutput.md)       | 在 MFT 有輸出時傳送。                                     |
| [METransformDrainComplete](metransformdraincomplete.md) | 清空作業完成時傳送。 請參閱 [清空](#draining)。 |
| [METransformMarker](metransformmarker.md)               | 當標記為「處理中」時傳送。 請參閱 [標記](#markers)。           |



 

這些事件會在頻外傳送。 請務必瞭解 MFT 內容中的頻外和頻外事件之間的差異。

原始的 MFT 設計支援 *內建* 事件。 內建事件包含有關資料流程的資訊，例如格式變更的相關資訊。 用戶端會藉由呼叫 [**IMFTransform：:P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)，將內建事件傳送到 MFT。 MFT 可以在 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 方法中將內建事件傳送回用戶端。  (明確地說，事件是在 [**MFT_OUTPUT_DATA_BUFFER**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_data_buffer)結構的 **pEvents** 成員中傳達。 ) 

MFT 會透過 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面傳送頻外事件，如下所示：

1.  MFT 會實 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面，如 [媒體事件](media-event-generators.md)產生器中所述。
2.  用戶端會在 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)介面的 MFT 上呼叫 **IUnknown：： QueryInterface** 。 非同步 MFT 必須公開這個介面。 同步 MFTs 不應公開這個介面。
3.  用戶端會呼叫 [**IMFMediaEventGenerator：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) 和 [**IMFMediaEventGenerator：： EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) ，以接收來自 MFT 的頻外事件。

## <a name="processinput"></a>ProcessInput

[**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)方法的修改方式如下：

1.  串流處理開始時，用戶端會傳送 [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md) 訊息。
2.  在串流處理期間，MFT 會藉由傳送 [METransformNeedInput](metransformneedinput.md) 事件來要求資料。 事件資料是資料流程識別碼。
3.  針對每個 [METransformNeedInput](metransformneedinput.md) 事件，用戶端會呼叫指定資料流程的 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 。
4.  在串流結束時，用戶端可能會使用 [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md)訊息來呼叫 [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 。

執行附注：

-   在接收 [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md)訊息之前，此 MFT 必須傳送任何 [METransformNeedInput](metransformneedinput.md)事件。
-   在串流處理期間，MFT 可能會在任何時間傳送 [METransformNeedInput](metransformneedinput.md) 事件。
-   此 MFT 應維持暫止 [METransformNeedInput](metransformneedinput.md) 事件的計數。 任何未對應至 METransformNeedInput 事件的 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 呼叫都必須傳回 **MF_E_NOTACCEPTING**。
-   當 MFT 收到 [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md) 訊息時，它會將擱置中 [METransformNeedInput](metransformneedinput.md) 事件的計數重設為零。
-   當 MFT 收到 [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md)訊息之後，就不能傳送任何 [METransformNeedInput](metransformneedinput.md)事件。
-   如果在 [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md)之前或 [**MFT_MESSAGE_NOTIFY_END_OF_STREAM**](mft-message-notify-end-of-stream.md)之後呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ，此方法必須傳回 **MF_E_NOTACCEPTING**。

## <a name="processoutput"></a>ProcessOutput

[**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)方法的修改方式如下：

1.  只要 MFT 有輸出，它就會傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件。
2.  針對每個 [METransformHaveOutput](metransformhaveoutput.md) 事件，用戶端會呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。

執行附注：

-   如果用戶端在任何其他時間呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) ，此方法會傳回 **E_UNEXPECTED**。
-   非同步 MFT 絕對不應該從 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)方法傳回 **MF_E_TRANSFORM_NEED_MORE_INPUT** 。 如果 MFT 需要更多輸入，則會傳送 [METransformNeedInput](metransformneedinput.md) 事件。

## <a name="draining"></a>排水

清空 MFT 會使 MFT 產生的輸出數量，與任何已傳送的輸入資料相同。 清空非同步 MFT 的運作方式如下：

1.  用戶端會傳送 [**MFT_MESSAGE_COMMAND_DRAIN**](mft-message-command-drain.md) 訊息。
2.  MFT 會繼續傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件，直到它沒有其他要處理的資料為止。 它不會在這段時間內傳送 [METransformNeedInput](metransformneedinput.md) 事件。
3.  在 MFT 傳送最後一個 [METransformHaveOutput](metransformhaveoutput.md) 事件之後，它會傳送 [METransformDrainComplete](metransformdraincomplete.md) 事件。

完成清空之後，除非從用戶端收到 [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md)訊息，否則 MFT 不會傳送另一個 [METransformNeedInput](metransformneedinput.md)事件。

## <a name="flushing"></a>沖洗

用戶端可以藉由傳送 [**MFT_MESSAGE_COMMAND_FLUSH**](mft-message-command-flush.md) 訊息來清除 MFT。 MFT 會卸載其所持有的所有輸入和輸出範例。

在接收來自用戶端的 [**MFT_MESSAGE_NOTIFY_START_OF_STREAM**](mft-message-notify-start-of-stream.md)訊息之前，不會傳送另一個 [METransformNeedInput](metransformneedinput.md)事件。

## <a name="markers"></a>標記

用戶端可以藉由傳送 [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) 訊息來標記資料流程中的某個點。 MFT 會以下列方式回應：

1.  MFT 會從現有的輸入資料產生任意數量的輸出範例，並為每個輸出範例傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件。
2.  產生所有輸出之後，MFT 會傳送 [METransformMarker](metransformmarker.md) 事件。 此事件必須在所有 [METransformHaveOutput](metransformhaveoutput.md) 事件之後傳送。

例如，假設某個解碼器有足夠的輸入資料來產生四個輸出範例。 如果用戶端傳送 [**MFT_MESSAGE_COMMAND_MARKER**](mft-message-command-marker.md) 訊息，則此 MFT 會將四個 [METransformHaveOutput](metransformhaveoutput.md) 事件排在佇列中，每個輸出範例 (一個) ，然後是 [METransformMarker](metransformmarker.md) 事件。

標記訊息類似于清空訊息。 不過，清空會視為資料流程中的中斷，而標記則不會。 清空和標記具有下列差異。

排水：

-   在清空時，MFT 不會傳送 [METransformNeedInput](metransformneedinput.md) 事件。
-   MFT 會捨棄無法用來建立輸出範例的任何輸入資料。
-   某些 MFTs 會在資料的結尾處產生「結尾」。 例如，當輸入資料停止之後，會產生額外的資料等音訊效果。 產生結尾的 MFT 應該在清空作業結束時這麼做。
-   在 MFT 完成清空之後，它會將下一個輸出範例標示 [**MFSampleExtension_Discontinuity**](mfsampleextension-discontinuity-attribute.md) 屬性，以表示資料流程中的不連續。

標記：

-   MFT 會繼續傳送 [METransformNeedInput](metransformneedinput.md) 事件，然後再傳送標記事件。
-   MFT 不會捨棄任何輸入資料。 如果有部分資料，則應該在標記點之後處理。
-   MFT 不會在標記點產生結尾。
-   此 MFT 不會在標記點之後設定不中斷旗標。

## <a name="format-changes"></a>格式變更

非同步 MFT 必須支援動態格式變更，如 [處理資料流程變更](handling-stream-changes.md)中所述。

## <a name="attributes"></a>屬性

非同步 MFT 必須執行 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 方法，以傳回有效的屬性存放區。 下列屬性適用于非同步 MFTs：



| 屬性                                                                                    | 描述                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MF_TRANSFORM_ASYNC](mf-transform-async.md)                                               | MFT 必須將此屬性設定為 **TRUE** (1) 。 用戶端可以查詢這個屬性，以找出 MFT 是否為非同步。 |
| [MF_TRANSFORM_ASYNC_UNLOCK](mf-transform-async-unlock.md)                                |                                                                                                                                   |
| [**MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE**](mft-support-dynamic-format-change-attribute.md) | MFT 必須將此屬性設定為 **TRUE** (1) 。 用戶端可以假設已設定這個屬性。                                |



 

## <a name="unlocking-asynchronous-mfts"></a>解除鎖定非同步 MFTs

非同步 MFTs 與原始的 MFT 資料處理模型不相容。 為了防止非同步 MFTs 中斷現有的應用程式，會定義下列機制：

<dl> 用戶端會在 MFT 上呼叫 <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes">IMFTransform：： GetAttributes</a> 。  
用戶端會查詢這個 <a href="mf-transform-async.md">MF_TRANSFORM_ASYNC</a> 屬性的。 若為非同步 MFT，此屬性的值為 **TRUE**。  
若要解除鎖定 MFT，用戶端必須將 <a href="mf-transform-async-unlock.md">MF_TRANSFORM_ASYNC_UNLOCK</a> 屬性設定為 **TRUE**。  
</dl>

在用戶端解除鎖定 MFT 之前，所有 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 方法應該會傳回 **MF_E_TRANSFORM_ASYNC_LOCKED**，但有下列例外狀況：

-   [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) (所有非同步 MFTs) 
-   [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) (所有非同步 MFTs) 
-   [**IMFTransform：： GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype) (編碼器僅) 
-   [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) (編碼器僅) 
-   [**IMFTransform：： GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) (所有非同步 MFTs) 
-   [**IMFTransform：： GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) (所有非同步 MFTs) 

下列程式碼顯示如何解除鎖定非同步 MFT：


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="shutting-down-the-mft"></a>關閉 MFT

非同步 MFTs 必須執行 [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) 介面。

-   [**關機**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown)： MFT 必須關閉其事件佇列。 如果使用標準事件佇列，請呼叫 [**IMFMediaEventQueue：： Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown)。 （選擇性） MFT 可能會釋放其他資源。 呼叫 **關機** 之後，用戶端不能使用 MFT。
-   [**GetShutdownStatus**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-getshutdownstatus)：呼叫 [**關機**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown)之後，MFT 應傳回 *pStatus* 參數中 **MFSHUTDOWN_COMPLETED** 的值。 它不應該傳回 **MFSHUTDOWN_INITIATED** 的值。

## <a name="registration-and-enumeration"></a>註冊和列舉

若要註冊非同步 MFT，請呼叫 [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)函式，並在 *旗標* 參數中設定 **MFT_ENUM_FLAG_ASYNCMFT** 旗標。  (先前已保留此旗標。 ) 

若要列舉非同步 MFTs，請呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數，並在 Flags 參數中設定 **MFT_ENUM_FLAG_ASYNCMFT** 旗 *標* 。 為了回溯相容性， [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函數不會列舉非同步 MFTs。 否則，在使用者的電腦上安裝非同步 MFT 可能會中斷現有的應用程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 



