---
title: 廣播 ASF 資料
description: 廣播 ASF 資料
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Media Format SDK，廣播 ASF 資料
- Advanced Systems Format (ASF) ，廣播資料
- ASF (Advanced Systems Format) ，廣播資料
- Windows Media Format SDK，傳送 ASF 資料
- Advanced Systems Format (ASF) ，傳送資料
- ASF (Advanced Systems Format) ，傳送資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104023151"
---
# <a name="broadcasting-asf-data"></a>廣播 ASF 資料

本主題說明如何使用 HTTP 通訊協定，在網路上傳送 ASF 資料。 透過網路傳送檔案需要使用寫入器物件，因此在閱讀本主題之前，您應該先對此物件有大致的瞭解。 如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。

如果您要開始使用未壓縮的資料，請執行下列動作：

1.  藉由呼叫 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函數來建立寫入器物件。 此函數會傳回 **IWMWriter** 指標。
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  藉由呼叫 [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) 函式來建立網路接收器物件，該函式會傳回 **IWMWriterNetworkSink** 指標。
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  在網路接收上呼叫 [**IWMWriterNetworkSink：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) ，並指定要開啟的埠號碼。例如，8080。 （選擇性）呼叫 [**IWMWriterNetworkSink：： GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) 以取得主機的 URL。 用戶端會存取此 URL 的內容。 您也可以呼叫 [**IWMWriterNetworkSink：： SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) 來限制用戶端數目。
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  在寫入器上呼叫 [**IWMWriterAdvanced：： AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) ，並使用網路接收器的 **IWMWriterNetworkSink** 介面指標，以將網路接收器附加至寫入器。
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  在寫入器物件上呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) 方法，並使用 [**IWMProfile**](iwmprofile.md) 指標來設定 ASF 設定檔。 如需建立設定檔的詳細資訊，請參閱 [使用設定檔](working-with-profiles.md)。
6.  （選擇性）使用寫入器上的 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 介面來指定中繼資料。
7.  在寫入器上呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) 。
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  針對每個範例，呼叫 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) 方法。 指定串流號碼、展示時間、樣本的持續時間，以及範例緩衝區的指標。 **WriteSample** 方法會壓縮範例。
9.  當您完成時，請在寫入器上呼叫 [**IWMWriter：： EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) 。
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. 在寫入器上呼叫 [**IWMWriterAdvanced：： RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) ，以卸離網路接收器物件。
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. 在網路接收上呼叫 [**IWMWriterNetworkSink：： Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) 以釋放埠。
    ```C++
    hr = pNetSink->Close();
    ```

    

透過網路串流 ASF 內容的另一種方式，是從現有的 ASF 檔案讀取該內容。 SDK 中提供的 WMVNetWrite 範例會示範這種方法。 除了先前所列的步驟之外，請執行下列動作：

1.  建立讀取器物件，並使用檔案的名稱來呼叫 **Open** 方法。
2.  針對 reader 物件呼叫 [**IWMReaderAdvanced：： SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) ，並將值 **設為 TRUE**。 這可讓應用程式讀取檔案中的每個資料流程，包括具有相互排除的資料流程。
3.  查詢 [**IWMProfile**](iwmprofile.md) 介面的讀取器。 當您在寫入器物件上呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) 時，請使用這個指標， (上一個程式中的步驟 5) 。
4.  針對設定檔中定義的每個資料流程，呼叫 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) 來取得資料流程號碼。 將此串流號碼傳遞給讀取器的 [**IWMReaderAdvanced：： SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) 方法。 這個方法會通知讀者傳遞壓縮的範例，而不是解碼它們。 這些範例會透過應用程式的 [**IWMReaderCallbackAdvanced：： OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) 回呼方法傳遞至應用程式。

    您必須為每個已解壓縮的資料流程取得編解碼器資訊，並在廣播之前將它新增至標頭。 若要取得編解碼器資訊，請呼叫 [**IWMHeaderInfo2：： GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) 和 [**IWMHeaderInfo2：： GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) ，以列舉讀取器中與檔案相關聯的編解碼器。 選取符合資料流程設定的編解碼器資訊。 然後藉由呼叫 [**IWMHeaderInfo3：： AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)來設定寫入器中的編解碼器資訊，傳遞從讀取器取得的資訊。

5.  在寫入器上設定設定檔之後，請在寫入器上呼叫 [**IWMWriter：： GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) 來取得輸入的數目。 針對每個輸入，呼叫 [**IWMWriter：： SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) ，其值 **為 Null**。 這會向寫入器物件表示應用程式會提供壓縮的範例，因此寫入器不需要使用任何編解碼器來壓縮資料。 呼叫 **BeginWriting** 之前，請務必先呼叫 **SetInputProps** 。
6.  （選擇性）將中繼資料屬性從讀取器複製到寫入器。
7.  由於讀取器的範例已經壓縮，因此請使用 [**IWMWriterAdvanced：： WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) 方法來撰寫範例，而不是 **WriteSample** 方法。 **WriteStreamSample** 方法會略過寫入器物件的一般壓縮程式。
8.  當讀取器到達檔案結尾時，會將 WMT \_ EOF 通知傳送至應用程式。

此外，應用程式應該會驅動讀取器物件上的時鐘，讓讀取器儘快從檔案提取資料。 若要這樣做，請在讀取器上呼叫 [**IWMReaderAdvanced：： SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) 方法，並將值 **設為 TRUE**。 當讀取器 \_ 傳送 WMT 啟動通知之後，請呼叫 [**IWMReaderAdvanced：:D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) ，並指定讀取器應提供的時間間隔。 讀取器完成此時間間隔之後，它會呼叫應用程式的 [**IWMReaderCallbackAdvanced：： OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) 回呼方法。 應用程式應該再次呼叫 **DeliverTime** ，以讀取下一個時間間隔。 例如，若要以一秒的間隔讀取檔案：


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**透過網路傳送 ASF 資料**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**使用寫入器接收器**](working-with-writer-sinks.md)
</dt> </dl>

 

 




