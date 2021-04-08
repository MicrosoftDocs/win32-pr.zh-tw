---
description: 從現有的 ASF 資料物件產生資料流程範例
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: 從現有的 ASF 資料物件產生資料流程範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111768"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a>從現有的 ASF 資料物件產生資料流程範例

ASF *分隔器* 物件是 WMContainer 層元件，可剖析 Advanced Systems 格式的 Asf 資料物件 (asf) 檔。

將資料封包傳遞給分隔器之前，應用程式必須在分隔器上初始化、設定和選取資料流程，才能為剖析程式做好準備。 如需詳細資訊，請參閱 [建立 Asf 分隔器物件](creating-the-asf-splitter-object.md) 和設定 [Asf 分隔器物件](configuring-the-asf-splitter-object.md)。

剖析 ASF 資料物件所需的方法如下：

-   [**IMFASFSplitter：**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) 將包含資料封包的緩衝區推送至分隔器，以啟動剖析程式的:P arsedata。
-   [**IMFASFSplitter：： GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) ，可收集從傳遞給分隔器的緩衝區產生的資料流程範例。

## <a name="finding-the-data-offset"></a>尋找資料位移

開始剖析程式之前，應用程式必須在 ASF 檔案內找出資料物件。 有兩種方式可從檔案的開頭取得資料物件的位移：

-   在初始化 ContentInfo 物件之前，您可以呼叫 [**IMFASFContentInfo：： GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) 方法。 此方法需要包含 ASF 標頭前30個位元組的緩衝區。 它會傳回整個標頭的大小，表示第一個資料封包的位移。 此值也包含資料物件標頭大小50個位元組。
-   初始化 ContentInfo 物件之後，您可以藉由呼叫 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)來取得簡報描述項，然後查詢適用于 [**MF \_ PD \_ ASF \_ 資料 \_ 起始 \_ 位移**](mf-pd-asf-data-start-offset-attribute.md) 屬性的簡報描述項。 這個屬性的值是標頭大小。
    > [!Note]  
    > 展示描述項上的 [ [**MF \_ PD \_ ASF \_ 資料 \_ 長度**](mf-pd-asf-data-length-attribute.md) ] 屬性會指定 ASF 資料物件的長度。

     

在這兩種情況下，傳回的值是標頭物件的大小加上資料物件的標頭區段大小。 因此，產生的值是 ASF 資料物件中資料封包開頭的位移。 當您開始將資料傳送到分隔器時，資料必須從 ASF 檔案開頭的這個位移開始。

位移值會以參數的形式傳遞至 **ParseData** ，以啟動剖析程式。

資料物件會分割成資料封包。 每個資料封包都包含一個資料封包標頭，以提供封包剖析資訊和承載資料—實際的數位媒體資料。 在搜尋案例中，應用程式可能會想要讓分隔器開始在特定的資料封包上進行剖析。 若要這樣做，您可以使用 ASF 索引子來取得位移。 索引子會傳回從封包界限開始的位移值。 如果您不是使用索引子，請確定位移是從資料封包標頭的開頭開始。 如果將不正確位移傳遞給分隔器，例如值沒有指向封包界限， **ParseHeader** 和 **GetNextSample** 呼叫會成功，但 **GetNextSample** 不會取出任何範例，且 *pSample* 參數中會收到 **Null** 。

如果分隔器已設定為以反向方向進行剖析，則分隔器一律會在傳遞至 **ParseData** 之媒體緩衝區的結尾處開始剖析。 因此，若要在呼叫 **ParseData** 時進行反向剖析，請在 *cbLength* 參數中傳遞位移，這會指定資料的長度，並將 *cbBufferOffset* 設定為零。

## <a name="generating-samples-for-asf-data-packets"></a>產生 ASF 資料封包的範例

應用程式會將資料封包傳遞給分隔器，以啟動剖析程式。 分隔器的輸入是一系列的媒體緩衝區，其中包含資料物件的整個或片段。 分隔器的輸出是一系列包含封包資料的媒體範例。

若要將輸入資料傳遞給分隔器，請建立媒體緩衝區，並使用 ASF 檔案的資料物件區段中的資料填入該緩衝區。  (如需媒體緩衝區的詳細資訊，請參閱 [媒體緩衝區](media-buffers.md)。 ) 然後將媒體緩衝區傳遞給 [**IMFASFSplitter：:P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) 方法。 您也可以指定：

-   緩衝區中分隔器應開始剖析的位移。 如果位移為零，則會從緩衝區開頭開始剖析。 如需設定資料位移的詳細資訊，請參閱本主題中的「尋找資料位移」一節。
-   要剖析的資料量。 如果這個值為零，則分隔器會剖析，直到到達緩衝區的結尾，如 [**IMFMediaBuffer：： GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) 方法所指定。

分隔器會藉由參考媒體緩衝區中的資料來產生媒體範例。 用戶端可以藉由在迴圈中呼叫 [**IMFASFSplitter：： GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) 來取出輸出範例，直到沒有其他資料可剖析為止。 如果 **GetNextSample** \_ \_ 在 *pdwStatusFlags* 參數中傳回 ASF STATUSFLAGS 不完整旗標，則表示有更多要抓取的範例，而且應用程式可以再次呼叫 **GetNextSample** 。 否則，呼叫 **ParseData** 以將更多資料傳遞給分隔器。 針對產生的範例，分隔器會設定下列資訊：

-   分割器會針對它所產生的所有樣本設定時間戳記。 取樣時間代表表示時間，不包括預先執行的時間。 應用程式可以呼叫 [**IMFSample：： GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) 來取得呈現時間，以 100-毫微秒單位表示。
-   如果在產生範例期間發生中斷，則分隔器會在不連續的第一個範例上設定 [**MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md) 中斷屬性。 不連續通常是因為網路連線上的封包、損毀的檔案資料或分隔器切換到另一個來來源資料流所造成。
-   針對影片，分隔器會檢查範例是否包含主要畫面格。 如果有的話，分隔器會在範例上設定 [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) 屬性。

如果分隔器正在剖析從媒體伺服器接收的資料封包，封包長度可能是可變的。 在此情況下，用戶端必須針對每個封包呼叫 **ParseData** ，並在傳送到分隔器的每個緩衝區上設定 MFASFSPLITTER 的封 [**\_ 包 \_ 界限**](mfasfsplitter-packet-boundary-attribute.md) 屬性。 這個屬性會向分隔器指出媒體緩衝區是否包含 ASF 封包的開頭。 如果緩衝區包含新封包的開頭，請將屬性設定為 **TRUE** 。 如果緩衝區包含前一個封包的接續，請將屬性設定為 **FALSE**。 緩衝區無法跨越多個封包。

將新的媒體緩衝區傳遞給分隔器之前，應用程式必須呼叫 [**IMFASFSplitter：： Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush)。 這個方法會重設分割器，並清除等候完成的任何部分框架。 這在搜尋案例中很有用，因為該案例的位移位於不同的位置。

### <a name="example"></a>範例

下列程式碼範例顯示如何剖析資料封包。 此範例會從資料物件的開頭到資料流程的結尾進行剖析，並顯示包含主要畫面格之範例的相關資訊。 如需使用此程式碼的完整範例，請參閱 [教學課程：讀取 ASF](tutorial--reading-an-asf-file.md)檔。


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF 分隔器](asf-splitter.md)
</dt> </dl>

 

 



