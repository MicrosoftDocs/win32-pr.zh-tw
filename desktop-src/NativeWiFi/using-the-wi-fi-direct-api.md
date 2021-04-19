---
description: 示範如何在桌面應用程式中使用 Wi-Fi Direct 函式。
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: 使用 Wi-Fi Direct 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993116"
---
# <a name="using-the-wi-fi-direct-functions"></a><span data-ttu-id="76d5e-103">使用 Wi-Fi Direct 函數</span><span class="sxs-lookup"><span data-stu-id="76d5e-103">Using the Wi-Fi Direct functions</span></span>

<span data-ttu-id="76d5e-104">本主題說明如何在桌面應用程式中使用 Wi-Fi Direct 函式。</span><span class="sxs-lookup"><span data-stu-id="76d5e-104">This topics shows how to use Wi-Fi Direct functions in desktop apps.</span></span> <span data-ttu-id="76d5e-105">從 Windows 8 和 Windows Server 2012 開始，Wi-Fi 直接功能已新增至原生 Wifi API。</span><span class="sxs-lookup"><span data-stu-id="76d5e-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="76d5e-106">Wi-Fi 直接功能是以 Wi-Fi 聯盟的 Wi-Fi 對等技術規格 v1.1 開發為基礎， (查看 [Wi-fi 同盟發佈的規格](https://www.wi-fi.org/)) 。</span><span class="sxs-lookup"><span data-stu-id="76d5e-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="76d5e-107">Wi-Fi 點對點技術規格的目標是要提供解決方案來 Wi-Fi 裝置到裝置的連線能力，而不需要無線存取點， (無線 AP) 設定連線或使用現有的 Wi-Fi 臨機操作 (IBSS) 機制。</span><span class="sxs-lookup"><span data-stu-id="76d5e-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="76d5e-108">未來的 Windows 版本可能無法使用臨機操作模式。</span><span class="sxs-lookup"><span data-stu-id="76d5e-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="76d5e-109">從 Windows 8.1 和 Windows Server 2012 R2 開始，請改用 Wi-Fi Direct。</span><span class="sxs-lookup"><span data-stu-id="76d5e-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="76d5e-110">下列函數支援 Wi-Fi 直接功能。</span><span class="sxs-lookup"><span data-stu-id="76d5e-110">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="76d5e-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) -表示應用程式想要取消尚未完成的暫止 [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) 函數。</span><span class="sxs-lookup"><span data-stu-id="76d5e-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="76d5e-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) -關閉 Wi-Fi Direct 服務的控制碼。</span><span class="sxs-lookup"><span data-stu-id="76d5e-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="76d5e-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) -在先前成功呼叫 [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) 函數之後關閉會話。</span><span class="sxs-lookup"><span data-stu-id="76d5e-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="76d5e-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) -開啟 Wi-Fi Direct 服務的控制碼，並協商要使用的 WI-FI 直接 API 版本。</span><span class="sxs-lookup"><span data-stu-id="76d5e-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="76d5e-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) -針對 Wi-Fi Direct 舊版裝置，取得並套用已儲存的設定檔。</span><span class="sxs-lookup"><span data-stu-id="76d5e-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="76d5e-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -啟動特定 Wi-Fi 直接裝置的隨選連線，這是先前已透過 Windows 配對體驗配對的裝置。</span><span class="sxs-lookup"><span data-stu-id="76d5e-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="76d5e-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) -針對指定的已安裝 Wi-Fi 直接裝置節點，更新 Wi-Fi 直接裝置位址的裝置可見度。</span><span class="sxs-lookup"><span data-stu-id="76d5e-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="76d5e-118">[**WFD \_OPEN \_ SESSION \_ COMPLETE \_ 回呼**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)-定義 **WFDStartOpenSession** 作業完成時， [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)函式所呼叫的回呼函數</span><span class="sxs-lookup"><span data-stu-id="76d5e-118">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="76d5e-119">若為傳統型應用程式，Wi-Fi 直接功能要求使用者必須將 Wi-fi Direct 裝置與 Windows 配對體驗使用者介面配對。</span><span class="sxs-lookup"><span data-stu-id="76d5e-119">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="76d5e-120">一旦完成這項配對，就會儲存設定檔，以允許使用 Wi-Fi 直接的函式來啟動 Wi-Fi 直接會話，以建立 Wi-Fi 直接裝置之間的連接。</span><span class="sxs-lookup"><span data-stu-id="76d5e-120">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="76d5e-121">若要使用 Wi-Fi Direct，應用程式必須先呼叫 [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) 函式，以取得 Wi-Fi 直接服務的控制碼。</span><span class="sxs-lookup"><span data-stu-id="76d5e-121">In order to use Wi-Fi Direct, an app must first obtain a handle to the Wi-Fi Direct service by calling the [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) function.</span></span> <span data-ttu-id="76d5e-122">**WFDOpenHandle** 函式所傳回的 Wi-Fi DIRECT (WFD) 控制碼，會用於後續 Wi-Fi 對 Wi-Fi 直接服務的直接函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="76d5e-122">The Wi-Fi Direct (WFD) handle returned by the **WFDOpenHandle** function is used for subsequent Wi-Fi Direct function calls made to the Wi-Fi Direct service.</span></span>

<span data-ttu-id="76d5e-123">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)函式會啟動非同步作業，以啟動特定 Wi-Fi 直接裝置的隨選連接。</span><span class="sxs-lookup"><span data-stu-id="76d5e-123">The [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function starts an asynchronous operation to start an on-demand connection to a specific Wi-Fi Direct device.</span></span> <span data-ttu-id="76d5e-124">目標 Wi-Fi 裝置之前必須經過 Windows 配對體驗的配對。</span><span class="sxs-lookup"><span data-stu-id="76d5e-124">The target Wi-Fi device must previously have been paired through the Windows Pairing experience.</span></span> <span data-ttu-id="76d5e-125">當非同步作業完成時，會呼叫 *pfnCallback* 參數中指定的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="76d5e-125">When the asynchronous operation completes, the callback function specified in the *pfnCallback* parameter is called.</span></span>

<span data-ttu-id="76d5e-126">使用 Wi-Fi Direct 服務完成應用程式之後，應用程式應該呼叫 [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) 函式，以通知 Wi-Fi 直接服務，應用程式是使用服務完成的。</span><span class="sxs-lookup"><span data-stu-id="76d5e-126">Once an application is done using the Wi-Fi Direct service, the application should call the [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) function to signal to the Wi-Fi Direct service that the application is done using the service.</span></span> <span data-ttu-id="76d5e-127">這可讓 Wi-Fi 的直接服務釋放應用程式所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="76d5e-127">This allows the Wi-Fi Direct service to release resources used by the application.</span></span>

<span data-ttu-id="76d5e-128">如需有關在 Windows Store 應用程式中使用 Wi-Fi Direct 的詳細資訊，請參閱 [**Windows**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)中的與相關類別。</span><span class="sxs-lookup"><span data-stu-id="76d5e-128">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76d5e-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="76d5e-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="76d5e-130">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="76d5e-130">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="76d5e-131">關於原生 Wifi</span><span class="sxs-lookup"><span data-stu-id="76d5e-131">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="76d5e-132">關於原生 Wifi API</span><span class="sxs-lookup"><span data-stu-id="76d5e-132">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="76d5e-133">關於 Wi-Fi 直接功能</span><span class="sxs-lookup"><span data-stu-id="76d5e-133">About the Wi-Fi Direct feature</span></span>](about-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="76d5e-134">**參考**</span><span class="sxs-lookup"><span data-stu-id="76d5e-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="76d5e-135">**PeerFinder**</span><span class="sxs-lookup"><span data-stu-id="76d5e-135">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="76d5e-136">**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="76d5e-136">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="76d5e-137">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="76d5e-137">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="76d5e-138">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="76d5e-138">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="76d5e-139">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="76d5e-139">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="76d5e-140">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="76d5e-140">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="76d5e-141">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="76d5e-141">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="76d5e-142">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="76d5e-142">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="76d5e-143">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="76d5e-143">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="76d5e-144">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="76d5e-144">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
