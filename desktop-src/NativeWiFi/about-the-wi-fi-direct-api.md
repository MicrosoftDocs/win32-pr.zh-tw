---
description: 原生 Wifi API 包含一組支援對傳統型應用程式使用 Wi-Fi Direct 的函式。
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: 關於 Wi-Fi 直接功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2816938b3e2d9156f2a97b67990386af2d5d780aa0226316cccc5edd0f2a4b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620206"
---
# <a name="about-the-wi-fi-direct-feature"></a>關於 Wi-Fi 直接功能

原生 Wifi API 包含一組支援對傳統型應用程式使用 Wi-Fi Direct 的函式。 從 Windows 8 和 Windows Server 2012 開始，Wi-Fi 直接函式新增至原生 Wifi API。

Wi-Fi 直接功能是以 Wi-Fi 聯盟的 Wi-Fi 對等技術規格 v1.1 開發為基礎， (查看 [Wi-fi 同盟發佈的規格](https://www.wi-fi.org/)) 。 Wi-Fi 點對點技術規格的目標是要提供解決方案來 Wi-Fi 裝置到裝置的連線能力，而不需要無線存取點， (無線 AP) 設定連線或使用現有的 Wi-Fi 臨機操作 (IBSS) 機制。

> [!Note]  
> 未來的 Windows 版本可能無法使用臨機操作模式。 從 Windows 8.1 和 Windows Server 2012 R2 開始，請改用 Wi-Fi 直接存取。

 

若為傳統型應用程式，Wi-Fi 直接功能需要使用者將 wi-fi Direct 裝置與 Windows 配對體驗使用者介面配對。 一旦完成這項配對，就會儲存設定檔，以允許使用 Wi-Fi 直接的函式來啟動 Wi-Fi 直接會話，以建立 Wi-Fi 直接裝置之間的連接。

下列函數支援 Wi-Fi 直接功能。

-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) -表示應用程式想要取消尚未完成的暫止 [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) 函數。
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) -關閉 Wi-Fi Direct 服務的控制碼。
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) -在先前成功呼叫 [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) 函數之後關閉會話。
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) -開啟 Wi-Fi Direct 服務的控制碼，並協商要使用的 WI-FI 直接 API 版本。
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) -針對 Wi-Fi Direct 舊版裝置，取得並套用已儲存的設定檔。
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -啟動特定 Wi-Fi 直接裝置的隨選連線，先前已透過 Windows 配對體驗配對。
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) -針對指定的已安裝 Wi-Fi 直接裝置節點，更新 Wi-Fi 直接裝置位址的裝置可見度。
-   [**WFD \_OPEN \_ SESSION \_ COMPLETE \_ 回呼**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)-定義 **WFDStartOpenSession** 作業完成時， [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)函式所呼叫的回呼函數

如需在傳統型應用程式中使用 Wi-Fi Direct 的詳細資訊，請參閱 [使用 Wi-Fi 直接功能](using-the-wi-fi-direct-api.md)。

如需 Wi-Fi 直接在 Windows Store 應用程式中使用的詳細資訊，請參閱 Windows 中的 [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)和相關類別 [**。網路功能。鄰近**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)命名空間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**其他資源**
</dt> <dt>

[關於原生 Wifi](about-native-wifi.md)
</dt> <dt>

[關於原生 Wifi API](about-the-native-wifi-api.md)
</dt> <dt>

[關於無線特定 API](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[使用 Wi-Fi Direct 函數](using-the-wi-fi-direct-api.md)
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

 

 
