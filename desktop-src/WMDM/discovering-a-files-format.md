---
title: 探索檔案的格式
description: 探索檔案的格式
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows媒體裝置管理員，檔案格式
- 裝置管理員，檔案格式
- 程式設計指南，檔案格式
- 桌面應用程式，檔案格式
- 建立 Windows 媒體裝置管理員應用程式、檔案格式
- 將檔案寫入裝置、檔案格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83706a3026968a694d3629551d310db9021b7f8c8118f3d98621751a95af26b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585327"
---
# <a name="discovering-a-files-format"></a>探索檔案的格式

將檔案傳送至裝置之前，應用程式應判斷裝置是否支援該檔案格式。

探索檔案的格式可能很複雜。 最簡單的方式是建立對應至特定 WMDM \_ FORMATCODE 列舉值的副檔名清單。 不過，這個系統有幾個問題：一個是單一格式可以有多個延伸模組 (例如 .jpg、jpe 和 jpeg 影像) 。 此外，不同的程式可以使用相同的副檔名來進行不同的格式。

若要克服嚴格對應的限制，應用程式最好驗證格式是否符合延伸模組。 DirectShow SDK 所提供的工具，可讓應用程式探索大部分媒體檔案類型的一組有限詳細資料。 Windows 媒體格式 SDK 會公開大量的詳細資料，但只會顯示最多 ASF 檔。 因為所有檔案類型應該盡可能驗證其格式程式碼，所以最好使用 DirectShow 來探索或驗證基本格式程式碼，然後使用 Windows 媒體格式 SDK 來探索任何其他有關 ASF 檔案的中繼資料。 DirectShow 也可以用來探索非 ASF 檔案的基本中繼資料。

以下是使用延伸模組對應和 DirectShow 探索檔案格式的其中一種方式。

首先，將副檔名與已知的副檔名清單進行比較。 務必讓您的比較不區分大小寫。 如果延伸模組未對應，請將格式設定為 WMDM \_ FORMATCODE \_ UNDEFINED。

-   如果找不到格式代碼 (或您想要確認檔案是) 的媒體檔案，您可以執行下列步驟：
    1.  使用 **CoCreateInstance** (CLSID MediaDet) 建立 DirectShow 媒體偵測器物件 \_ ，並取出 **IMediaDet** 介面。
    2.  藉由呼叫 **IMediaDet：:p 的檔案 \_ 名稱** 來開啟檔案。 如果檔案受到保護，此呼叫將會失敗。
    3.  藉由呼叫 **IMediaDet：： get \_ StreamMediaType**（傳回 **AM \_ 媒體 \_ 類型**）來取得預設資料流程的媒體類型。
    4.  藉由呼叫 **IMediaDet：： get \_ OutputStreams** 取得資料流程的數目。
        -   如果只有一個資料流程而且是音訊，則檔案類型會是 WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO
        -   如果只有一個資料流程而且是影片，則檔案類型會是 WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO
        -   如果只有一個資料流程而且是影片，而且位元速率為零，則檔案類型會是 WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT。

您也可以嘗試比對取自 **get \_ StreamMediaType** 的 **VIDEOINFOHEADER** 或 **WAVEFORMATEX** 成員的音訊或影片編解碼器。

下列 c + + 函式會示範副檔名比對，並使用 DirectShow 來嘗試分析未知的檔案。


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將檔案寫入至裝置**](writing-files-to-the-device.md)
</dt> </dl>

 

 




