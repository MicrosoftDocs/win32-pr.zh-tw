---
title: 判斷播放清單同步處理狀態
description: 判斷播放清單同步處理狀態
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Windows Media Player，同步播放清單
- Windows Media Player 物件模型，同步播放清單
- 物件模型，同步處理播放清單
- Windows Media Player行動裝置，同步播放清單
- Windows Media Player ActiveX 控制項、同步播放清單
- Windows Media Player行動 ActiveX 控制項、同步播放清單
- ActiveX 控制項，同步播放清單
- 播放清單，同步處理
- 中繼檔播放清單，同步處理
- Windows媒體中繼檔播放清單，同步處理
- 可攜式裝置，判斷同步播放清單的狀態
- 同步播放清單，同步處理狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14af59f66d1b21eac00208ecc805f756761256e47a35042694bcd65e6f96558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579457"
---
# <a name="determining-playlist-synchronization-state"></a>判斷播放清單同步處理狀態

Windows Media Player 10 或更新版本會使用 **SyncState** 屬性來包含特定數位媒體檔案是否已複製到可攜式裝置的相關資訊，以及是否因為裝置沒有足夠的記憶體而導致複製失敗的情況。

下列程式碼範例會建立函式，此函式會從數位媒體檔案抓取此資訊。 函數會採用下列參數：

-   *pMedia*。 **IWMPMedia** 介面的指標，代表要檢查的數位媒體檔案。
-   *lPsIndex*。 目前裝置的合作關係索引。
-   *pulOnDevice*。 **長** 變數的指標，此變數會接收指出數位媒體檔案是否已複製到裝置的值。
-   *pulDidNotFit*。 **長** 變數的指標，此變數會接收值，指出複製作業是否因為裝置沒有足夠的記憶體而失敗。

**SyncState** 屬性中包含的資訊是以位方式編碼。 您可以在 [列舉媒體專案](enumerating-the-media-items.md)的範例程式碼中看到此函式的使用方式。


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMPMedia 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPMedia3::getItemInfoByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[**管理同步播放清單**](managing-synchronization-playlists.md)
</dt> <dt>

[**SyncState 屬性**](syncstate-attribute.md)
</dt> </dl>

 

 




