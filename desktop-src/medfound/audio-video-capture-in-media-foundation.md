---
description: Microsoft 媒體基礎支援音訊和影片捕捉。
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: 媒體基礎中的音訊/影片捕獲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cf225c8e11823779a401288135017d119fe67e4cd32fa39b54f3cd39b7bb45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880903"
---
# <a name="audiovideo-capture-in-media-foundation"></a>媒體基礎中的音訊/影片捕獲

Microsoft 媒體基礎支援音訊和影片捕捉。 您可以透過 UVC 類別驅動程式支援影片捕獲裝置，而且必須與 UVC 1.1 相容。 音訊捕獲裝置可透過 Windows 音訊會話 API (WASAPI) 來支援。

捕獲裝置會以媒體來源物件媒體基礎表示，它會公開 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面。 在大部分情況下，應用程式不會直接使用此介面，但會使用較高層級的 API （例如 [來源讀取器](source-reader.md) ）來控制捕獲裝置。

## <a name="enumerate-capture-devices"></a>列舉捕獲裝置

若要列舉系統上的捕獲裝置，請執行下列步驟：

1.  呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 函數來建立屬性存放區。
2.  將 [ [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型](mf-devsource-attribute-source-type.md) ] 屬性設定為下列其中一個值：

    | 值                                                    | 描述                      |
    |----------------------------------------------------------|----------------------------------|
    | **MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ GUID** | 列舉音訊捕獲裝置。 |
    | **MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ GUID** | 列舉影片捕獲裝置。 |

    

     

3.  呼叫 [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) 函數。 此函數會配置 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標的陣列。 每個指標都代表系統上一個裝置的啟用物件。
4.  呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 方法，從其中一個啟用物件建立媒體來源的實例。

下列範例會在列舉清單中建立第一個影片捕獲裝置的媒體來源：


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



您可以查詢啟用物件中的各種屬性，包括下列各項：

-   [ [MF \_ DEVSOURCE 屬性] 的 [ \_ \_ 易記 \_ 名稱](mf-devsource-attribute-friendly-name.md) ] 屬性包含裝置的顯示名稱。 顯示名稱適用于向使用者顯示，但可能不是唯一的。
-   針對影片裝置， [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) 屬性包含裝置的符號連結。 符號連結可唯一識別系統上的裝置，但不是可讀取的字串。
-   針對音訊裝置， [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ 端點 \_ 識別碼](mf-devsource-attribute-source-type-audcap-endpoint-id.md) 屬性包含裝置的音訊端點識別碼。 音訊端點識別碼類似于符號連結。 它可唯一識別系統上的裝置，但不是可讀取的字串。

下列範例會採用 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標的陣列，並將每個裝置的顯示名稱列印到 [偵錯工具] 視窗：


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



如果您已經知道影片裝置的符號連結，還有另一種方式可建立裝置的媒體來源：

1.  呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 以建立屬性存放區。
2.  將 [ [mf \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型](mf-devsource-attribute-source-type.md) ] 屬性設定為 [ **mf \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ GUID**]。
3.  將 [ [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ VIDCAP \_ 符號 \_ 連結](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) ] 屬性設定為符號連結。
4.  請呼叫 [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) 或 [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) 函數。 前者會傳回 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 指標。 後者會傳回啟用物件的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 指標。 您可以使用啟用物件來建立來源。  (啟用物件可以封送處理至另一個進程，因此如果您想要在另一個進程中建立來源，則會很有用。 如需詳細資訊，請參閱 [啟用物件](activation-objects.md)。 ) 

下列範例會採用影片裝置的符號連結，並建立媒體來源。


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



從音訊端點識別碼建立音訊裝置有相當的方式：

1.  呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 以建立屬性存放區。
2.  將 [ [mf \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型](mf-devsource-attribute-source-type.md) ] 屬性設定為 [ **mf \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ GUID**]。
3.  將 [ [MF \_ DEVSOURCE \_ 屬性 \_ 來源 \_ 類型 \_ AUDCAP \_ 端點 \_ 識別碼](mf-devsource-attribute-source-type-audcap-endpoint-id.md) ] 屬性設定為端點識別碼。
4.  請呼叫 [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) 或 [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) 函數。

下列範例會使用音訊端點識別碼並建立媒體來源。


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a>使用 capture 裝置

建立 capture 裝置的媒體來源之後，請使用 [來源讀取器](source-reader.md) 從裝置取得資料。 來源讀取器會提供包含捕獲音訊資料或影片畫面的媒體範例。 下一步取決於您的應用程式案例：

-   影片預覽：使用 Microsoft Direct3D 或 Direct2D 來顯示影片。
-   檔案捕獲：使用 [接收寫入器](sink-writer.md) 對檔案進行編碼。
-   音訊預覽：使用 [WASAPI](/windows/desktop/CoreAudio/wasapi)。

如果您想要將音訊捕獲與影片捕獲結合，請使用 *匯總媒體來源*。 匯總媒體來源包含媒體來源的集合，並將其所有串流合併為單一媒體來源物件。 若要建立匯總媒體來源的實例，請呼叫 [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) 函數。

## <a name="shut-down-the-capture-device"></a>關閉捕獲裝置

當不再需要 capture 裝置時，您必須在透過呼叫 [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)或 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)取得的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)物件上呼叫 [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) ，以關閉裝置。 無法呼叫 **關機** 可能會導致記憶體連結，因為系統可能會保留 **IMFMediaSource** 資源的參考，直到呼叫 **關機** 為止。


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



如果您將包含符號連結的字串配置到 capture 裝置，您也應該釋放此物件。


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊擷取](audio-video-capture.md)
</dt> </dl>

 

 
