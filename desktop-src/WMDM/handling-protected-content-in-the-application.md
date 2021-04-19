---
title: 處理應用程式中受保護的內容
description: 處理應用程式中受保護的內容
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Media 裝置管理員，憑證
- 裝置管理員，憑證
- 程式設計指南，憑證
- 桌面應用程式，憑證
- 建立 Windows Media 裝置管理員應用程式，憑證
- certificates
- Windows Media 裝置管理員、受 DRM 保護的內容
- 裝置管理員，受 DRM 保護的內容
- 程式設計指南，受 DRM 保護的內容
- 桌面應用程式，受 DRM 保護的內容
- 建立 Windows Media 裝置管理員應用程式，受 DRM 保護的內容
- 受 DRM 保護的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc354e78b9c937db339f5bf6a167f504986fbb64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967912"
---
# <a name="handling-protected-content-in-the-application"></a>處理應用程式中受保護的內容

\[Windows Media DRM 功能已被取代，不應該使用。 請改用 [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) 。\]

應用程式必須要有傳送憑證，才能處理受 DRM 保護的內容。 若要瞭解取得此憑證的位置，請參閱 [適用于開發的工具](tools-for-development.md)。 若要處理未受保護的內容，您可以使用虛擬憑證（如 [驗證應用程式](authenticating-the-application.md)中所述）。

使用裝置之前，您的應用程式應判斷裝置是否支援可攜式裝置的 Windows Media DRM 10，如果是，則表示 DRM 元件是最新的。  (Current 表示安全時鐘正確，且裝置已正確地個人化。 ) 如果裝置不支援此版本的 DRM，或無法更新，您仍然可以將檔案傳送至裝置，但根據授權版本，可能無法播放檔案。

> [!Note]  
> 目前不支援裝置的個人化。

 

如果您的應用程式將會連結至 Windows Media Format SDK 方法，則必須連結至 Windows Media Format library WMStubDRM .lib。 如需有關在受 DRM 保護的內容上呼叫 Windows 媒體格式方法的詳細資訊，請參閱 Windows Media Format SDK 檔中的「啟用 DRM 支援」。 請注意，連結至 Mssachlp .lib 和 WMStubDRM 時有問題。 這涵蓋于 [MSDN 上的知識庫文章 890079](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079)。

下列 c + + 程式碼範例會判斷裝置是否為 Windows Media DRM 10 裝置，如果是，則它的時鐘是最新的。

`HRESULT IsDRMClockUpToDate()`


```C++
{
    HRESULT hr = S_OK;

    // Create the DRM handler class.
    CComPtr<IWMDRMDeviceApp> pDRM;
    hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

    // Find out first if the device is a WMDRM 10 device, and if so,
    // whether it requires clock updates.
    DWORD status = 0;
    hr = pDRM->QueryDeviceStatus(pDevice, &status);

    if (FAILED(hr)
       || (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. 
       || (status & WMDRM_DEVICE_REVOKED))   // Device is revoked.
    {
        return E_FAIL;
    }
    else if (status & WMDRM_DEVICE_NEEDCLOCK || 
        status & WMDRM_DEVICE_REFRESHCLOCK)
    {
        // Attempt update. See following example.
        hr = UpdateDRM(status);
    }
    return hr;
}
```



如果裝置支援適用于可攜式裝置的 Windows Media DRM 10，且需要更新 (也就是，如果前一個範例中的 *狀態* 值不只是 WMDM \_ device \_ ISWMDRM) ，應用程式應該呼叫 [**IWMDRMDeviceApp：： AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) ，並傳入 *status* 值以執行必要的更新。 桌上型電腦必須連線到網際網路。

下列 c + + 範例函式會嘗試更新 DRM 裝置。


```C++
HRESULT UpdateDRM(DWORD status)
{
    HRESULT hr = S_OK;
    hr = pDRM->AcquireDeviceData(pDevice, this, status, &result);
    if (hr != S_OK || result != 0)
    {
            return E_FAIL;
    }
    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows Media 裝置管理員應用程式**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**處理受保護的內容**](handling-protected-content.md)
</dt> </dl>

 

 