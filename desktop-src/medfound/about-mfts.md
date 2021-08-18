---
description: 關於 MFTs
ms.assetid: ca9cef70-b897-4fd5-9a13-8bf1c2b84b00
title: 關於 MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04bfc09cbd17e5f0810f46eb6e42b230010348e89040b3cd407e98ee069c8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035702"
---
# <a name="about-mfts"></a>關於 MFTs

媒體基礎轉換 (MFTs) 提供用來處理媒體資料的一般模型。 MFTs 可用於 (Dsp) 的解碼器、編碼器和數位訊號處理器。 簡而言之，位於媒體來源和媒體接收器之間媒體管線中的任何事物，都是一個 MFT。

針對大部分的應用程式，媒體基礎架構的較高層級會隱藏 MFT 資料處理的詳細資料。 許多媒體基礎的應用程式永遠不會直接呼叫 MFT。 不過，您當然可以直接在您的應用程式中裝載 MFT。

MFTs 是第一次使用 DirectX 媒體物件引進的轉換模型演進 (DMOs) 。 事實上，建立支援這兩種模型的轉換相當簡單。 相較于 DMOs，MFTs 的必要行為更清楚地指定，可讓您更輕鬆地撰寫正確的執行。 此外，MFTs 還可支援硬體加速的影片處理。

本主題簡要說明了 MFT 處理模型，並著重于整體設計，而不是特定的方法呼叫。 如需更詳細的逐步說明，請參閱 [基本的 MFT 處理模型](basic-mft-processing-model.md)。

## <a name="streams"></a>串流

MFT 具有輸入資料流程和輸出資料流程。 輸入資料流程會接收資料，而且輸出資料流程會產生資料。 例如，一個資料流程有一個輸入資料流程，它會接收編碼的資料，另一個輸出資料流程會產生已解碼的資料。

在 MFT 上的資料流程不會以相異的 COM 物件表示。 相反地，每個資料流程都有指定的資料流程識別碼，而 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面中的方法會將串流識別碼作為輸入參數。

某些 MFTs 具有固定的資料流程數目。 例如，解碼器和編碼器通常只會有一個輸入和一個輸出。 其他 MFTs 有動態的資料流程數目。 如果 MFT 支援動態資料流，用戶端可以新增輸入資料流程。 用戶端無法新增輸出資料流程，但 MFT 可能會在處理期間新增或移除輸出資料流程。 例如，multiplexers 通常可讓用戶端新增輸入資料流程，並有多個多工資料流程的輸出。 根據輸入資料流程的內容而定，Demultiplexers 是反向的，具有一個輸入，但是輸出資料流程的動態數目。 下圖顯示多工器與信號信號之間的差異。

![此圖顯示編碼器/解碼器 (1 個輸入、1個輸出) 、多工器 (2 個輸入、1個輸出) ，以及一個信號 (1 個輸入、2個輸出) ](images/f2b95bd5-f862-4d66-9d75-550a90f6cc97.gif)

## <a name="media-types"></a>媒體類型

第一次建立 MFT 時，沒有任何資料流程具有已建立的格式。 在 MFT 可以處理資料之前，用戶端必須設定資料流程的格式。 例如，使用解碼器時，輸入格式為原始原始程式檔中使用的壓縮格式，而輸出格式為未壓縮的格式，例如 PCM 音訊或 RGB 影片。 串流格式會使用 [媒體類型](media-types.md)來描述。

根據 MFT 的內部狀態，它可能會提供每個串流可能的媒體類型清單。 當您設定媒體類型時，可以使用此清單做為提示。 設定某個資料流程的媒體類型可以變更另一個資料流程可能類型的清單。 例如，在用戶端設定輸入類型之前，解碼器通常無法提供任何輸出類型。 輸入型別包含的資訊，是因為解碼器需要傳回可能的輸出類型清單。

若要設定資料流程上的媒體類型，請呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 或 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)。 若要取得資料流程可能媒體類型的清單，請呼叫 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) 或 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)。

## <a name="processing-data"></a>處理資料

在用戶端設定資料流程的媒體類型之後，即已準備好處理資料。 為了進行這項操作，用戶端會在提供輸入資料到 MFT 之間進行替代，並從 MFT 取得輸出資料：

-   若要將輸入資料提供給 MFT，請呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)。
-   若要從 MFT 提取輸出資料，請呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。

[**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)方法會使用用戶端所配置之媒體範例的指標。 媒體範例包含一或多個緩衝區，而且每個緩衝區都包含要處理之 MFT 的輸入資料。

[**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)方法支援兩種不同的配置模型： MFT 配置輸出緩衝區或用戶端配置輸出緩衝區。 部分 MFTs 支援這兩種配置模型，但不需要同時支援這兩種配置模型。 例如，某個 MFT 可能需要用戶端配置輸出緩衝區。 [**IMFTransform：： GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)方法會傳回輸出資料流程的相關資訊，包括由 MFT 支援的配置模型。

MFTs 的設計目的是盡可能緩衝最少的資料，以便將管線中的延遲降至最低。 因此，在任何指定的時間，MFT 都可以發出下列其中一個條件：

-   此 MFT 需要更多輸入資料。 在此狀態下，除非用戶端至少呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 一次，否則 MFT 無法產生輸出。
-   除非用戶端至少呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 一次，否則 MFT 不會接受任何其他輸入。

例如，假設您使用的是影片解碼來解碼包含混合的主要畫面格和差異框架的影片串流。 一開始，此 MFT 需要一些輸入，才能解碼任何框架。 用戶端會呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 來傳遞第一個畫面格。 假設第一個框架是 delta 框架 (在下圖中顯示為預測框架) 的 ' P '。 此解碼器會保存在此框架上，但在取得下一個主要畫面格之前，它無法產生任何輸出。

![此圖顯示需要輸入的 mft，指向預測的框架](images/f5a88ac6-24da-40e5-b356-649aa6f811c3.gif)

用戶端會繼續呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ，最後會到達下圖中顯示的下一個主要畫面格 (下圖中顯示為程式碼內框架) 的 ' I '。 現在，此解碼器有足夠的畫面格開始解碼。 此時它會停止接受輸入，而且用戶端必須呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 來取得已解碼的畫面格。

![此圖顯示不接受輸入的 mft，指向一個程式碼內框架和三個預測的框架](images/ae014a1a-9d03-4cfa-a04d-4a63bdc83f73.gif)

用戶端最簡單的方法就是直接呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 和 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。 「 [基本 MFT 處理模型](basic-mft-processing-model.md)」主題會說明更複雜的演算法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 



