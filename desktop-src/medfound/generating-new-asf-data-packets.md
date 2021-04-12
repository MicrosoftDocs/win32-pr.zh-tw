---
description: 產生新的 ASF 資料封包
ms.assetid: 7afa9694-c965-40e2-8549-e32ff48def2a
title: 產生新的 ASF 資料封包
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f3432ecf34c58247a1533adb202b75f59d770c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468621"
---
# <a name="generating-new-asf-data-packets"></a>產生新的 ASF 資料封包

ASF 多工器是 *一種 WMContainer* 層元件，可與 [ASF 資料物件](asf-file-structure.md) 搭配使用，並讓應用程式能夠針對符合 ContentInfo 物件中所定義之需求的資料流程產生 ASF 資料封包。

多工器有一個輸入和一個輸出。 它會接收包含數位媒體資料的串流範例，並產生一或多個可寫入至 ASF 容器的資料封包。

下列清單摘要說明產生 ASF 資料封包的流程：

1.  將輸入資料傳遞給 IMFASFMultiplexer 中的多 [**任務器：:P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)。
2.  藉由在迴圈中呼叫 [**IMFASFMultiplexer：： GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) 來收集資料封包，直到所有完成的封包都已取出為止。
3.  將輸入資料轉換成完整的封包之後，多工器中可能會有一些暫止的資料，但 [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)並不會加以取出。 呼叫 [**IMFASFMultiplexer：： Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) 以 packetize 暫止的範例，並再次呼叫 **GetNextPacket** ，以從多工器收集這些樣本。
4.  藉由呼叫 [**IMFASFMultiplexer：： End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) 以反映多工器在產生資料封包期間所做的變更，來更新相關聯的 ASF 標頭物件。

下圖說明透過多工器對 ASF 檔案產生的資料封包。

![顯示 asf 檔案之資料封包產生的圖表](images/packet.gif)

## <a name="asf-data-packet-creation"></a>建立 ASF 資料封包

建立並初始化多工器（如建立多工器 [物件](creating-the-multiplexer-object.md)中所述）之後，請呼叫 [**IMFASFMultiplexer：:P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) ，將輸入資料傳遞給多工器，以處理資料封包。 指定的輸入必須位於媒體範例 ([**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面) 可以有一或多個媒體緩衝區 ([**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) 介面) 包含資料流程的資料。 在 ASF 到 ASF 轉碼的情況下，可以從建立 packetized 資料流程範例的分隔器產生輸入媒體範例。 如需詳細資訊，請參閱 [ASF 分隔器](asf-splitter.md)。

在呼叫 [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)之前，請確定輸入媒體範例的時間戳記是有效的呈現時間;否則 **ProcessSample** 會失敗，並傳回 MF \_ E \_ NO \_ 範例 \_ 時間戳記程式碼。

多工器可以透過 [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)，以壓縮或未壓縮的媒體範例形式接受輸入。 多工器會根據資料流程的頻寬使用量，將傳送時間指派給這些範例。 在這個過程中，多工器會檢查有漏洞值區參數 (的位元速率和緩衝區視窗使用率) ，而且可以拒絕不遵守這些值的範例。 輸入媒體範例可能會因為下列其中一個原因而導致頻寬檢查失敗：

-   如果輸入媒體範例晚抵達，因為最後指派的傳送時間大於此媒體範例的時間戳記。 [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) 失敗並傳回 **MF \_ E \_ 晚期 \_ 範例** 錯誤碼。
-   如果輸入媒體範例上的時間戳記早于指派的傳送時間 (這表示) 緩衝區溢位。 如果多工器已設定為在多工器初始化期間設定 MFASF 多工器 **\_ \_ AUTOADJUST \_ 位元速率** 旗標來調整位元速率，則可以忽略這種情況。 如需詳細資訊，請參閱建立多工器 [物件](creating-the-multiplexer-object.md)中的「多工器初始化和有漏洞 Bucket 設定」。 如果未設定此旗標，而多工器遇到頻寬溢出， [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) 就會失敗，並傳回 **MF \_ E \_ 頻寬 \_ 溢出** 的錯誤碼。

在多工器指派傳送時間之後，輸入媒體範例會新增至 [ *傳送] 視窗*，也就是輸入媒體範例的清單，依傳送時間和準備處理到資料封包。 在資料封包結構期間，會剖析輸入媒體範例，並將相關的資料寫入資料封包作為承載。 完整的資料封包可包含一或多個輸入媒體範例中的資料。

當新的輸入媒體範例抵達傳送視窗時，會將它們新增至佇列，直到有足夠的媒體樣本可形成一個完整的封包。 輸入媒體範例所包含媒體緩衝區中的資料不會複製到產生的資料封包。 資料封包會保存輸入媒體緩衝區的參考，直到已完全 packetized 輸入媒體範例，並從多工器收集完整的封包為止。

當有完整的資料封包可用時，可以藉由呼叫 [**IMFASFMultiplexer：： GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)來加以取出。 如果您在完成封包準備進行抓取時呼叫 [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) ，它會失敗並傳回 **MF \_ E \_ NOTACCEPTING** 錯誤碼。 這表示多工器無法接受更多輸入，您必須呼叫 **GetNextPacket** 來取出等候中的封包。 在理想的情況下，每個 **ProcessSample** 呼叫後面應該接著一或多個 **GetNextPacket** 呼叫，以取得完整的資料封包。 它可能需要一個以上的輸入媒體範例來建立完整的資料封包。 相反地，一個輸入媒體範例中的資料可能會跨越多個封包。 因此，並非所有對 **ProcessSample** 的呼叫都會產生輸出媒體範例。

如果輸入媒體範例包含由 [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) 屬性工作表示的主要畫面格，則多工器會將屬性複製到封包。

## <a name="getting-asf-data-packets"></a>取得 ASF 資料封包

若要收集多工器所產生之完整資料封包的輸出媒體範例，請在迴圈中呼叫 [**IMFASFMultiplexer：： GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) ，直到沒有其他輸出媒體樣本剩下的封包。 以下列出成功案例：

-   如果有完整的資料封包可用， [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)會在 *pdwStatusFlags* 參數中收到「 **ASF \_ 狀態 \_ 旗標 \_ 不完整**」旗標; *ppIPacket* 參數會接收第一個資料封包的指標。 只要收到此旗標，您就必須呼叫這個方法。 在每個反復專案中， *ppIPacket* 會指向佇列中的下一個封包。
-   如果只有一個資料封包， *ppIPacket* 會指向它，而 *pdwStatusFlags* 中不會收到 [ **ASF \_ 狀態 \_ 旗標未 \_ 完成**] 旗標。
-   如果多工器仍在 packetizing 和新增資料封包的過程中， [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)可能會成功，而不會產生任何資料封包。 在此情況下， *ppIPacket* 會指向 **Null**。 若要繼續，您必須藉由呼叫 [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)，提供多工器的輸入媒體範例。

下列範例程式碼顯示使用多工器產生資料封包的函式。 產生的資料封包內容將會寫入至呼叫端所配置的資料位元組資料流程中。


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



此函式 `WriteBufferToByteStream` 會顯示在 [**IMFByteStream：： Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write)主題中。

若要查看使用此程式碼範例的完整應用程式，請參閱 [教學課程：將 ASF 資料流程從一個檔案複製到另](tutorial--copying-asf-streams-from-one-file-to-another.md)一個檔案。

## <a name="post-packet-generation-calls"></a>Post Packet-Generation 呼叫

若要確定沒有任何完整的資料封包正在等候多工器，請呼叫 [**IMFASFMultiplexer：： Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush)。 這會強制多工器 packetize 正在進行中的所有媒體範例。 應用程式可以透過 **GetNextPacket** 在迴圈中以媒體範例的形式收集這些封包，直到沒有其他要抓取的封包為止。

產生所有媒體範例之後，請呼叫 [**IMFASFMultiplexer：： End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) 以更新與這些資料封包相關聯的 ASF 標頭物件。 標頭物件是藉由傳遞用來初始化多工器的 ContentInfo 物件來指定。 此呼叫會更新不同的標頭物件，以反映在資料封包產生期間由多工器所做的變更。 這項資訊包括封包計數、傳送持續時間、播放持續時間，以及所有資料流程的串流號碼。 整體的標頭大小也會更新。

您必須確保在抓取所有資料封包之後呼叫 [**End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) 。 如果有任何封包在多工器中等候， **End** 將會失敗，並傳回 **MF \_ E \_ FLUSH \_ 需要** 的錯誤碼。 在此情況下，請在迴圈中呼叫 [**Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) 和 [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) ，以取得等候封包。

> [!Note]  
> 針對 VBR 編碼，在呼叫 **End** 之後，您必須在 ContentInfo 物件的編碼屬性中設定編碼統計資料。 如需此程式的詳細資訊，請參閱在 [ContentInfo 物件中設定屬性](setting-properties-in-the-contentinfo-object.md)（property）中的「使用編碼器設定來設定 ContentInfo 物件」。 下列清單顯示要設定的特定屬性：
>
> -   [**MFPKEY \_RAVG**](mfpkey-ravgproperty.md) 是 VBR 內容的平均位元速率。
> -   [**MFPKEY \_BAVG**](mfpkey-bavgproperty.md) 是平均位元速率的緩衝區視窗。
> -   [**MFPKEY \_RMAX**](mfpkey-rmaxproperty.md) 是 VBR 內容的尖峰位元速率。
> -   [**MFPKEY \_BMAX**](mfpkey-bmaxproperty.md) 是尖峰緩衝區視窗。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 多工器](asf-multiplexer.md)
</dt> <dt>

[教學課程：將 ASF 資料流程從一個檔案複製到另一個檔案](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[教學課程：使用 CBR 編碼方式撰寫 WMA 檔案](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



