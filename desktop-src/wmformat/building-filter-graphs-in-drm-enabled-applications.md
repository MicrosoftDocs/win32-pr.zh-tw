---
title: 在 DRM-Enabled 應用程式中建立篩選圖形
description: 在 DRM-Enabled 應用程式中建立篩選圖形
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows媒體格式 SDK，建立篩選圖形
- Windows媒體格式 SDK，DirectShow
- Windows媒體格式 SDK，啟用 DRM 的應用程式
- Advanced Systems Format (ASF) ，建立篩選圖形
- ASF (Advanced Systems Format) ，建立篩選圖形
- Advanced Systems Format (ASF) ，DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、已啟用 DRM 的應用程式
- ASF (Advanced Systems Format) 、已啟用 DRM 的應用程式
- DirectShow，建立篩選圖形
- DirectShow，啟用 DRM 的應用程式
- 數位版權管理 (DRM) ，DirectShow
- DRM (數位版權管理) ，DirectShow
- 數位版權管理 (DRM) ，建立篩選圖形
- DRM (數位版權管理) ，建立篩選圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e7f411a52c0ce7c42410c7a901787c7f6d9d7089921019639cb3f5e708dff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447948"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>在 DRM-Enabled 應用程式中建立篩選圖形

如果您的 DirectShow 應用程式支援播放受 DRM 保護的檔案，您通常不應該使用 **RenderFile** 來建立篩選圖形，因為在檔案開啟之前，沒有任何方法可指定您要求的 DRM 許可權。 依預設，WM ASF 讀取器只會要求播放許可權。 篩選不會加入至圖形，因此應用程式無法探索到檔案，直到檔案成功開啟為止。

若要使用 [WM ASF 讀取](wm-asf-reader-filter.md)器建立啟用 DRM 的播放圖形，您必須使用 **CoCreateInstance** 將篩選具現化、使用 **IGraphBuilder：： AddFilter** 將它新增至篩選圖形、加以設定，然後轉譯其輸出圖釘。 這項技術會在 PlayWndASF 範例中示範。 當您以這種方式建立圖形時，您已經擁有可用來呼叫 **QueryService** 以取得 **IWMDRMWriter** 的 **IBaseFilter** 指標。 不過，在 Windows 媒體格式 SDK 讀取器物件由 WM ASF 讀取器內部建立之前，無法使用此介面。 應用程式必須設定 DRM 許可權的第一個機會，是在其 WMT \_ 沒有許可權的範例 \_ \_ 事件處理常式中，如下列程式碼片段所示：


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**DRM 屬性清單**](drm-attribute-list.md)
</dt> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




