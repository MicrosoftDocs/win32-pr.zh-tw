---
description: 本主題說明用戶端如何使用媒體基礎轉換 (MFT) 來處理資料。 用戶端就是直接在 MFT 上呼叫方法的任何作業。 這可能是應用程式或媒體基礎管線。
ms.assetid: be977d75-999e-4e57-9672-00a89246a2c1
title: 基本 MFT 處理模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca54df6d9765aaf54456c3d9dc4461a82a93d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026057"
---
# <a name="basic-mft-processing-model"></a>基本 MFT 處理模型

本主題說明用戶端如何使用媒體基礎轉換 (MFT) 來處理資料。 *用戶端* 就是直接在 MFT 上呼叫方法的任何作業。 這可能是應用程式或媒體基礎管線。

如果您想要的話，請閱讀本主題：

-   撰寫可直接呼叫一或多個 MFTs 的應用程式。
-   撰寫自訂的 MFT，並想要瞭解 MFT 的預期行為。

本主題說明 *同步* 處理模型。 在此模型中，所有資料處理方法都會封鎖，直到它們完成為止。 MFTs can also support an *asynchronous* model, which is described in the topic [Asynchronous MFTs](asynchronous-mfts.md).

-   [基本處理模型](#basic-processing-model)
    -   [建立 MFT](#create-the-mft)
    -   [取得資料流程識別碼](#get-stream-identifiers)
    -   [設定媒體類型](#set-media-types)
    -   [取得緩衝區需求](#get-buffer-requirements)
    -   [處理資料](#process-data)
-   [基本模型的延伸模組](#extensions-to-the-basic-model)
-   [IMF2DBuffer](#imf2dbuffer)
-   [清除 MFT](#flushing-an-mft)
-   [清空 MFT](#draining-an-mft)
-   [範例屬性](#sample-attributes)
-   [間斷](#discontinuities)
-   [動態格式變更](#dynamic-format-changes)
-   [串流事件](#stream-events)
-   [相關主題](#related-topics)

## <a name="basic-processing-model"></a>基本處理模型

### <a name="create-the-mft"></a>建立 MFT

有幾種方式可以建立 MFT：

-   呼叫 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函數。
-   呼叫 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數。
-   如果您已經知道 MFT 的 CLSID，只要呼叫 **CoCreateInstance** 就可以了。

某些 MFTs 可能會提供其他選項，例如特殊的建立函數。

### <a name="get-stream-identifiers"></a>取得資料流程識別碼

一個 MFT 有一或多個 *資料流程*。 輸入資料流程會接收輸入資料，而且輸出資料流程會產生輸出資料。 資料流程不會以相異物件表示。 相反地，不同的 MFT 方法會以串流識別碼作為參數。

某些 MFTs 可讓用戶端新增或移除輸入資料流程。 在串流處理期間，MFT 可以新增或移除輸出資料流程。  (用戶端無法加入或移除輸出資料流程。 ) 

1.   (選擇項。 ) 呼叫 [**IMFTransform：： GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits) ，以取得 MFT 可支援的最小和最大資料流程數目。 如果最小值和最大值相同，則 MFT 具有固定的資料流程數目。
2.  呼叫 [**IMFTransform：： GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount) 來取得初始的資料流程數目。
3.  呼叫 [**IMFTransform：： GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids) 以取得資料流程識別碼。 如果這個方法傳回 E \_ >notimpl，表示 MFT 具有固定的資料流程數目，而資料流程識別碼是從零開始的連續。
4.   (選擇項。 ) 如果 MFT 沒有固定數目的資料流程，請呼叫 [**IMFTransform：： AddInputStreams**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-addinputstreams) 來新增更多輸入資料流程，或呼叫 [**IMFTransform：:D eleteinputstream**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-deleteinputstream) 來移除輸入資料流程。  (您無法新增或移除輸出資料流程。 ) 

### <a name="set-media-types"></a>設定媒體類型

在 MFT 可以處理資料之前，用戶端必須設定每個 MFT 串流的媒體類型。 在設定輸出類型之前，可能會要求用戶端設定輸入類型，或可能需要與第一個) 相反的順序 (輸出類型。 某些 MFTs 沒有訂單的需求。

MFT 可以提供資料流程的慣用媒體類型清單。 此外，MFTs 也可以藉由將這項資訊新增至登錄，來指出它們所支援的一般格式。

若要設定媒體類型，請執行下列動作：

1.   (選擇性。針對每個輸入資料流程 ) ，呼叫 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) 來取得該資料流程的慣用類型清單。
    -   如果這個方法傳回 \_ \_ \_ 未設定的 MF E 轉換型別 \_ \_ ，您必須先設定輸出類型，然後跳到步驟3。
    -   如果方法傳回 E \_ >notimpl，則 MFT 沒有慣用輸入類型的清單，請跳至步驟2。
2.  針對每個輸入資料流程，呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 來設定輸入類型。 您可以使用步驟1中的媒體類型，或描述您輸入資料的類型。 如果任何資料流程傳回 \_ \_ \_ 未設定的 MF E 轉換類型 \_ \_ ，請跳至步驟3。
3.   (選擇性。針對每個輸出資料流程 ) ，呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 取得該資料流程的慣用類型清單。
    -   如果此方法傳回 \_ \_ \_ 未設定的 MF E 轉換型別 \_ \_ ，您必須先設定輸入類型，然後返回步驟1。
    -   如果有任何資料流程傳回 E \_ >notimpl，則 MFT 沒有慣用的輸出類型清單，請跳至步驟4。
4.  針對每個輸出資料流程，呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定輸出類型。 您可以使用步驟3中的媒體類型，或是描述您所需輸出格式的類型。
5.  如果任何輸入資料流程沒有媒體類型，請返回步驟1。

### <a name="get-buffer-requirements"></a>取得緩衝區需求

用戶端設定媒體類型之後，應該會取得每個資料流程的緩衝區需求：

-   針對每個輸入資料流程，呼叫 [**IMFTransform：： GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)。
-   針對每個輸出資料流程，呼叫 [**IMFTransform：： GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)。

### <a name="process-data"></a>處理資料

MFT 是設計成可靠的狀態機器。 但不會對用戶端進行任何回呼。

1.  使用 [**MFT \_ 訊息 \_ 通知 \_ 開始 \_ 串流**](mft-message-notify-begin-streaming.md)訊息來呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 。 此訊息要求 MFT 在串流處理期間配置其所需的任何資源。
2.  呼叫 [**IMFTransform：**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 在至少一個輸入資料流程上:P rocessinput，以將輸入範例傳遞至 MFT。
3.   (選擇性。 ) 呼叫 [**IMFTransform：： GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus) ，以查詢 MFT 是否可以產生輸出範例。 如果方法傳回 S \_ OK，請檢查 *pdwFlags* 參數。 如果 *pdwFlags* 包含 **MFT \_ 輸出 \_ 狀態 \_ 範例 \_ 就緒** 旗標，請移至步驟4。 如果 *pdwFlags* 為零，請返回步驟2。 如果方法傳回 E \_ >notimpl，請移至步驟4。
4.  呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 取得輸出資料。
    -   如果方法傳回 **MF \_ E \_ 轉換 \_ 需要 \_ 更多 \_ 輸入**，則表示此 MFT 需要更多輸入資料，請返回步驟2。
    -   如果方法傳回 **MF \_ E \_ 轉換 \_ 資料流程 \_ 變更**，則表示輸出資料流程的數目已變更，或輸出格式已變更。 用戶端可能需要查詢新的串流識別碼或設定新的媒體類型。 如需詳細資訊，請參閱 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)的檔。
5.  如果仍有要處理的輸入資料，請移至步驟2。 如果 MFT 已耗用所有可用的輸入資料，請繼續進行步驟6。
6.  使用 [**MFT \_ 訊息 \_ 通知資料流程訊息的 \_ 結尾 \_ 來 \_**](mft-message-notify-end-of-stream.md)呼叫 [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 。
7.  使用 [**MFT \_ 訊息 \_ 命令 \_ 清空**](mft-message-command-drain.md)訊息來呼叫 [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 。
8.  呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 以取得剩餘的輸出。 重複此步驟，直到方法傳回 **MF \_ E \_ 轉換 \_ 需要 \_ 更多 \_ 輸入**。 此傳回值表示已從 MFT 清空所有輸出。  (不會將此視為錯誤狀況。 ) 

此處所述的順序在 MFT 中盡可能保持最少的資料。 在每次呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)之後，用戶端都會嘗試取得輸出。 若要產生一個輸出範例，可能需要數個輸入範例，否則單一輸入範例可能會產生數個輸出範例。 用戶端的最佳行為是從 MFT 提取輸出範例，直到 MFT 需要更多輸入為止。

不過，此 MFT 應該能夠處理用戶端不同的方法呼叫順序。 例如，用戶端可能只會在呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 和 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)之間進行替代。 當此 MFT 有一些要產生的輸出時，它會從 **ProcessInput** 傳回 **MF \_ E \_ NOTACCEPTING** 來限制其取得的輸入數量。

此處所述的方法呼叫順序不是唯一有效的事件順序。 例如，步驟3和4假設用戶端以輸入類型開始，然後嘗試輸出類型。 用戶端也可以反轉此順序，並從輸出類型開始。 無論是哪一種情況，如果 MFT 都需要相反的順序，它應該會傳回錯誤碼 MF \_ E \_ 轉換 \_ 類型 \_ 未 \_ 設定。

用戶端可以在串流處理期間隨時呼叫資訊方法（例如 [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype) 和 [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)）。 用戶端也可以在任何時間嘗試變更媒體類型。 如果這不是有效的作業，則 MFT 應該會傳回錯誤碼。 簡單地說，MFTs 應該幾乎不會假設作業的順序，而不是呼叫本身所記載的部分。

下圖顯示本主題中所述程式的流程圖。

![從取得資料流程識別碼到設定輸入類型、取得輸入和處理輸出的迴圈的流程圖](images/mft-processing.gif)

## <a name="extensions-to-the-basic-model"></a>基本模型的延伸模組

（選擇性） MFT 可支援一些基本串流模型的擴充功能。

-   延遲讀取串流。 如果 [**IMFTransform：： GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) 方法傳回輸出資料流程的 **MFT \_ 輸出 \_ 資料流程 \_ 延遲 \_ 讀取** 旗標，則用戶端不需要從該輸出資料流程收集資料。 MFT 會繼續接受輸入，而在某個時間點，MFT 會捨棄該資料流程的輸出資料。 如果所有輸出資料流程都有此旗標，則 MFT 永遠不會無法接受輸入。 其中一個範例可能是視覺效果轉換，只有當用戶端有備用 CPU 週期來繪製視覺效果時，才會取得輸出。
-   Discardable 資料流程。 如果 [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) 方法傳回輸出資料流程的 **mft \_ 輸出 \_ 資料流程 \_ DISCARDABLE** 旗標，則用戶端可以要求 mft 捨棄輸出，但除非要求，否則 mft 不會捨棄任何輸出。 當 MFT 到達輸入緩衝區的最大值時，用戶端必須收集一些輸出資料，或要求 MFT 捨棄輸出。
-   選用的資料流程。 如果 [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) 方法傳回輸出資料流程的 **mft \_ 輸出 \_ 資料流程 \_ 選擇性** 旗標，或 [**IMFTransform：： GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo) 方法傳回輸入資料流程的 **mft \_ 輸入 \_ 資料流程 \_ 選擇性** 旗標，則該資料流程是選擇性的。 用戶端不需要在資料流程上設定媒體類型。 如果用戶端沒有設定型別，則會取消選取資料流程。 取消選取的輸出資料流程不會產生範例，且用戶端在呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)時，不會提供資料流程的緩衝區。 取消選取的輸入資料流程不接受輸入資料。 MFT 可以將其所有輸入和輸出資料流程標示為選用。 但是，必須至少選取一個輸入和一個輸出，才能讓 MFT 正常運作。
-   非同步處理。 非同步處理模型是在 Windows 7 中引進的。 It is described in the topic [Asynchronous MFTs](asynchronous-mfts.md).

## <a name="imf2dbuffer"></a>IMF2DBuffer

如果 MFT 處理未壓縮的影片資料，它應該使用 [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) 介面來操作範例緩衝區。 若要取得這個介面，請查詢任何輸入或輸出緩衝區上的 [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面。 若未使用此介面，可能會導致額外的緩衝區複本。 若要適當地使用此介面，當 **IMF2DBuffer** 可用時，轉換不應使用 **IMFMediaBuffer** 介面鎖定緩衝區。

如需處理影片資料的詳細資訊，請參閱 [未壓縮的影片緩衝區](uncompressed-video-buffers.md)。

## <a name="flushing-an-mft"></a>清除 MFT

清除 mft 會導致 mft 捨棄其所有輸入資料。 這可能會導致輸出資料流程出現中斷。 用戶端通常會在搜尋至輸入資料流程中的新點或切換至新的輸入資料流程之前，先排清 MFT，然後用戶端不在意資料遺失。

若要排清 MFT，請使用 [**mft \_ 訊息 \_ 命令 \_ 清除**](mft-message-command-flush.md)訊息來呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 。

## <a name="draining-an-mft"></a>清空 MFT

*清空* mft 會使 mft 產生的輸出數量，與任何已傳送的輸入資料相同。 如果 MFT 無法從可用的輸入產生完整輸出範例，則會捨棄輸入資料。 用戶端通常會在到達來來源資料流的結尾時，或在來來源資料流中的格式變更之前，清空 MFT。 若要清空 MFT，請執行下列動作：

1.  使用 [**MFT \_ 訊息 \_ 命令 \_ 清空**](mft-message-command-drain.md)訊息來呼叫 [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) 。 這則訊息會通知 MFT，應盡可能傳遞已傳送的輸入資料中的輸出資料。
2.  呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) 以取得輸出資料，直到方法傳回 **MF \_ E \_ 轉換 \_ 需要 \_ 更多 \_ 輸入** 為止。

當 MFT 正在清空時，它不會接受任何其他輸入。

## <a name="sample-attributes"></a>範例屬性

輸入範例可能具有必須複製到對應輸出範例的屬性。

-   如果 MFT 針對 [**MFPKEY \_ EXATTRIBUTE \_ 支援**](mfpkey-exattribute-supported-property.md)的屬性傳回 **VARIANT \_ TRUE** ，則此 mft 必須複製這些屬性。
-   如果 [**MFPKEY \_ EXATTRIBUTE \_ 支援**](mfpkey-exattribute-supported-property.md) 的屬性為 **VARIANT \_ FALSE** 或未設定，則用戶端必須複製這些屬性。

針對具有一個輸入和一個輸出的 MFT，您可以使用下列一般規則：

-   如果每個輸入範例都只產生一個輸出範例，您可以讓用戶端複製屬性。 讓 [**MFPKEY \_ EXATTRIBUTE \_ 支援**](mfpkey-exattribute-supported-property.md) 的屬性保持未設定。
-   如果輸入範例和輸出範例之間沒有一對一的對應，則此 MFT 必須決定輸出範例的正確屬性。 將 [**MFPKEY \_ EXATTRIBUTE \_ 支援**](mfpkey-exattribute-supported-property.md) 的屬性設定為 **VARIANT \_ TRUE**。

## <a name="discontinuities"></a>間斷

中斷是音訊或影片串流中的中斷。 不連續可能是因為網路連線上的封包、檔案損毀、檔案資料損毀、從某個來來源資料流切換到另一個來源串流，或許多其他原因所致。 不連續會在不連續的第一個範例上設定 MFSampleExtension 不中斷屬性來發出信號。 [**\_**](mfsampleextension-discontinuity-attribute.md) 無法在範例的中間發出中斷。 因此，任何不連續的資料都應該以個別的範例傳送。

某些轉換（特別是處理未壓縮資料的轉換，例如音訊和影片效果）在處理輸入資料時應該忽略不連續。 這些 MFTs 通常是設計用來處理連續資料，而且應該將任何收到的資料視為連續的資料，即使在不連續的情況下也一樣。

如果 MFT 忽略輸入資料的不連續，則如果輸出範例的時間戳記與輸入範例相同，它仍應設定輸出範例上的不連續旗標。 但是，如果輸出範例有不同的時間戳記，則 MFT 不應傳播中斷。  (在某些音訊 resamplers 中，就會發生這種情況。例如，在資料流程中錯誤的位置 ) 不連續的情況，會比不中斷的情況更糟。

大部分的解碼器無法忽略不連續，因為中斷會影響下一個範例的解讀。 任何使用畫面間壓縮的編碼技術（例如 MPEG-2）都屬於此類別。 某些編碼配置僅使用框架內的壓縮，例如 DV 和 MJPEG。 這些解碼器可以安全地忽略不連續。

回應不連續的轉換通常應該會在中斷的情況發生之前輸出盡可能多的資料，並捨棄其餘部分。 具有不連續旗標的輸入範例應處理為數據流中的第一個範例。  (此行為符合為 [**MFT \_ 訊息 \_ 命令 \_ 清空**](mft-message-command-drain.md) 訊息指定的行為。 ) 不過，確切的詳細資料將取決於媒體格式。

如果解碼器沒有任何可減輕中斷的情況，就應該將不連續旗標複製到輸出資料。 Demultiplexers 和其他使用壓縮資料的 MFTs 必須將任何不連續複製到輸出資料流程。 否則，下游元件可能無法正確解碼壓縮的資料。 一般來說，除非 MFT 包含明確的程式碼，以使不連續變得順暢，否則幾乎一律會正確地傳遞不連續下游。

## <a name="dynamic-format-changes"></a>動態格式變更

格式在串流期間可能會變更。 例如，外觀比例可能會在影片資料流程的中間變更。

如需有關 MFT 如何處理資料流程變更的詳細資訊，請參閱 [處理資料流程變更](handling-stream-changes.md)。

## <a name="stream-events"></a>串流事件

若要將事件傳送到 MFT，請呼叫 [**IMFTransform：:P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)。 如果方法傳回 **MF \_ S 轉換不會 \_ \_ \_ \_ 傳播 \_ 事件**，則在後續呼叫 [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)時，MFT 會將事件傳回給呼叫者。 如果方法傳回任何其他 **HRESULT** 值，則在 **PROCESSOUTPUT** 中，MFT 不會將事件傳回至用戶端。 在此情況下，用戶端會負責將下游事件傳播至管線中的下一個元件（如果適用）。 如需詳細資訊，請參閱 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> </dl>

 

 



