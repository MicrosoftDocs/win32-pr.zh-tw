---
description: 步驟3會執行 Frame-Grabbing 函式
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: 步驟3會執行 Frame-Grabbing 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97f585ff365e40ec611a9e11ce365839aa87be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850972"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a>步驟3：執行 Frame-Grabbing 函式

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

本主題是 [抓取海報框架](grabbing-a-poster-frame.md)的步驟3。

下一步是執行 GetBitmap 函式，此函式會使用媒體偵測器來抓取海報框架。 在此函數中，執行下列步驟：

1.  建立媒體偵測器。
2.  指定媒體檔案。
3.  檢查檔案中的每個資料流程。 如果是影片串流，請取得影片的原生維度。
4.  取得海報框架，並指定搜尋時間和目標維度。

藉由呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立媒體偵測器物件：


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



使用 [**IMediaDet：:p 內容 \_ 名稱方法**](imediadet-put-filename.md) 指定檔案名。 這個方法會採用 **BSTR** 參數。


```C++
hr = pDet->put_Filename(bstrFilename);
```



取得資料流程的數目，並對每個檢查媒體類型的資料流程執行迴圈。 [**IMediaDet：： get \_ OutputStreams**](imediadet-get-outputstreams.md)方法會抓取資料流程的數目，而 [**IMediaDet：:p 的內容 \_ CurrentStream**](imediadet-put-currentstream.md)方法會指定要檢查的資料流程。 結束第一個影片串流上的迴圈。


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



如果找不到任何影片資料流程，則函式會結束。

在先前的程式碼中， [**IMediaDet：： get \_ StreamType**](imediadet-get-streamtype.md) 方法只會傳回主要類型 GUID。 如果您不需要檢查完整的媒體類型，這會很方便。 不過，若要取得影片尺寸，必須檢查格式區塊，因此需要完整的媒體類型。 您可以藉由呼叫 [**IMediaDet：： get \_ StreamMediaType**](imediadet-get-streammediatype.md) 方法來取得，此方法會填入 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。 媒體偵測器會使用 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式區塊，將所有影片串流轉換成未壓縮的格式。


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



[**Get \_ StreamMediaType**](imediadet-get-streammediatype.md)方法會配置呼叫端必須釋放的格式區塊。 這個範例會使用基類庫中的 [**FreeMediaType**](freemediatype.md) 函式。

現在您已準備好取得海報框架。 先呼叫 [**IMediaDet：： GetBitmapBits**](imediadet-getbitmapbits.md) 方法以及緩衝區的 **Null** 指標：


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



此呼叫會在 *lSize* 參數中傳回所需的緩衝區大小。 第一個參數指定要搜尋的資料流程時間;這個範例會使用時間零。 針對寬度和高度，此範例會使用稍早取得的原生影片維度。 如果您指定其他值，媒體偵測器會延展點陣圖使其相符。

如果方法成功，請配置緩衝區，並再次呼叫 [**GetBitmapBits**](imediadet-getbitmapbits.md) ：


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



以下是完整的函式，有更好的錯誤處理。


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



下一 [步：步驟4：在工作區上繪製點陣圖](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[抓取海報框架](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
