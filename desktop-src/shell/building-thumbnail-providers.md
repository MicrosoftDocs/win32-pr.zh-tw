---
description: 從 Windows Vista 起，更大的使用是由檔案專屬的縮圖影像所組成，而不是在舊版的 Windows 中。
title: 建立縮圖處理常式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 218264a9-ed26-4049-a721-232943f6ec53
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05e13f24a2f4d70a58bab904150b1e488f74854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972068"
---
# <a name="building-thumbnail-handlers"></a><span data-ttu-id="0e0ac-103">建立縮圖處理常式</span><span class="sxs-lookup"><span data-stu-id="0e0ac-103">Building Thumbnail Handlers</span></span>

<span data-ttu-id="0e0ac-104">從 Windows Vista 起，更大的使用是由檔案專屬的縮圖影像所組成，而不是在舊版的 Windows 中。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-104">As of Windows Vista, greater use is made of file-specific thumbnail images than in earlier versions of Windows.</span></span> <span data-ttu-id="0e0ac-105">它們用於所有視圖、對話方塊以及提供它們的任何檔案類型。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-105">They are used in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="0e0ac-106">縮圖顯示也已變更。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-106">Thumbnail display was also changed.</span></span> <span data-ttu-id="0e0ac-107">您可以使用連續的使用者可選取大小，而不是個別的大小，例如圖示和縮圖。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-107">A continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails.</span></span>

<span data-ttu-id="0e0ac-108">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)介面可提供比舊版 [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage)或 [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2)更簡單的縮圖。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-108">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface makes providing a thumbnail more straightforward than the older [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) or [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span></span> <span data-ttu-id="0e0ac-109">不過請注意，使用 **IExtractImage** 或 **IExtractImage2** 的現有程式碼仍然有效且受支援。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-109">Note, however, that existing code that uses **IExtractImage** or **IExtractImage2** is still valid and supported.</span></span>

## <a name="the-recipethumbnailprovider-sample"></a><span data-ttu-id="0e0ac-110">RecipeThumbnailProvider 範例</span><span class="sxs-lookup"><span data-stu-id="0e0ac-110">The RecipeThumbnailProvider Sample</span></span>

<span data-ttu-id="0e0ac-111">本節中的 [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) 範例解析包含在 WINDOWS 軟體開發套件 (SDK) 中。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-111">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample dissected in this section is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0e0ac-112">其預設安裝位置為 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 6.0 \\ 範例 \\ WinUI \\ Shell \\ AppShellIntegration \\ RecipeThumbnailProvider。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-112">Its default install location is C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppShellIntegration\\RecipeThumbnailProvider.</span></span> <span data-ttu-id="0e0ac-113">不過，大部分的程式碼也都包含在此處。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-113">However, the bulk of the code is included here as well.</span></span>

<span data-ttu-id="0e0ac-114">[RecipeThumbnailProvider](samples-recipethumbnailprovider.md)範例會示範如何針對以配方副檔名註冊的新檔案類型來執行縮圖處理常式。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-114">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample demonstrates the implementation of a thumbnail handler for a new file type registered with a .recipe extension.</span></span> <span data-ttu-id="0e0ac-115">此範例說明如何使用不同的縮圖處理常式 Api，將縮圖解壓縮元件物件模型註冊 (COM) 伺服器以進行自訂檔案類型。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-115">The sample illustrates the use of the different thumbnail handler APIs to register thumbnail extraction Component Object Model (COM) servers for custom file types.</span></span> <span data-ttu-id="0e0ac-116">本主題將逐步引導您完成範例程式碼，並醒目提示程式碼選擇和指導方針。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-116">This topic walks you through the sample code, highlighting coding choices and guidelines.</span></span>

<span data-ttu-id="0e0ac-117">縮圖處理常式必須一律搭配下列其中一個介面來執行 [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) ：</span><span class="sxs-lookup"><span data-stu-id="0e0ac-117">A thumbnail handler must always implement [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) in concert with one of these interfaces:</span></span>

-   [<span data-ttu-id="0e0ac-118">**IInitializeWithStream**</span><span class="sxs-lookup"><span data-stu-id="0e0ac-118">**IInitializeWithStream**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="0e0ac-119">**IInitializeWithItem**</span><span class="sxs-lookup"><span data-stu-id="0e0ac-119">**IInitializeWithItem**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="0e0ac-120">**IInitializeWithFile**</span><span class="sxs-lookup"><span data-stu-id="0e0ac-120">**IInitializeWithFile**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="0e0ac-121">在某些情況下，不可能使用資料流程進行初始化。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-121">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="0e0ac-122">在縮圖處理常式未執行 [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)的情況下，它必須選擇不在隔離的進程中執行，而系統索引子預設會在資料流程發生變更時放置它。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-122">In scenarios where your thumbnail handler does not implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process where the system indexer places it by default when there is a change to the stream.</span></span> <span data-ttu-id="0e0ac-123">若要退出進程隔離功能，請設定下列登錄值。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-123">To opt out of the process isolation feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

<span data-ttu-id="0e0ac-124">如果您執行 [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) 並執行以資料流程為基礎的初始化，則處理常式會更安全且可靠。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-124">If you implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization, your handler is more secure and reliable.</span></span> <span data-ttu-id="0e0ac-125">一般而言，停用進程隔離只適用于舊版處理常式;避免針對任何新的程式碼停用此功能。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-125">Typically, disabling process isolation is only intended for legacy handlers; avoid disabling this feature for any new code.</span></span> <span data-ttu-id="0e0ac-126">**IInitializeWithStream** 應該是您第一次選擇的初始化介面。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-126">**IInitializeWithStream** should be your first choice of initialization interface whenever possible.</span></span>

<span data-ttu-id="0e0ac-127">因為範例中的影像檔未內嵌于配方檔案中，而不是其檔案資料流程的一部分，所以此範例中會使用 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) 。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-127">Because the image file in the sample is not embedded in the .recipe file and is not a part of its file stream, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) is used in the sample.</span></span> <span data-ttu-id="0e0ac-128">[**IInitializeWithItem：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize)方法的執行只會將其參數傳遞至私用類別變數。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-128">The implementation of the [**IInitializeWithItem::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) method simply passes its parameters to private class variables.</span></span>

<span data-ttu-id="0e0ac-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) 只有一個方法（[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)），它會使用最大的影像大小（以圖元為單位）來呼叫。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) has only one method—[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)—that is called with the largest desired size of the image, in pixels.</span></span> <span data-ttu-id="0e0ac-130">雖然參數命名為 *cx*，但它的值會當做影像 x 和 y 維度的大小上限。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-130">Although the parameter is named *cx*, its value is used as the maximum size of both the x and y dimensions of the image.</span></span> <span data-ttu-id="0e0ac-131">如果取出的縮圖不是正方形，則較長的軸會受到 *cx* 的限制，並保留原始影像的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-131">If the retrieved thumbnail is not square, then the longer axis is limited by *cx* and the aspect ratio of the original image is preserved.</span></span>

<span data-ttu-id="0e0ac-132">當它傳回時， [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) 會提供抓取影像的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-132">When it returns, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) provides a handle to the retrieved image.</span></span> <span data-ttu-id="0e0ac-133">它也會提供一個值，指出影像的色彩格式，以及它是否有有效的 Alpha 資訊。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-133">It also provides a value that indicates the color format of the image and whether it has valid alpha information.</span></span>

<span data-ttu-id="0e0ac-134">範例中的 GetThumbnail 實開頭是對私用 **\_ GetBase64EncodedImageString** 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-134">The GetThumbnail implementation in the sample begins with a call to the private **\_GetBase64EncodedImageString** method.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



<span data-ttu-id="0e0ac-135">配方檔案類型只是註冊為唯一副檔名的 XML 檔。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-135">The .recipe file type is simply an XML file registered as a unique file name extension.</span></span> <span data-ttu-id="0e0ac-136">它包含名為 **Picture** 的元素，可提供影像的相對路徑和檔案名，以做為這個特殊配方檔案的縮圖。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-136">It includes an element called **Picture** that provides the relative path and file name of the image to use as the thumbnail for this particular .recipe file.</span></span> <span data-ttu-id="0e0ac-137">**Picture** 元素是由指定基底64編碼影像的 **來源** 屬性，以及選擇性的 **大小** 屬性所組成。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-137">The **Picture** element consists of the **Source** attribute that specifies a base 64 encoded image, and an optional **Size** attribute.</span></span>

<span data-ttu-id="0e0ac-138">**大小** 有兩個值（小型和大型）。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-138">**Size** has two values, Small and Large.</span></span> <span data-ttu-id="0e0ac-139">這可讓您提供多個具有個別影像的 **圖片** 節點。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-139">This allows you to provide multiple **Picture** nodes with separate images.</span></span> <span data-ttu-id="0e0ac-140">然後，會根據 [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)呼叫中所提供的最大大小值 (*cx*) 來取出影像。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-140">The image retrieved then depends on the maximum size value (*cx*) provided in the call to [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span></span> <span data-ttu-id="0e0ac-141">因為 Windows 絕不會將影像的大小調整為超過其大小上限，所以可以為不同的解析度提供不同的影像。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-141">Because Windows never sizes the image any larger than its maximum size, different images can be provided for different resolutions.</span></span> <span data-ttu-id="0e0ac-142">不過，為了簡單起見，此範例會省略 **Size** 屬性，並在所有情況下只提供一個影像。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-142">However, for simplicity, the sample omits the **Size** attribute and provides only one image for all situations.</span></span>

<span data-ttu-id="0e0ac-143">**\_ GetBase64EncodedImageString** 方法（其執行方式如下所示）會使用 XML 檔物件模型 (DOM) Api 來取出 **圖片** 節點。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-143">The **\_GetBase64EncodedImageString** method, whose implementation is shown here, uses XML Document Object Model (DOM) APIs to retrieve the **Picture** node.</span></span> <span data-ttu-id="0e0ac-144">從該節點，它會從 **來源** 屬性資料中解壓縮映射。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-144">From that node it extracts the image from the **Source** attribute data.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetBase64EncodedImageString(UINT /* cx */, 
                                                           PWSTR *ppszResult)
{
    *ppszResult = NULL;

    IXMLDOMDocument *pXMLDoc;
    HRESULT hr = _LoadXMLDocument(&pXMLDoc);
    if (SUCCEEDED(hr))
    {
        BSTR bstrQuery = SysAllocString(L"Recipe/Attachments/Picture");
        hr = bstrQuery ? S_OK : E_OUTOFMEMORY;
        if (SUCCEEDED(hr))
        {
            IXMLDOMNode *pXMLNode;
            hr = pXMLDoc->selectSingleNode(bstrQuery, &pXMLNode);
            if (SUCCEEDED(hr))
            {
                IXMLDOMElement *pXMLElement;
                hr = pXMLNode->QueryInterface(&pXMLElement);
                if (SUCCEEDED(hr))
                {
                    BSTR bstrAttribute = SysAllocString(L"Source");
                    hr = bstrAttribute ? S_OK : E_OUTOFMEMORY;
                    if (SUCCEEDED(hr))
                    {
                        VARIANT varValue;
                        hr = pXMLElement->getAttribute(bstrAttribute, &varValue);
                        if (SUCCEEDED(hr))
                        {
                            if ((varValue.vt == VT_BSTR) && varValue.bstrVal && varValue.bstrVal[0])
                            {
                                hr = SHStrDupW(varValue.bstrVal, ppszResult);
                            }
                            else
                            {
                                hr = E_FAIL;
                            }
                            VariantClear(&varValue);
                        }
                        SysFreeString(bstrAttribute);
                    }
                    pXMLElement->Release();
                }
                pXMLNode->Release();
            }
            SysFreeString(bstrQuery);
        }
        pXMLDoc->Release();
    }
    return hr;
}
```



<span data-ttu-id="0e0ac-145">[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)接著會將抓取的字串傳遞至 **\_ GetStreamFromString**。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-145">[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) then passes the retrieved string to **\_GetStreamFromString**.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
```



<span data-ttu-id="0e0ac-146">**\_ GetStreamFromString** 方法（其執行方式如下所示）會將編碼的影像轉換為數據流。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-146">The **\_GetStreamFromString** method, whose implementation is shown here, which converts the encoded image to a stream.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetStreamFromString(PCWSTR pszImageName, 
                                                   IStream **ppImageStream)
{
    HRESULT hr = E_FAIL;

    DWORD dwDecodedImageSize = 0;
    DWORD dwSkipChars        = 0;
    DWORD dwActualFormat     = 0;

    // Base64-decode the string
    BOOL fSuccess = CryptStringToBinaryW(pszImageName, 
                                         NULL, 
                                         CRYPT_STRING_BASE64,
                                         NULL, 
                                         &dwDecodedImageSize, 
                                         &dwSkipChars, 
                                         &dwActualFormat);
    if (fSuccess)
    {
        BYTE *pbDecodedImage = (BYTE*)LocalAlloc(LPTR, dwDecodedImageSize);
        if (pbDecodedImage)
        {
            fSuccess = CryptStringToBinaryW(pszImageName, 
                                            lstrlenW(pszImageName), 
                                            CRYPT_STRING_BASE64,
                                            pbDecodedImage, 
                                            &dwDecodedImageSize, 
                                            &dwSkipChars, 
                                            &dwActualFormat);
            if (fSuccess)
            {
                *ppImageStream = SHCreateMemStream(pbDecodedImage, 
                                                   dwDecodedImageSize);
                if (*ppImageStream != NULL)
                {
                    hr = S_OK;
                }
            }
            LocalFree(pbDecodedImage);
        }
    }
    return hr;
}
```



<span data-ttu-id="0e0ac-147">然後， **GetThumbnail** 會使用 WINDOWS 影像處理元件 (WIC) api 從資料流程中解壓縮點陣圖，並取得該點陣圖的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-147">**GetThumbnail** then uses Windows Imaging Component (WIC) APIs to extract a bitmap from the stream and get a handle to that bitmap.</span></span> <span data-ttu-id="0e0ac-148">已設定 Alpha 資訊，WIC 已正確結束，且方法會成功終止。</span><span class="sxs-lookup"><span data-stu-id="0e0ac-148">The alpha information is set, WIC is properly exited, and the method terminates successfully.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
        if (SUCCEEDED(hr))
        {
            hr = WICCreate32BitsPerPixelHBITMAP(pImageStream, 
                                                cx, 
                                                phbmp, 
                                                pdwAlpha);;

            pImageStream->Release();
        }
        CoTaskMemFree(pszBase64EncodedImageString);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="0e0ac-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e0ac-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e0ac-150">縮圖處理常式</span><span class="sxs-lookup"><span data-stu-id="0e0ac-150">Thumbnail Handlers</span></span>](thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="0e0ac-151">縮圖處理常式指導方針</span><span class="sxs-lookup"><span data-stu-id="0e0ac-151">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> <dt>

[<span data-ttu-id="0e0ac-152">**IID \_ PPV 引數 \_**</span><span class="sxs-lookup"><span data-stu-id="0e0ac-152">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
