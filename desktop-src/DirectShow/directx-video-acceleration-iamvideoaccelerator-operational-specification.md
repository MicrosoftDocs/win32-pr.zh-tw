---
description: DirectX Video 加速 IAMVideoAccelerator 操作規格
ms.assetid: 25ee05d5-8554-4739-9122-e3c0255bf965
title: DirectX Video 加速 IAMVideoAccelerator 操作規格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3360e18e91197f2a15a36fb112f0419b6382e915
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935637"
---
# <a name="directx-video-acceleration-iamvideoaccelerator-operational-specification"></a>DirectX Video 加速 IAMVideoAccelerator 操作規格

操作的精確機制如下：

1.  此處所定義的每個受限模式設定檔都有相關聯的 DirectX VA GUID，可由下游輸入 pin 的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 和 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 支援，並列于 [**IAMVideoAccelerator：： GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids)中。
2.  同樣地，搭配 DirectX VA 使用的每一種加密通訊協定類型，都應該有相關聯的加密通訊協定類型 GUID，可由下游輸入 pin 的 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 和 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 所支援，並且列在 **IAMVideoAccelerator：： GetVideoAcceleratorGUIDs** 中。 \_無法在此清單中傳送 "no encryption" GUID DXVA NoEncrypt，因為它的支援是必要的，因此是隱含的。
3.  在呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 來嘗試連接到下游輸入的 pin 碼之後，解碼器的 [**IAMVideoAcceleratorNotify：： GETCREATEVIDEOACCELERATORDATA**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) 應傳回 DXVA \_ ConnectMode 資料結構的指標，其中包含連接的連接模式資訊。 [**IAMVideoAccelerator：： GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo) 應該使用 \* pdwNumTypesCompBuffers = 16 來呼叫，並且根據慣例，傳回壓縮的緩衝區資訊，而這是根據 DirectX VA 規格的3.4 節中所定義的每個緩衝區 (的類型編號) 可直接當做以零為基底的索引，在傳回的 **AMVACompBufferInfo** 資料結構陣列中使用。 這需要針對將不會使用的任何緩衝區類型 (包括緩衝區類型0在內，因為未定義該緩衝區類型的使用) ，加速器驅動程式將會提供某種形式的 "虛設" 參數值的 AMVACompBufferInfo 資料結構 (例如 dwNumCompBuffers = 0、dwWidthToCreate = 0、dwHeightToCreate = 0 和 dwBytesToAllocate = 0) 。
4.  DXVA 函式指示和相關聯的資料緩衝區會使用 [**IAMVideoAccelerator：： Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute)來傳送。 DXVA 函數會在呼叫的 dwFunction 參數中指出。 唯一與初始化相關的 DXVA 函數是 DXVA \_ ConfigQueryOrReplyFunc 和 DXVA \_ EncryptProtocolFunc。
    -   如果 dwFunction 包含 DXVA \_ ConfigQueryOrReplyFunc，在此呼叫中將資料傳遞給快速鍵的 lpPrivateInputData 指標應指向設定資料結構，從快速鍵接收資訊的 lpPrivateOutputData 指標應指向可放置替代或重複設定資料結構的區域、pamvaBufferInfo 陣列的 AMVABUFFERINFO 指標應為 **Null**，而 dwNumBuffers 則應為零。 傳回的 HRESULT 包含「 \_ 確定」或「 \_ 錯誤」標記法，或 \_ \_ 在通訊協定執行 (（例如不正確設定參數) ）發生嚴重問題時，出現 E 失敗或電子 INVALIDARG 或其他錯誤指示 HRESULT。 對於 DXVA ConfigQueryOrReplyFunc 的所有使用， **IAMVideoAccelerator：： execute** 的所有呼叫都 \_ 必須在 **IAMVideoAccelerator：： execute** 的所有其他呼叫之前。
    -   如果 dwFunction 包含 DXVA \_ EncryptProtocolFunc，在此呼叫中將資料傳遞給快速鍵的 lpPrivateInputData 指標應指向以 DXVA EncryptProtocolHeader 開頭的加密通訊協定資料結構 \_ ，從快速鍵接收資訊的 lpPrivateOutputData 指標應指向要傳回資料的區域 (例如，加密通訊協定) 的憑證 (\_ 可放置 ENCRYPTPROTOCOLHEADER) ，AMVABUFFERINFO 陣列的 pamvaBufferInfo 指標應為 **Null**，而 dwNumBuffers 則應為零。 \_只要加密通訊協定正常運作，傳回的 HRESULT 就會包含 [確定]，而且當 \_ 通訊協定執行發生嚴重問題時，會包含電子失敗或電子 \_ INVALIDARG 或其他錯誤指示 HRESULT。

        在以上述方式初始化作業之後，該解碼器的實際作業會依照下列方式繼續進行：

5.  **IAMVideoAccelerator：： BeginFrame** 應該在使用壓縮的緩衝區參數傳送任何 bDXVA Func 之前呼叫， \_ 這會導致寫入未壓縮的目的地介面。 DirectX VA 中的 [**IAMVideoAccelerator：： BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) 用途是將目的地介面與索引值產生關聯，並通知影片加速器驅動程式，以起始寫入介面，讓驅動程式可以回應是否已準備好要覆寫介面。 在 **IAMVideoAccelerator：： BeginFrame** 中傳遞的 **AMVABeginFrameInfo** 結構，應該包含單一單字 wBeginPictureIndex 參數的 pInputData 指標，該參數符合傳遞至 **IAMVideoAccelerator：： BeginFrame** (的框架索引，dwSizeInputData 應為 2) 。 這是要在壓縮的緩衝區中用來對介面進行寫入命令 (例如，用來做為 wDecodedPictureIndex、wDeblockedPictureIndex、wBlendedDestinationIndex 或 wPicResampleDestPicIndex) 的索引。 **IAMVideoAccelerator：： BeginFrame** 的每個呼叫都應與 [**IAMVideoAccelerator：： EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe)的對應呼叫配對，如下所述。 例如，若要將壓縮的圖片解碼，然後使用前端緩衝區對緩衝區來與圖形影像混合，則在將壓縮圖片解碼為 wDecodedPictureIndex 中指定的介面之前，會先呼叫 **IAMVideoAccelerator：： BeginFrame：** 接著呼叫 **IAMVideoAccelerator：： EndFrame** 之後，在傳遞用來解碼圖片的所有壓縮緩衝區之後，再呼叫 **IAMVideoAccelerator：： BeginFrame** ，然後再將圖形來源中的圖形來源與已解碼的圖片結合到 wBlendedDestinationIndex 中指定的介面，然後在 Alpha blend 組合作業之後第二次呼叫 **IAMVideoAccelerator：： EndFrame** 。AMVABeginFrameInfo 中的指標 pOutputData 應該是 **Null** (而且 dwSizeOutputData 應該是 "0" ) 。 **IAMVideoAccelerator：： BeginFrame** 所傳回的 HRESULT 應為：
    -   \_如果未壓縮的介面可用且已備妥可供使用，則為 [正常]。
    -   E \_ 暫止如果未壓縮的表面尚未可用，但很快就會變成可用狀態 (如果正在讀取未壓縮的介面以供顯示，且表面的讀取/顯示尚未完成) 。
    -   \_ \_ 只有在偵測到資料格式或通訊協定錯誤 (例如 dwSizeInputData 的錯誤值或非 **Null** 的 pOutputData) 時，才會讓 e 失敗或 e INVALIDARG 其他錯誤指示。
6.  DXVA 函式指示和相關聯的資料緩衝區會使用 **IAMVideoAccelerator：： Execute** 來傳送。 \_在 [**IAMVideoAccelerator：： Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute)的相同呼叫中，可能會指出一個以上的 bDXVA Func 值。 BDXVA \_ Func 值應封裝至呼叫的 dwFunction 參數中，並在八個 MSBs 中使用第一個函式命令、接下來八位中的下一個命令，依此類推，並以零填補任何剩餘的位。 BDXVA func 的值 0xFF \_ 表示 bDXVA \_ func 已擴充為二或四個位元組。 如果第二個位元組也是0xFF，這表示 bDXVA \_ Func 延伸至四個位元組。 如果第三個位元組的前四個位是0xF 或0x0，這表示 bDXVA \_ Func 包含 DXVA \_ CONFIGQUERYORREPLYFUNC 或 DXVA \_ EncryptProtocolFunc。 多位元組命令不應指出 dwFunction 結尾之後的接續。 請小心使用，以確保在相同的 IAMVideoAccelerator 呼叫中指定的不同 bDXVA Func 值之間，不會有任何順序相依性存在：在 \_ 後續呼叫 **IAMVideoAccelerator：： Execute** 之前，**執行** 和所有可能的競爭條件 (例如在圖片解碼和子圖片混色之間，在子圖片載入和子圖片混色之間，以及在下一次呼叫 IAMVideoAccelerator **：： BeginFrame 和** IAMVideoAccelerator [**：： QueryRenderStatus 的**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus)情況下，) 會導致無法正常呼叫。
    -   如果 dwFunction 包含 DXVA \_ ConfigQueryOrReplyFunc，在此呼叫中將資料傳遞給快速鍵的 lpPrivateInputData 指標應指向設定資料結構，從快速鍵接收資訊的 lpPrivateOutputData 指標應指向可放置替代或重複設定資料結構的區域、pamvaBufferInfo 陣列的 AMVABUFFERINFO 指標應為 **Null**，而 dwNumBuffers 則應為零。 傳回的 HRESULT 包含「 \_ 確定」或「 \_ FALSE」指示以回應查詢，或是 \_ \_ 當通訊協定執行 (（例如 invalid.configuration 參數) ）發生嚴重問題時，e 失敗或 e INVALIDARG 其他錯誤指示 HRESULT。 對於 DXVA ConfigQueryOrReplyFunc 的所有使用， **IAMVideoAccelerator：： execute** 的所有呼叫都 \_ 必須在 **IAMVideoAccelerator：： execute** 的所有其他呼叫之前。
    -   如果 dwFunction 包含 DXVA \_ EncryptProtocolFunc，在此呼叫中將資料傳遞給快速鍵的 lpPrivateInputData 指標應指向以 DXVA EncryptProtocolHeader 開頭的加密通訊協定資料結構 \_ ，從快速鍵接收資訊的 lpPrivateOutputData 指標應指向要傳回資料的區域 (例如，加密通訊協定) 的憑證 (\_ 可放置 ENCRYPTPROTOCOLHEADER) ，AMVABUFFERINFO 陣列的 pamvaBufferInfo 指標應為 **Null**，而 dwNumBuffers 則應為零。 \_只要加密通訊協定正常運作，傳回的 HRESULT 就會包含 [確定]，而且當 \_ 通訊協定執行發生嚴重問題時，會包含電子失敗或電子 \_ INVALIDARG 或其他錯誤指示 HRESULT。
    -   如果 dwFunction 不包含 DXVA \_ ConfigQueryOrReplyFunc 或 DXVA \_ EncryptProtocolFunc，則將資料傳遞至快速鍵的 lpPrivateInputData 指標應指向緩衝區描述清單。 每個緩衝區的緩衝區描述清單結構中的前四個專案 (dwTypeIndex、dwBufferIndex、dwDataOffset 和 dwDataSize) 應該等於相同緩衝區之 AMVABUFFERINFO 資料結構中的專案。 如果 \_ 在 dwFunction 中指定 bDXVA Func 等於 "1"，且 bPicReadbackRequests 為 "1"，從快速鍵接收資訊的 lpPrivateOutputData 指標應指向持續性記憶體的區域 (例如，) 要使用加速器中的讀回巨大區塊資料來填入， (這類資料，直到 **IAMVideoAccelerator：： QueryRenderStatus** 寫入相同的圖片參數緩衝區為止， \_ 如以下的專案10所述) 。 否則，從快速鍵接收資訊的 lpPrivateOutputData 指標應指向要設定為下列其中一個指示值的單一 DWORD (特別適用于報告非主控制項 VLD 操作) 中的位流錯誤。

        | 值 | 描述                                     |
        |-------|-------------------------------------------------|
        | 0     | 執行正常。                                   |
        | 1     | 遇到資料格式的次要問題。       |
        | 2     | 遇到資料格式的重大問題。 |
        | 3     | 遇到資料格式的嚴重問題。      |
        | 4     | 遇到其他嚴重問題。               |

        

         

        如果指出任一類型的「嚴重」問題，則除非可以採取矯正措施，否則軟體解碼器應該會停止 (的函式運作) 。 在圖片的緩衝區轉譯完成之前，主控制項所傳回的這項資料將無法讀取，因為可以透過 [**IAMVideoAccelerator：： QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus)進行測試。 只要介面作業正常運作，傳回的 HRESULT 就 \_ 會包含 [確定]，而且可能會 \_ 在發生嚴重問題時傳回 e FAIL 或 e \_ INVALIDARG 或其他錯誤指示 HRESULT。

7.  當使用 [**IAMVideoAccelerator：： Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) with bDXVA Func 等於 "1" 時，針對每一張圖片的解碼傳送的第一個緩衝區 \_ ，以及在位流中解碼圖片的所有緩衝區都必須在任何用來解碼後續圖片的緩衝區之前傳送。 如果傳送了巨大區塊控制命令緩衝區，則應該傳送對應的剩餘差異資料緩衝區， (包含相同巨大區塊) 的資料，但具有相同的 **IAMVideoAccelerator：： Execute** 呼叫。
8.  在傳送所有壓縮的緩衝區之後，應該會呼叫 [**IAMVideoAccelerator：： EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) ，這會導致在指定的未壓縮介面中建立輸出內容 (針對 WDecodedPictureIndex、WDeblockedPictureIndex、WBlendedDestinationIndex 或 wPicResampleDestPicIndex) 指定的作業結果。 此呼叫 **IAMVideoAccelerator：： EndFrame** 的目的是要通知影片加速器硬體已傳送指定作業所需的所有資料。 透過 **IAMVideoAccelerator：： EndFrame** 傳送下游的資料指標應指向包含即將結束之框架索引的單一單字 wEndPictureIndex。 在傳送相關的壓縮緩衝區之前，此參數必須符合先前呼叫 [**IAMVideoAccelerator：： BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) 所指定的 wBeginPictureIndex 值。 在呼叫 **IAMVideoAccelerator：： EndFrame** 之後，在任何圖片的 WDecodedPictureIndex、WDeblockedPictureIndex、WBlendedDestinationIndex 或 wPicResampleDestPicIndex 中都找不到具有索引 wEndPictureIndex 的未壓縮介面，直到發出另一個 **IAMVideoAccelerator：： BeginFrame** 的呼叫時，才會發出，以宣告將會發生這種情況，且會 \_ 傳回 a OK。 不過，後續的讀取存取命令可能會發生目的地介面索引，例如 wForwardRefPictureIndex、wBackwardRefPictureIndex、wPicResampleSourcePicIndex 或 bRefPicSelect \[ i \] 。 **IAMVideoAccelerator：： EndFrame** 所傳回的 HRESULT 應為 S \_ OK，除非有某種類型的資料格式或通訊協定錯誤，在此情況下，它可能是 E \_ 失敗或 e \_ INVALIDARG 或其他錯誤指示。
9.  如果是以欄位為基礎的解碼 (例如，在 MPEG-2 bitstreams 中) 位流中的功能圖片將不會有一對一的對應，無法在加速器介面中的未壓縮表面。 在 MPEG-2 位流中解碼欄位圖片時，將會有兩個「圖片」解碼，以產生一個完整的輸出未壓縮表面。 在 DirectX VA 介面定義中，每個框架都會對應到每個使用的 wDecodedPictureIndex、wDeblockedPictureIndex、wBlendedDestinationIndex 或 wPicResampleDestPicIndex。 因此，需要對 **IAMVideoAccelerator：： BeginFrame** 和 **IAMVideoAccelerator：： EndFrame** 進行兩組呼叫，才能將欄位圖片解碼成輸出未壓縮表面。
10. 呼叫 [**IAMVideoAccelerator：： QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) ，dwFlags 等於零，這會在呼叫 **IAMVideoAccelerator：： EndFrame** 具有特定的 wEndPictureIndex，並檢查在 WDecodedPictureIndex、WDeblockedPictureIndex、wBlendedDestinationIndex 或 wPicResampleDestPicIndex 中包含 wEndPictureIndex 之傳送的緩衝區狀態， \_ 如果將資料寫入未壓縮表面的所有作業都已完成，而且如果作業尚未完成，將會傳回 E \_ 暫止。 如果 \_ \_ 發生通訊協定錯誤，可能會傳回 E 或 e INVALIDARG 或其他錯誤指示。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 DirectX Video 加速對應至 IAMVideoAccelerator](mapping-directx-video-acceleration-to-iamvideoaccelerator.md)
</dt> </dl>

 

 



