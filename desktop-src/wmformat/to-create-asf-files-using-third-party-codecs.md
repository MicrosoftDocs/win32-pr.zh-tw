---
title: 使用協力廠商編解碼器建立 ASF 檔案
description: 使用協力廠商編解碼器建立 ASF 檔案
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- Windows媒體格式 SDK，建立 ASF 檔案
- Windows媒體格式 SDK，協力廠商編解碼器
- Advanced Systems Format (ASF) ，建立檔案
- ASF (Advanced Systems Format) ，建立檔案
- Advanced Systems Format (ASF) ，協力廠商編解碼器
- ASF (Advanced Systems Format) ，協力廠商編解碼器
- 協力廠商編解碼器
- 編解碼器，協力廠商
- 編解碼器，建立 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1eeeb891037581a550d8c15c2f2b4cefa14f81f20d0d55623d382d0e933e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197077"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a>使用協力廠商編解碼器建立 ASF 檔案

您可以使用 Windows 媒體格式 SDK 來建立 ASF 檔案，其中包含以您選擇的任何編解碼器編碼的數位媒體。 使用此 SDK 隨附的編解碼器時，您必須執行下列步驟。

1.  使用所需的編解碼器將內容編碼。
2.  尋找或建立 GUID 值，以識別使用步驟1中所用編解碼器編碼的內容。
3.  建立新的設定檔，或修改現有的設定檔以搭配編碼的內容使用。
    -   使用適當的主要類型建立編碼內容的資料流程。 如需主要媒體類型的詳細資訊，請參閱 [媒體類型](media-types.md)。 使用步驟2中識別的 GUID 作為媒體子類型。
    -   將資料流程的位元速率和緩衝區視窗設定為不會產生緩衝區溢位的值。 編碼時，您應該能夠從編解碼器取得這些值。 SDK 執行時間元件會檢查位元速率/緩衝區視窗值，並視需要卸載範例，以使指定的資料符合這些值。 如果您不正確地設定這些值，檔案將無法正確地進行串流，因而導致播放不良。
    -   針對影片資料流程，您必須將 [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)結構中所包含之 **BITMAPINFOHEADER** 結構的 **biCompression** 成員設定為內容的適當 FOURCC 值。 此值必須等於子類型 GUID 的前四個位元組。 例如，如果 **biCompression** 是 MAKEFOURCC ( t '、' E '、'，t ' ) = 0x54455354，則子類型 GUID 的開頭會像這樣： 54455354-xxxx。
4.  建立寫入器物件，並載入在上一個步驟中建立的設定檔。 如需寫入檔案的詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。
5.  在檔案的輸入之間執行迴圈，並為每個檔案指派輸入屬性。 如需輸入的詳細資訊，請參閱 [使用輸入](working-with-inputs.md)。 若為使用協力廠商編解碼器編碼的資料流程，請在呼叫 [**IWMWriter：： BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)之前，將 [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)介面指標設定為 **Null** 。
6.  使用在上一個步驟中建立的新設定檔來寫入檔案。 使用 [**IWMWriterAdvanced：： WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) 傳遞壓縮的範例，而不是 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)。 針對影片，您必須將 WM \_ SF \_ CLEANPOINT 傳遞為 *dwFlags* 參數，以指定哪些範例是主要畫面格。

若要處理和解壓縮以協力廠商編解碼器編碼的資料流程，您必須閱讀壓縮的資料流程範例。 您的讀取應用程式也必須處理資料流程的解壓縮範例。

## <a name="putting-mpeg-2-streams-into-asf"></a>將 MPEG 2 串流放入 ASF

> [!Note]  
> 本主題適用于使用 Windows 媒體格式 SDK 的應用程式，可將使用 B 框架) 的 mpeg-2 (或其他壓縮格式放置於 ASF 檔案容器中。

 

寫入器物件要求所有輸入範例都必須有時間戳記，並假設每個輸入範例的呈現時間晚于其之前的呈現時間。 雖然幾乎所有未壓縮的影片，甚至某些壓縮的影片串流都符合這些條件，但 MPEG-2 資料流程並不會。 在 MPEG 2 中，並非所有樣本都有時間戳記，而當 B 框架存在時，範例解碼順序與轉譯順序不同。 當寫入器物件遇到無法排序的範例時，它會將它們重新排列成「正確」的順序。 因此，若要將 MPEG-2 資料流程原生 (未解碼) 在 ASF 容器中，您必須執行下列步驟：

寫入檔案時：

1.  將固定大小的資料單位延伸 () 至每個輸入範例，此範例會保存包含範例之實際 MPEG 時間戳記開始時間和停止時間值的結構。 如果樣本沒有時間戳記，請針對這些值使用-1。
2.  提供寫入器物件「虛設」輸入時間戳記，一律會不斷增加，以便將範例以完全相同的順序寫入至檔案。 虛擬時間戳記應該大約對應到實際的呈現時間，如一段時間的平均值。 虛擬時間戳記會形成搜尋時間軸，因此，如果它們相對於即時戳記，則搜尋檔案上的作業將會產生非預期的結果。 不過，取樣時間之間的抖動量不會嚴重影響搜尋作業。

讀取檔案時：

-   針對從檔案讀取的每個範例，檢查是否已到期。 如果它包含大於或等於零的開始時間，請將該值複製到輸出範例的時間戳記，然後再傳遞給解碼器。 將輸出範例上的所有其他時間戳記設為 **Null**。 在 DirectShow 中，藉由呼叫 **IMediaSample：： SetTime** (**null**、**null**) 來完成此動作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**緩衝處理內容**](buffering-content.md)
</dt> <dt>

[**IWMWriter 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**IWMWriterAdvanced 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**使用非同步讀取器傳遞壓縮的範例**](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**使用同步讀取器取出資料流程範例**](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> <dt>

[**寫入 ASF 檔案**](writing-asf-files.md)
</dt> </dl>

 

 




