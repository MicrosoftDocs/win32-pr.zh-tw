---
title: 使用同步讀取器讀取檔案
description: 使用同步讀取器讀取檔案
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows媒體格式 SDK，讀取檔案
- Windows媒體格式 SDK，同步讀取器
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- Advanced Systems Format (ASF) ，讀取檔案
- ASF (Advanced Systems Format) ，讀取檔案
- 同步讀取器，IWMReaderCallback 介面
- IWMReaderCallback，同步讀取器
- 同步讀取器，讀取檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c30ed2f9af78c9643f269adb24f740f2fe9227bc2e5b8a36d5c9d29606564176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197470"
---
# <a name="reading-files-with-the-synchronous-reader"></a>使用同步讀取器讀取檔案

您可以使用同步讀取器，以使用同步呼叫來讀取 ASF 檔案，而不是讀取器物件中的非同步方法。 使用同步呼叫可減少讀取檔案所需的執行緒數目。 非同步讀取器會使用多個執行緒來處理資料流程。 針對具有多個資料流程的檔案，使用的執行緒數目可能會變得非常大。 同步讀取器只會使用一個執行緒。

同步讀取器的設計目的是為了滿足內容建立和檔案編輯應用程式的需求。 您可以針對其他應用程式使用同步讀取器，但其功能有限。

同步讀取器可以使用 UNC 路徑名稱 (例如 " \\ \\ someshare \\ somedirectory \\ somefile.txt 之 .wmv" ) ，開啟本機檔案或網路上的檔案。 您無法將檔案串流至同步讀取器，或從網際網路位置開啟檔案。 同步讀取器也提供使用 **IStream** COM 介面作為來源的支援。

同步讀取器提供比非同步讀取器更能從 ASF 檔案抓取樣本的更多功能。 同步讀取器可以依串流號碼和輸出來傳遞範例。 您可以壓縮或解壓縮串流號碼所傳遞的範例。 同步讀取器也可以在播放期間于壓縮和未壓縮的傳遞之間切換;這項功能稱為「快速編輯」。 這項功能可讓編輯應用程式讀取 Windows 媒體內容，並將它直接傳遞至寫入器，直到到達所需的框架為止。 屆時，應用程式可以告訴讀者開始傳遞未壓縮的內容，讓應用程式可以修改並傳遞給 recompression 的寫入器。 當應用程式完成修改指定的框架時，它可以告訴讀者再次開始傳遞壓縮的框架。

同步讀取器物件的最基本功能可以細分為下列步驟。 在這些步驟中，「應用程式」是指您使用 Windows 媒體格式 SDK 撰寫的程式。

1.  應用程式會將要讀取的檔案名傳遞給同步讀取器。 當同步讀取器開啟檔案時，它會將輸出編號指派給每個資料流程。 如果檔案使用相互排除，讀取器會為所有互斥資料流程指派單一輸出。
2.  應用程式會從讀取器取得各種輸出的設定相關資訊。 收集的資訊將可讓應用程式正確地轉譯媒體範例。
3.  應用程式會一次從同步讀取器開始要求範例。 同步讀取器會以緩衝區物件傳遞 [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) 介面的每個範例。
4.  應用程式會在讀取器傳遞之後，負責呈現資料。 Windows 媒體格式 SDK 不提供任何轉譯常式。 一般而言，應用程式會使用其他 sdk 來轉譯資料，例如 microsoft Direct X SDK 或 microsoft Windows Platform SDK 的多媒體功能。

這些步驟說明于 WMSyncReader 範例應用程式中。 如需詳細資訊，請參閱 [範例應用程式](sample-applications.md)。

同步讀取器也支援更先進的功能。 同步讀取器可讓您執行下列作業：

-   指定要依時間或依畫面格編號取出的樣本範圍。
-   適用于互斥資料流程的控制資料流程選取範圍。
-   使用標準 COM 介面、 **IStream** 來開啟檔案。
-   讀取檔案標頭中的設定檔資料。
-   從檔案標頭讀取中繼資料。
-   在播放期間于資料流程和輸出範例之間切換。
-   在播放期間于壓縮和未壓縮的串流範例之間切換。

下列各節將詳細說明同步讀取器物件的使用方式。

-   [建立同步讀取器並開啟檔案](to-create-a-synchronous-reader-and-open-a-file.md)
-   [尋找資料流程號碼和輸出編號](to-find-stream-numbers-and-output-numbers.md)
-   [使用同步讀取器取出媒體範例](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [使用同步讀取器依時間進行搜尋](to-seek-by-time-using-the-synchronous-reader.md)
-   [使用同步讀取器依框架編號搜尋](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [使用同步讀取器依 SMPTE 時間碼進行搜尋](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [使用同步讀取器取出資料流程範例](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [使用同步讀取器取出壓縮的範例](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

**範例程式碼**

下列範例程式碼示範如何使用同步讀取器從 ASF 檔案讀取範例。 它會依框架編號指定要傳遞的範例範圍。


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMSyncReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**讀取 ASF 檔案**](reading-asf-files.md)
</dt> <dt>

[**同步讀取器物件**](synchronous-reader-object.md)
</dt> </dl>

 

 




