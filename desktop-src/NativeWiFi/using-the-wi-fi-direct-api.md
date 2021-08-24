---
description: 示範如何在桌面應用程式中使用 Wi-Fi Direct 函式。
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: 使用 Wi-Fi Direct 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9a00a5474632ed54a84a7dc8cc5c64774e7cfe7547e6994acee599df2461ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684728"
---
# <a name="using-the-wi-fi-direct-functions"></a>使用 Wi-Fi Direct 函數

本主題說明如何在桌面應用程式中使用 Wi-Fi Direct 函式。 從 Windows 8 和 Windows Server 2012 開始，Wi-Fi 直接函式新增至原生 Wifi API。

Wi-Fi 直接功能是以 Wi-Fi 聯盟的 Wi-Fi 對等技術規格 v1.1 開發為基礎， (查看 [Wi-fi 同盟發佈的規格](https://www.wi-fi.org/)) 。 Wi-Fi 點對點技術規格的目標是要提供解決方案來 Wi-Fi 裝置到裝置的連線能力，而不需要無線存取點， (無線 AP) 設定連線或使用現有的 Wi-Fi 臨機操作 (IBSS) 機制。

> [!Note]  
> 未來的 Windows 版本可能無法使用臨機操作模式。 從 Windows 8.1 和 Windows Server 2012 R2 開始，請改用 Wi-Fi 直接存取。

 

下列函數支援 Wi-Fi 直接功能。

-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) -表示應用程式想要取消尚未完成的暫止 [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) 函數。
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) -關閉 Wi-Fi Direct 服務的控制碼。
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) -在先前成功呼叫 [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) 函數之後關閉會話。
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) -開啟 Wi-Fi Direct 服務的控制碼，並協商要使用的 WI-FI 直接 API 版本。
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) -針對 Wi-Fi Direct 舊版裝置，取得並套用已儲存的設定檔。
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -啟動特定 Wi-Fi 直接裝置的隨選連線，先前已透過 Windows 配對體驗配對。
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) -針對指定的已安裝 Wi-Fi 直接裝置節點，更新 Wi-Fi 直接裝置位址的裝置可見度。
-   [**WFD \_OPEN \_ SESSION \_ COMPLETE \_ 回呼**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)-定義 **WFDStartOpenSession** 作業完成時， [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)函式所呼叫的回呼函數

若為傳統型應用程式，Wi-Fi 直接功能需要使用者將 wi-fi Direct 裝置與 Windows 配對體驗使用者介面配對。 一旦完成這項配對，就會儲存設定檔，以允許使用 Wi-Fi 直接的函式來啟動 Wi-Fi 直接會話，以建立 Wi-Fi 直接裝置之間的連接。

若要使用 Wi-Fi Direct，應用程式必須先呼叫 [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) 函式，以取得 Wi-Fi 直接服務的控制碼。 **WFDOpenHandle** 函式所傳回的 Wi-Fi DIRECT (WFD) 控制碼，會用於後續 Wi-Fi 對 Wi-Fi 直接服務的直接函式呼叫。

[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)函式會啟動非同步作業，以啟動特定 Wi-Fi 直接裝置的隨選連接。 目標 Wi-Fi 裝置之前必須經過 Windows 配對體驗的配對。 當非同步作業完成時，會呼叫 *pfnCallback* 參數中指定的回呼函數。

使用 Wi-Fi Direct 服務完成應用程式之後，應用程式應該呼叫 [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) 函式，以通知 Wi-Fi 直接服務，應用程式是使用服務完成的。 這可讓 Wi-Fi 的直接服務釋放應用程式所使用的資源。

如需 Wi-Fi 直接在 Windows Store 應用程式中使用的詳細資訊，請參閱 Windows 中的 [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)和相關類別 [**。網路功能。鄰近**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)命名空間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**其他資源**
</dt> <dt>

[關於原生 Wifi](about-native-wifi.md)
</dt> <dt>

[關於原生 Wifi API](about-the-native-wifi-api.md)
</dt> <dt>

[關於 Wi-Fi 直接功能](about-the-wi-fi-direct-api.md)
</dt> <dt>

**參考**
</dt> <dt>

[**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ 回呼**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
