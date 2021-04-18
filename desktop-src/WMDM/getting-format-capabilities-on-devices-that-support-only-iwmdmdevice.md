---
title: 透過 IWMDMDevice 取得格式功能
description: 在僅支援 IWMDMDevice 的裝置上取得格式功能
ms.assetid: bff079a1-d192-4e53-9b1d-9ad3b5dcca51
keywords:
- Windows Media 裝置管理員，裝置功能
- 裝置管理員，裝置功能
- 程式設計指南，裝置功能
- 桌面應用程式，裝置功能
- 建立 Windows Media 裝置管理員應用程式，裝置功能
- 將檔案寫入裝置、裝置功能
- IWMDMDevice 方法
- Windows Media 裝置管理員，IWMDMDevice 方法
- 裝置管理員，IWMDMDevice 方法
- 程式設計手冊，IWMDMDevice 方法
- 桌面應用程式，IWMDMDevice 方法
- 建立 Windows Media 裝置管理員應用程式，IWMDMDevice 方法
- 將檔案寫入裝置，IWMDMDevice 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a923919611b40197b1deed30e781042e008ef41
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/27/2019
ms.locfileid: "104313845"
---
# <a name="getting-format-capabilities-through-iwmdmdevice"></a>透過 IWMDMDevice 取得格式功能

查詢裝置的播放功能的建議方法是 [**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)。 但是，如果裝置不支援此方法，則應用程式會改為呼叫 [**IWMDMDevice：： GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport) ，將支援的音訊格式陣列以 [**\_ WAVEFORMATEX**](-waveformatex.md)結構和 MIME 格式，從裝置取出為字串。

下列步驟顯示應用程式如何使用此方法來查詢裝置以取得支援的格式：

1.  呼叫 **GetFormatSupport** 可取出音訊和 mime 格式的陣列。
2.  對抓取的音訊格式執行迴圈，並檢查每個 [**\_ WAVEFORMATEX**](-waveformatex.md)結構，以嘗試尋找可接受的音訊格式
3.  如果需要) 尋找可接受的檔案類型，請在已取出的 MIME 格式字串之間執行迴圈 (。 SDK 不會定義 MIME 格式的常數;您應使用業界標準值 (可在 iana.org 網站) 找到。 裝置應該會列出它所支援的特定 MIME 類型。

下列 c + + 程式碼示範如何使用 **GetFormatSupport** 從裝置上取出格式功能。


```C++
// Function to print out device caps for a device 
// that supports only IWMDMDevice.
void CWMDMController::GetCaps(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get all capabilities for audio and mime support.
    _WAVEFORMATEX* pAudioFormats;
    LPWSTR* pMimeFormats;
    UINT numAudioFormats = 0;
    UINT numMimeFormats = 0;
    hr = pDevice->GetFormatSupport(
        &pAudioFormats,
        &numAudioFormats,
        &pMimeFormats,
        &numMimeFormats);
    if (FAILED(hr)) return;

    // Print out audio format data.
    if (numAudioFormats > 0)
    {
        // TODO: Display a banner for the supported audio-format listing.
    }
    else
    {
        // TODO: Display a message indicating that no audio formats are supported.
    }
    for (int i = 0; i < numAudioFormats; i++)
    {
       // TODO: For each valid audio format, display the max channel, 
       // max samples/second, avg. bytes/sec, block alignment, and 
       // max bits/sample values.
    }

    // Print out MIME formats.
    if (numMimeFormats > 0)
        // TODO: Display a banner to precede the MIME format listing.
    else
        // TODO: Display a banner indicating that no MIME formats are supported.
    for (i = 0; i < numMimeFormats; i++)
    {
        // TODO: Display the specified MIME format.
    }
    return;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**探索裝置格式功能**](discovering-device-format-capabilities.md)
</dt> <dt>

[**在支援 IWMDMDevice3 的裝置上取得格式功能**](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
</dt> </dl>

 

 




