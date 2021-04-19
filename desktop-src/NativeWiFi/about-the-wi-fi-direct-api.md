---
description: 原生 Wifi API 包含一組支援對傳統型應用程式使用 Wi-Fi Direct 的函式。
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: 關於 Wi-Fi 直接功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e503cb2bf86f81904b1c85c2bdf96b66c0762e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981211"
---
# <a name="about-the-wi-fi-direct-feature"></a><span data-ttu-id="fc7c9-103">關於 Wi-Fi 直接功能</span><span class="sxs-lookup"><span data-stu-id="fc7c9-103">About the Wi-Fi Direct feature</span></span>

<span data-ttu-id="fc7c9-104">原生 Wifi API 包含一組支援對傳統型應用程式使用 Wi-Fi Direct 的函式。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-104">The Native Wifi API contains a set of functions that support the use of Wi-Fi Direct for desktop apps.</span></span> <span data-ttu-id="fc7c9-105">從 Windows 8 和 Windows Server 2012 開始，Wi-Fi 直接功能已新增至原生 Wifi API。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="fc7c9-106">Wi-Fi 直接功能是以 Wi-Fi 聯盟的 Wi-Fi 對等技術規格 v1.1 開發為基礎， (查看 [Wi-fi 同盟發佈的規格](https://www.wi-fi.org/)) 。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="fc7c9-107">Wi-Fi 點對點技術規格的目標是要提供解決方案來 Wi-Fi 裝置到裝置的連線能力，而不需要無線存取點， (無線 AP) 設定連線或使用現有的 Wi-Fi 臨機操作 (IBSS) 機制。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="fc7c9-108">未來的 Windows 版本可能無法使用臨機操作模式。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="fc7c9-109">從 Windows 8.1 和 Windows Server 2012 R2 開始，請改用 Wi-Fi Direct。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="fc7c9-110">若為傳統型應用程式，Wi-Fi 直接功能要求使用者必須將 Wi-fi Direct 裝置與 Windows 配對體驗使用者介面配對。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-110">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="fc7c9-111">一旦完成這項配對，就會儲存設定檔，以允許使用 Wi-Fi 直接的函式來啟動 Wi-Fi 直接會話，以建立 Wi-Fi 直接裝置之間的連接。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-111">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="fc7c9-112">下列函數支援 Wi-Fi 直接功能。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-112">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="fc7c9-113">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) -表示應用程式想要取消尚未完成的暫止 [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) 函數。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-113">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="fc7c9-114">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) -關閉 Wi-Fi Direct 服務的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-114">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="fc7c9-115">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) -在先前成功呼叫 [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) 函數之後關閉會話。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-115">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="fc7c9-116">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) -開啟 Wi-Fi Direct 服務的控制碼，並協商要使用的 WI-FI 直接 API 版本。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-116">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="fc7c9-117">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) -針對 Wi-Fi Direct 舊版裝置，取得並套用已儲存的設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-117">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="fc7c9-118">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -啟動特定 Wi-Fi 直接裝置的隨選連線，這是先前已透過 Windows 配對體驗配對的裝置。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-118">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="fc7c9-119">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) -針對指定的已安裝 Wi-Fi 直接裝置節點，更新 Wi-Fi 直接裝置位址的裝置可見度。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-119">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="fc7c9-120">[**WFD \_OPEN \_ SESSION \_ COMPLETE \_ 回呼**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)-定義 **WFDStartOpenSession** 作業完成時， [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)函式所呼叫的回呼函數</span><span class="sxs-lookup"><span data-stu-id="fc7c9-120">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="fc7c9-121">如需在傳統型應用程式中使用 Wi-Fi Direct 的詳細資訊，請參閱 [使用 Wi-Fi 直接功能](using-the-wi-fi-direct-api.md)。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-121">For more information on using Wi-Fi Direct in a desktop app, see [Using the Wi-Fi Direct functions](using-the-wi-fi-direct-api.md).</span></span>

<span data-ttu-id="fc7c9-122">如需有關在 Windows Store 應用程式中使用 Wi-Fi Direct 的詳細資訊，請參閱 [**Windows**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)中的與相關類別。</span><span class="sxs-lookup"><span data-stu-id="fc7c9-122">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc7c9-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc7c9-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fc7c9-124">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-124">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fc7c9-125">關於原生 Wifi</span><span class="sxs-lookup"><span data-stu-id="fc7c9-125">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="fc7c9-126">關於原生 Wifi API</span><span class="sxs-lookup"><span data-stu-id="fc7c9-126">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="fc7c9-127">關於無線特定 API</span><span class="sxs-lookup"><span data-stu-id="fc7c9-127">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="fc7c9-128">使用 Wi-Fi Direct 函數</span><span class="sxs-lookup"><span data-stu-id="fc7c9-128">Using the Wi-Fi Direct functions</span></span>](using-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="fc7c9-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fc7c9-130">**PeerFinder**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-130">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="fc7c9-131">**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-131">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="fc7c9-132">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-132">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="fc7c9-133">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-133">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="fc7c9-134">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-134">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="fc7c9-135">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-135">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="fc7c9-136">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-136">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="fc7c9-137">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-137">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="fc7c9-138">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-138">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="fc7c9-139">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="fc7c9-139">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
