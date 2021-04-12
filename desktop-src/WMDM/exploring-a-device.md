---
title: 探索裝置
description: 探索裝置
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Media 裝置管理員，探索裝置
- 裝置管理員，探索裝置
- 程式設計指南，探索裝置
- 桌面應用程式，探索裝置
- 建立 Windows Media 裝置管理員應用程式，探索裝置
- 探索裝置
- 存儲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372229"
---
# <a name="exploring-a-device"></a>探索裝置

探索裝置類似于探索磁片磁碟機。 裝置上的所有物件都稱為「 *儲存體*」。 儲存體可以是檔案、資料夾或抽象物件 (例如裝置上的播放清單) 。 您必須檢查儲存體的屬性和中繼資料 (是否支援) 瞭解它的儲存體類型。 在裝置上以階層方式組織存放裝置;每個儲存體都只有一個父系，而所有存放裝置最終都會從單一根裝置儲存體（通常名為 ""）開始 \\ 。

下列步驟說明如何探索裝置：

1.  如 [列舉裝置](enumerating-devices.md)所述，取得裝置的 [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)介面。
2.  呼叫 [**IWMDMDevice：： EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) 來取出 [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) 介面。 這個介面是用來取得傳回此介面之儲存體的所有子物件。 從裝置取得這個介面時，在這裡，它只會保留一個儲存體：根裝置存放裝置。
3.  使用計數1呼叫 [**IWMDMEnumStorage：： Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) ，以抓取根裝置存放裝置的 [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) 介面。  (您無法向裝置要求一個以上的子系。 ) 
4.  以遞迴方式呼叫 [**IWMDMStorage：： EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) ，然後 **IWMDMEnumStorage：： Next** 來檢查裝置上的所有存放裝置，以取得存放裝置的子系。 若要查看儲存體是否有子系可避免呼叫 **EnumStorage** 和 **下一個**，您可以呼叫 [**IWMDMStorage：： GETATTRIBUTES**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) 來檢查旗標 WMDM \_ 儲存體 attr 是否有檔案 \_ \_ \_ 或 WMDM \_ 儲存體 \_ attr \_ 有 \_ 資料夾。 如需如何取得儲存體屬性的詳細資訊，請參閱 [取得和設定中繼資料和屬性](getting-and-setting-metadata-and-attributes.md) ，以及 [取得和設定應用程式中的中繼資料和屬性](getting-and-setting-metadata-and-attributes-in-the-application.md)。

Windows Media 裝置管理員不會公開一組標準的資料夾來保存特定類型的媒體 (例如播放清單) 的「我的播放清單」資料夾。 每個裝置都有唯一的檔案系統，而您必須決定適當的位置來尋找或傳送特定的檔案。

> [!Note]  
> Windows 檔案總管可以顯示未實際存在於裝置上的虛擬資料夾。 範例虛擬資料夾是顯示 MTP 裝置的「媒體」和「資料」資料夾。 Windows 會建立這些資料夾，讓使用者更容易下載;它們實際上並不存在於裝置上。 您的應用程式不應該相依于尋找這些類型的一般資料夾。 相反地，Windows 檔案總管可能不會顯示裝置上存在的一些資料夾或物件 (例如，播放清單) 。

 

下列 c + + 範例程式碼示範裝置的遞迴探索。 它使用兩個函數：

-   ExploreDevice，此為啟動函式，可接收裝置指標並取得該裝置之根列舉值的指標。
-   RecursiveExploreStorage，呼叫以遞迴方式探索裝置。


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows Media 裝置管理員應用程式**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




