---
description: 從文字筆墨物件轉換的執行 (tInk) 為筆跡。
ms.assetid: 9365da4c-3667-49f0-838f-f099d28dab44
title: 將文字筆墨物件轉換成筆墨
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef543fda3ed53123e99ee042aed67af9cedfef3533ae47bc40d8dd284a73675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941158"
---
# <a name="converting-a-text-ink-object-to-ink"></a>將文字筆墨物件轉換成筆墨

從文字筆墨物件轉換的執行 (tInk) 為筆跡。

## <a name="to-convert-from-a-text-ink-object-to-ink"></a>從文字筆墨物件轉換成筆墨

1.  使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 介面將文字筆跡物件的內容寫出至資料流程。 文字筆墨物件使用筆墨序列化格式來寫入資料流程。
2.  將資料流程的內容讀取至位元組陣列。
3.  使用 [**InkDisp**](inkdisp-class.md) 物件的 [**load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) 方法，將資料流程的內容載入至 **InkDisp** 物件。

## <a name="text-ink-object-to-ink-object-example"></a>文字筆墨物件至筆墨物件範例

下列程式碼片段會將文字筆墨物件轉換成筆墨。

首先，程式碼會取得文字筆墨物件。


```C++
/* Create a variable to hold the text ink object */
CComPtr<IInkObject *> spITextInk;

/* Obtain the text ink object */
```



然後，程式碼會建立包含文字筆墨物件內容之資料流程的指標。


```C++
// Create a Stream pointer to hold the saved object
CComPtr<IStream *> spStream = NULL; 
```



然後，程式碼會從文字筆墨物件取得 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 介面。


```C++
// Declare the IPersistStream to be used for retrieving the saved data from the text ink
CComPtr<IPersistStream *> spIPersistStream = NULL;
// Get the actual IPersistStream interface off of the TextInk
HRESULT hr = pITextInk->QueryInterface(IID_IPersistStream, (void **)&spIPersistStream);
ASSERT(SUCCEEDED(hr) && spIPersistStream);
```



然後，程式碼會使用 [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) 介面將文字筆墨物件的內容儲存至資料流程。


```C++
if( SUCCEEDED(hr) && pIPersistStream )
{
    // Create the stream 
    if( SUCCEEDED(hr=CreateStreamOnHGlobal(NULL, TRUE, &spStream)) && spStream )
    {
        // Save the TextInk through IPersistStream Interface to the IStream
        hr = spIPersistStream->Save(spStream, FALSE);
    }
}
```



然後，程式碼會建立 [**InkCollector**](inkcollector-class.md)物件、建立 **InkCollector** 的 [**InkDisp**](inkdisp-class.md)物件、將 **InkCollector** 附加至應用程式視窗，以及啟用 **InkCollector** 上的筆墨收集。


```C++
// Now create an InkCollector object along with InkDisp Object
if( SUCCEEDED(hr) && spStream)
{
    CComPtr<IInkCollector *> spIInkCollector;
    CComPtr<IInkDisp *> spIInkDisp = NULL;

    // Create the InkCollector object.
    hr = CoCreateInstance(CLSID_InkCollector, 
        NULL, CLSCTX_INPROC_SERVER, 
        IID_IInkCollector, 
        (void **) &spIInkCollector);
    if (FAILED(hr)) 
        return -1;

    // Get a pointer to the Ink object
    hr = spIInkCollector->get_Ink(&spIInkDisp);
    if (FAILED(hr)) 
        return -1;

    // Tell InkCollector the window to collect ink in
    hr = spIInkCollector->put_hWnd((long)hwnd);
    if (FAILED(hr)) 
        return -1;

    // Enable ink input in the window
    hr = spIInkCollector->put_Enabled(VARIANT_TRUE);
    if (FAILED(hr)) 
        return -1;
```



然後，程式碼會抓取資料流程的大小並建立安全陣列來保存資料流程的內容。


```C++
    // Now create a variant data type based on the IStream data
    const LARGE_INTEGER li0 = {0, 0};
    ULARGE_INTEGER uli = {0,0};

    // Find the size of the stream
    hr = spStream->Seek(li0, STREAM_SEEK_END, &uli);
    ASSERT(0 == uli.HighPart);
    DWORD dwSize = uli.LowPart;

    // Set uli to point to the beginning of the stream.
    hr=spStream->Seek(li0, STREAM_SEEK_SET, &uli);
    ASSERT(SUCCEEDED(hr));

    // Create a safe array to hold the stream contents
    if( SUCCEEDED(hr) )
    {
        VARIANT vtData;
        VariantInit(&vtData);
        vtData.vt = VT_ARRAY | VT_UI1;

        vtData.parray = ::SafeArrayCreateVector(VT_UI1, 0, dwSize);
        if (vtData.parray)
        {
```



最後，程式碼會存取安全陣列，並使用 [**InkDisp**](inkdisp-class.md) 物件的 [**load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) 方法從陣列載入筆墨。


```C++
            DWORD dwRead = 0;
            LPBYTE pbData = NULL; 

            if (SUCCEEDED(::SafeArrayAccessData(vtData.parray, (void**)&pbData)))
            {
                // Read the data from the stream to the varian data and load that into an InkDisp object
                if (TRUE == spStream->Read(pbData, uli.LowPart, &dwRead)
                    && SUCCEEDED(spIInkDisp->Load(vtData)))
                {
                    hr = S_OK;
                }
                ::SafeArrayUnaccessData(vtData.parray);
            }
            ::SafeArrayDestroy(vtData.parray);
        }
    }
}
```



 

 
