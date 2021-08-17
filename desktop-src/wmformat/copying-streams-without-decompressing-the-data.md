---
title: 複製資料流程而不解壓縮資料
description: 複製資料流程而不解壓縮資料
ms.assetid: c268ce44-a09d-4304-bc39-8b6657da2bdb
keywords:
- Windows媒體格式 SDK，複製資料流程
- Advanced Systems Format (ASF) ，複製資料流程
- ASF (Advanced Systems Format) ，複製資料流程
- 串流，不需要解壓縮資料即可複製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2387861c25ad565298fb2731300f6da8ccc00c26c5f7c82c36fede1bb7f62f9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931558"
---
# <a name="copying-streams-without-decompressing-the-data"></a>複製資料流程而不解壓縮資料

將資料流程從一個檔案複製到另一個檔案的最簡單且最常見的方式，是以其壓縮狀態取出範例，然後將它們寫入至新檔案，而不需要解壓縮和 recompressing。 從檔案以其壓縮狀態取得的範例稱為資料流程範例，因為它們不會從資料流程中的表示方式改變。 建議您一律使用串流範例來複製資料流程，因為解壓縮和 recompressing 數位媒體資料會降低品質。 如果您必須從解壓縮的資料複製資料流程，請參閱 [使用解壓縮的範例複製資料流程](copying-streams-using-decompressed-samples.md)。

您可以使用壓縮的範例將兩個或多個資料流程串連成單一資料流程，但只有在位元速率相同的情況下。 此程式基本上與下面所述的步驟相同，不同之處在于您必須讀取多個原始檔案，才能取得所需的所有內容。 但是，如果 **WM \_ 媒體 \_ 類型** 結構 (包括所有壓縮資料流程的所有 **pbFormat** 結構成員) 相同，則您只能將來自多個檔案的壓縮範例寫入至單一資料流程。 若要合併來自不同格式之多個資料流程的資料，您必須將內容解壓縮並重新壓縮成目的地資料流程。 此外，當您將兩個或多個資料流程中的資料結合成單一資料流程時，您必須將所有資料流程的緩衝區視窗值同時加入，以取得新資料流程的緩衝區視窗。 這是因為無法判斷在一個資料流程結尾和另一個資料流程的開頭，會佔用多少緩衝區。

您可以使用 [**IWMReaderAdvanced：： SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples)，以非同步讀取器抓取資料流程範例。 資料流程範例會傳遞至 [**IWMReaderCallbackAdvanced：： OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample)，而不是 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)。 如果您要讀取檔案，並取出壓縮的部分資料流程和解壓縮的部分，您必須同時執行兩個回呼方法。

同步讀取器提供更大的彈性來抓取範例。 您可以使用 [**IWMSyncReader：： SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples)，在播放期間自由地在壓縮和解壓縮的範例之間切換。

若要將整個資料流程從一個 ASF 檔案複製到新的 ASF 檔案，請執行下列步驟。 這些步驟會使用同步讀取器，因為這類作業更容易使用。

1.  藉由呼叫 [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) 函數來建立同步讀取器物件。
2.  呼叫 [**IWMSyncReader：： open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open)，在讀取器中開啟檔案。
3.  藉由呼叫 **IWMSyncReader：： QueryInterface**，取得同步讀取器物件之 [**IWMProfile**](iwmprofile.md)介面的指標。
4.  藉由呼叫 [**IWMProfile：： GetStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber)來取出所需資料流程的屬性。 這會針對您想要的資料流程，取得資料流程設定物件之 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) 介面的指標。
5.  取得資料流程的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構複本。 對 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)進行兩個呼叫，以取得結構的大小，第二個呼叫取得結構本身。
6.  藉由呼叫 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函數來建立配置檔案管理員物件。
7.  呼叫 [**IWMProfileManager：： CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) 來建立新的設定檔 (或開啟您要新增串流) 的現有設定檔。 在新的設定檔上呼叫 [**IWMProfile：： AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) ，以從現有的檔案新增串流。 新增資料流程時，請使用在步驟4中取得的 **IWMStreamConfig** 指標。
8.  使用 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函數的呼叫來建立寫入器物件。 藉由呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)，將新建立的設定檔設定為寫入器中的使用中設定檔。 藉由呼叫 [**IWMWriter：： SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename)來建立輸出的檔案。
9.  針對與您要複製的資料流程或資料流程相關聯的每個輸入，呼叫 [**IWMWriter：： SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops)，並針對 [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)介面傳遞 **Null** 。 這會通知寫入器物件，它不需要驗證您所傳遞的資料。 您必須在呼叫 **BeginWriting** (步驟 14) 之前進行此呼叫，否則讀取物件可能無法將內容解碼。
10. 藉由呼叫 [**IWMSyncReader：： SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) ，並將 *fCompressed* 參數設為 True，將同步讀取器設定為傳遞所選資料流程的壓縮資料流程範例。
11. 針對每個要複製的資料流程取得編解碼器資訊，並在寫入之前將編解碼器資訊新增至標頭。 若要取得編解碼器資訊，請呼叫 [**IWMHeaderInfo2：： GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) 和 [**IWMHeaderInfo2：： GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) ，以列舉讀取器中與檔案相關聯的編解碼器。 選取符合資料流程設定的編解碼器資訊。 然後藉由呼叫 [**IWMHeaderInfo3：： AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)來設定寫入器中的編解碼器資訊，傳遞從讀取器取得的資訊。
12. 藉由呼叫 **IWMWriter：： QueryInterface** 來取得 [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)介面的指標。
13. 藉由呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)，將寫入器設定為寫入模式。
14. 重複呼叫 [**IWMSyncReader：： GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)，並指定所需的資料流程號碼。 收到範例時，請使用 [**IWMWriterAdvanced：： WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample)的呼叫將它們傳遞給寫入器。 若為影片資料流程，您應該檢查旗標 (是否在每次呼叫 **GetNextSample** 時，由寫入器所設定的任何) 。 如果 \_ \_ 設定了 WM SF CLEANPOINT，您也必須在呼叫 **WriteStreamSample** 時加以設定。
15. 當讀取完成時，請呼叫 [**IWMWriter：： EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting)。 應傳送資料流程。

> [!Note]  
> 使用資料流程範例時，無法從某個檔案將影像資料流程複製到另一個檔案。 若要複製影像資料流程資料，請取出未壓縮的範例，然後以平常的方式透過寫入器進行處理。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將資料從一個檔案複製到另一個檔案**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**使用解壓縮的範例複製資料流程**](copying-streams-using-decompressed-samples.md)
</dt> </dl>

 

 




