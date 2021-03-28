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
# <a name="building-thumbnail-handlers"></a>建立縮圖處理常式

從 Windows Vista 起，更大的使用是由檔案專屬的縮圖影像所組成，而不是在舊版的 Windows 中。 它們用於所有視圖、對話方塊以及提供它們的任何檔案類型。 縮圖顯示也已變更。 您可以使用連續的使用者可選取大小，而不是個別的大小，例如圖示和縮圖。

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)介面可提供比舊版 [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage)或 [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2)更簡單的縮圖。 不過請注意，使用 **IExtractImage** 或 **IExtractImage2** 的現有程式碼仍然有效且受支援。

## <a name="the-recipethumbnailprovider-sample"></a>RecipeThumbnailProvider 範例

本節中的 [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) 範例解析包含在 WINDOWS 軟體開發套件 (SDK) 中。 其預設安裝位置為 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 6.0 \\ 範例 \\ WinUI \\ Shell \\ AppShellIntegration \\ RecipeThumbnailProvider。 不過，大部分的程式碼也都包含在此處。

[RecipeThumbnailProvider](samples-recipethumbnailprovider.md)範例會示範如何針對以配方副檔名註冊的新檔案類型來執行縮圖處理常式。 此範例說明如何使用不同的縮圖處理常式 Api，將縮圖解壓縮元件物件模型註冊 (COM) 伺服器以進行自訂檔案類型。 本主題將逐步引導您完成範例程式碼，並醒目提示程式碼選擇和指導方針。

縮圖處理常式必須一律搭配下列其中一個介面來執行 [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) ：

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

在某些情況下，不可能使用資料流程進行初始化。 在縮圖處理常式未執行 [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)的情況下，它必須選擇不在隔離的進程中執行，而系統索引子預設會在資料流程發生變更時放置它。 若要退出進程隔離功能，請設定下列登錄值。

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

如果您執行 [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) 並執行以資料流程為基礎的初始化，則處理常式會更安全且可靠。 一般而言，停用進程隔離只適用于舊版處理常式;避免針對任何新的程式碼停用此功能。 **IInitializeWithStream** 應該是您第一次選擇的初始化介面。

因為範例中的影像檔未內嵌于配方檔案中，而不是其檔案資料流程的一部分，所以此範例中會使用 [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) 。 [**IInitializeWithItem：： Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize)方法的執行只會將其參數傳遞至私用類別變數。

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) 只有一個方法（[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)），它會使用最大的影像大小（以圖元為單位）來呼叫。 雖然參數命名為 *cx*，但它的值會當做影像 x 和 y 維度的大小上限。 如果取出的縮圖不是正方形，則較長的軸會受到 *cx* 的限制，並保留原始影像的外觀比例。

當它傳回時， [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) 會提供抓取影像的控制碼。 它也會提供一個值，指出影像的色彩格式，以及它是否有有效的 Alpha 資訊。

範例中的 GetThumbnail 實開頭是對私用 **\_ GetBase64EncodedImageString** 方法的呼叫。


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



配方檔案類型只是註冊為唯一副檔名的 XML 檔。 它包含名為 **Picture** 的元素，可提供影像的相對路徑和檔案名，以做為這個特殊配方檔案的縮圖。 **Picture** 元素是由指定基底64編碼影像的 **來源** 屬性，以及選擇性的 **大小** 屬性所組成。

**大小** 有兩個值（小型和大型）。 這可讓您提供多個具有個別影像的 **圖片** 節點。 然後，會根據 [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)呼叫中所提供的最大大小值 (*cx*) 來取出影像。 因為 Windows 絕不會將影像的大小調整為超過其大小上限，所以可以為不同的解析度提供不同的影像。 不過，為了簡單起見，此範例會省略 **Size** 屬性，並在所有情況下只提供一個影像。

**\_ GetBase64EncodedImageString** 方法（其執行方式如下所示）會使用 XML 檔物件模型 (DOM) Api 來取出 **圖片** 節點。 從該節點，它會從 **來源** 屬性資料中解壓縮映射。


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



[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)接著會將抓取的字串傳遞至 **\_ GetStreamFromString**。


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



**\_ GetStreamFromString** 方法（其執行方式如下所示）會將編碼的影像轉換為數據流。


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



然後， **GetThumbnail** 會使用 WINDOWS 影像處理元件 (WIC) api 從資料流程中解壓縮點陣圖，並取得該點陣圖的控制碼。 已設定 Alpha 資訊，WIC 已正確結束，且方法會成功終止。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[縮圖處理常式](thumbnail-providers.md)
</dt> <dt>

[縮圖處理常式指導方針](thumbnail-provider-guidelines.md)
</dt> <dt>

[**IID \_ PPV 引數 \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
