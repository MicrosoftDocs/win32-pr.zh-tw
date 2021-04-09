---
title: MsRdpClient8 類別
description: Microsoft RDP 用戶端控制 (可轉散發套件) -第9版。
ms.assetid: 877D475B-E2B4-46FB-B7A1-D376F6AE6B8D
ms.tgt_platform: multiple
keywords:
- MsRdpClient8 類別遠端桌面服務
- MsRdpClient8 類別遠端桌面服務，說明
topic_type:
- apiref
api_name:
- MsRdpClient8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc1410df2be1b738d217372a563cfdef13cbc3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934114"
---
# <a name="msrdpclient8-class"></a><span data-ttu-id="786ac-105">MsRdpClient8 類別</span><span class="sxs-lookup"><span data-stu-id="786ac-105">MsRdpClient8 class</span></span>

<span data-ttu-id="786ac-106">Microsoft RDP 用戶端控制 (可轉散發套件) -第9版</span><span class="sxs-lookup"><span data-stu-id="786ac-106">Microsoft RDP Client Control (redistributable) - version 9</span></span>

<span data-ttu-id="786ac-107">這個類別會執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="786ac-107">This class implements the following interfaces.</span></span>

-   [<span data-ttu-id="786ac-108">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="786ac-108">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
-   [<span data-ttu-id="786ac-109">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="786ac-109">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
-   [<span data-ttu-id="786ac-110">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="786ac-110">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
-   [<span data-ttu-id="786ac-111">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="786ac-111">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
-   [<span data-ttu-id="786ac-112">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="786ac-112">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
-   [<span data-ttu-id="786ac-113">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="786ac-113">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
-   [<span data-ttu-id="786ac-114">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="786ac-114">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
-   [<span data-ttu-id="786ac-115">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="786ac-115">**IMsRdpClient**</span></span>](imsrdpclientshell2.md)
-   [<span data-ttu-id="786ac-116">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="786ac-116">**IMsTscAx**</span></span>](imstscax-interface.md)
-   [<span data-ttu-id="786ac-117">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="786ac-117">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [<span data-ttu-id="786ac-118">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="786ac-118">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
-   [<span data-ttu-id="786ac-119">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="786ac-119">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
-   [<span data-ttu-id="786ac-120">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="786ac-120">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
-   [<span data-ttu-id="786ac-121">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="786ac-121">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
-   [<span data-ttu-id="786ac-122">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="786ac-122">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
-   [<span data-ttu-id="786ac-123">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="786ac-123">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
-   [<span data-ttu-id="786ac-124">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="786ac-124">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
-   [<span data-ttu-id="786ac-125">**IMsRdpPreferredRedirectionInfo**</span><span class="sxs-lookup"><span data-stu-id="786ac-125">**IMsRdpPreferredRedirectionInfo**</span></span>](imsrdppreferredredirectioninfo.md)

<span data-ttu-id="786ac-126">**MsRdpClient8** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="786ac-126">**MsRdpClient8** has these types of members:</span></span>

-   [<span data-ttu-id="786ac-127">方法</span><span class="sxs-lookup"><span data-stu-id="786ac-127">Methods</span></span>](#methods)
-   [<span data-ttu-id="786ac-128">屬性</span><span class="sxs-lookup"><span data-stu-id="786ac-128">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="786ac-129">方法</span><span class="sxs-lookup"><span data-stu-id="786ac-129">Methods</span></span>

<span data-ttu-id="786ac-130">**MsRdpClient8** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="786ac-130">The **MsRdpClient8** class has these methods.</span></span>



| <span data-ttu-id="786ac-131">方法</span><span class="sxs-lookup"><span data-stu-id="786ac-131">Method</span></span>                                                                                      | <span data-ttu-id="786ac-132">描述</span><span class="sxs-lookup"><span data-stu-id="786ac-132">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="786ac-133">**連接**</span><span class="sxs-lookup"><span data-stu-id="786ac-133">**Connect**</span></span>](imstscax-connect.md)                                                         | <span data-ttu-id="786ac-134">使用目前在控制項上設定的屬性起始連接。</span><span class="sxs-lookup"><span data-stu-id="786ac-134">Initiates a connection using the properties currently set on the control.</span></span><br/>                                                                                                                                                                                                          |
| [<span data-ttu-id="786ac-135">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="786ac-135">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)                             | <span data-ttu-id="786ac-136">針對每個指定的虛擬通道名稱建立用戶端虛擬通道物件。</span><span class="sxs-lookup"><span data-stu-id="786ac-136">Creates a client-side virtual channel object for each specified virtual channel name.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="786ac-137">**中斷連線**</span><span class="sxs-lookup"><span data-stu-id="786ac-137">**Disconnect**</span></span>](imstscax-disconnect.md)                                                   | <span data-ttu-id="786ac-138">中斷使用中連接。</span><span class="sxs-lookup"><span data-stu-id="786ac-138">Disconnects the active connection.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="786ac-139">**GetErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="786ac-139">**GetErrorDescription**</span></span>](imsrdpclient5-geterrordescription.md)                            | <span data-ttu-id="786ac-140">捕獲錯誤碼和錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="786ac-140">Retrieves the error codes and error messages.</span></span><br/>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="786ac-141">**GetStatusText**</span><span class="sxs-lookup"><span data-stu-id="786ac-141">**GetStatusText**</span></span>](imsrdpclient7-getstatustext.md)                                        | <span data-ttu-id="786ac-142">抓取指定狀態碼的狀態文字。</span><span class="sxs-lookup"><span data-stu-id="786ac-142">Retrieves the status text for the specified status code.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="786ac-143">**GetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="786ac-143">**GetVirtualChannelOptions**</span></span>](imsrdpclient-getvirtualchanneloptions.md)                   | <span data-ttu-id="786ac-144">抓取為虛擬通道設定的選項。</span><span class="sxs-lookup"><span data-stu-id="786ac-144">Retrieves the options set for a virtual channel.</span></span><br/>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="786ac-145">**NotifyRedirectDeviceChange**</span><span class="sxs-lookup"><span data-stu-id="786ac-145">**NotifyRedirectDeviceChange**</span></span>](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | <span data-ttu-id="786ac-146">通知遠端桌面 ActiveX 控制項的裝置重新導向模組，表示系統上已發生裝置變更。</span><span class="sxs-lookup"><span data-stu-id="786ac-146">Notifies the device redirection module of the Remote Desktop ActiveX control that a device change has occurred on the system.</span></span> <span data-ttu-id="786ac-147">這個方法會將 [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) 通知傳遞給控制項。</span><span class="sxs-lookup"><span data-stu-id="786ac-147">This method passes [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) notifications to the control.</span></span><br/>                                                        |
| [<span data-ttu-id="786ac-148">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="786ac-148">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md) | <span data-ttu-id="786ac-149">在 ActiveX 控制項顯示驗證對話方塊之後呼叫 (例如，[憑證錯誤] 對話方塊) 。</span><span class="sxs-lookup"><span data-stu-id="786ac-149">Called after an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="786ac-150">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="786ac-150">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md) | <span data-ttu-id="786ac-151">在 ActiveX 控制項顯示驗證對話方塊之前呼叫 (例如，) [憑證錯誤] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="786ac-151">Called before an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="786ac-152">**OnAutoReconnected**</span><span class="sxs-lookup"><span data-stu-id="786ac-152">**OnAutoReconnected**</span></span>](imstscaxevents-onautoreconnected.md)                               | <span data-ttu-id="786ac-153">當用戶端控制項自動重新連接到遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-153">Called when the client control has automatically reconnected to a remote session.</span></span><br/>                                                                                                                                                                                                  |
| [<span data-ttu-id="786ac-154">**OnAutoReconnecting**</span><span class="sxs-lookup"><span data-stu-id="786ac-154">**OnAutoReconnecting**</span></span>](-imstscaxevents--onautoreconnecting.md)                           | <span data-ttu-id="786ac-155">當用戶端在自動重新連接會話與 RD 工作階段主機伺服器時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-155">Called when a client is in the process of automatically reconnecting a session with a RD Session Host server.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="786ac-156">**OnAutoReconnecting2**</span><span class="sxs-lookup"><span data-stu-id="786ac-156">**OnAutoReconnecting2**</span></span>](imstscaxevents-onautoreconnecting2.md)                           | <span data-ttu-id="786ac-157">當用戶端在自動重新連接會話與 RD 工作階段主機伺服器時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-157">Called when a client is in the process of automatically reconnecting a session with a RD Session Host server.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="786ac-158">**OnChannelReceivedData**</span><span class="sxs-lookup"><span data-stu-id="786ac-158">**OnChannelReceivedData**</span></span>](imstscaxevents-onchannelreceiveddata.md)                       | <span data-ttu-id="786ac-159">當用戶端在可編寫腳本的虛擬通道上接收資料時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-159">Called when the client receives data on a scriptable virtual channel.</span></span><br/>                                                                                                                                                                                                              |
| [<span data-ttu-id="786ac-160">**OnConfirmClose**</span><span class="sxs-lookup"><span data-stu-id="786ac-160">**OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)                                     | <span data-ttu-id="786ac-161">當用戶端呼叫 [**IMsRdpClient：： RequestClose**](imsrdpclient-requestclose.md) 方法時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-161">Called when the client calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="786ac-162">**OnConnected**</span><span class="sxs-lookup"><span data-stu-id="786ac-162">**OnConnected**</span></span>](imstscaxevents-onconnected.md)                                           | <span data-ttu-id="786ac-163">當用戶端控制項正在建立與 RD 工作階段主機 server 的連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-163">Called when the client control is in the process of establishing a connection with a RD Session Host server.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="786ac-164">**OnConnecting**</span><span class="sxs-lookup"><span data-stu-id="786ac-164">**OnConnecting**</span></span>](imstscaxevents-onconnecting.md)                                         | <span data-ttu-id="786ac-165">當用戶端控制項開始連接到伺服器以回應 [**IMsTscAx：： Connect**](imstscax-connect.md)的呼叫時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-165">Called when the client control begins connecting to a server in response to a call to [**IMsTscAx::Connect**](imstscax-connect.md).</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="786ac-166">**OnConnectionBarPullDown**</span><span class="sxs-lookup"><span data-stu-id="786ac-166">**OnConnectionBarPullDown**</span></span>](imstscaxevents-onconnectionbarpulldown.md)                   | <span data-ttu-id="786ac-167">當使用者在連接列上向下拖曳時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-167">Called when the user has dragged down on the connection bar.</span></span><br/>                                                                                                                                                                                                                       |
| [<span data-ttu-id="786ac-168">**OnDevicesButtonPressed**</span><span class="sxs-lookup"><span data-stu-id="786ac-168">**OnDevicesButtonPressed**</span></span>](imstscaxevents-ondevicesbuttonpressed.md)                     | <span data-ttu-id="786ac-169">當按下連接列中的 [裝置] 按鈕時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-169">Called when the devices button in the connection bar has been pressed.</span></span><br/>                                                                                                                                                                                                             |
| [<span data-ttu-id="786ac-170">**OnDisconnected**</span><span class="sxs-lookup"><span data-stu-id="786ac-170">**OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)                                     | <span data-ttu-id="786ac-171">當用戶端控制項與 RD 工作階段主機伺服器中斷連線時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-171">Called when the client control has been disconnected from the RD Session Host server.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="786ac-172">**OnEnterFullScreenMode**</span><span class="sxs-lookup"><span data-stu-id="786ac-172">**OnEnterFullScreenMode**</span></span>](imstscaxevents-onenterfullscreenmode.md)                       | <span data-ttu-id="786ac-173">當用戶端進入全螢幕模式時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-173">Called when the client enters full-screen mode.</span></span> <span data-ttu-id="786ac-174">例如，當使用者按下全螢幕模式 [快速鍵](terminal-services-shortcut-keys.md) 組合 (CTRL + ALT + BREAK) 時，就會呼叫此事件。</span><span class="sxs-lookup"><span data-stu-id="786ac-174">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span><br/>                                                                     |
| [<span data-ttu-id="786ac-175">**OnFatalError**</span><span class="sxs-lookup"><span data-stu-id="786ac-175">**OnFatalError**</span></span>](imstscaxevents-onfatalerror.md)                                         | <span data-ttu-id="786ac-176">當用戶端控制項遇到嚴重錯誤時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-176">Called when the client control encounters a fatal error.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="786ac-177">**OnFocusReleased**</span><span class="sxs-lookup"><span data-stu-id="786ac-177">**OnFocusReleased**</span></span>](imstscaxevents-onfocusreleased.md)                                   | <span data-ttu-id="786ac-178">在按下放開焦點按鍵組合時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-178">Called when the release focus key combination is pressed.</span></span> <span data-ttu-id="786ac-179">例如，當使用者按下 CTRL + ALT + 向左鍵或 CTRL + ALT + 向右鍵按鍵組合時，就會呼叫此事件。</span><span class="sxs-lookup"><span data-stu-id="786ac-179">For example, this event is called when the user presses the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination.</span></span><br/>                                                                                             |
| [<span data-ttu-id="786ac-180">**OnIdleTimeoutNotification**</span><span class="sxs-lookup"><span data-stu-id="786ac-180">**OnIdleTimeoutNotification**</span></span>](imstscaxevents-onidletimeoutnotification.md)               | <span data-ttu-id="786ac-181">當使用者在 [**IMsRdpClientAdvancedSettings：:p 長 \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) 方法設定期間沒有滑鼠或鍵盤輸入時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-181">Called when there has been no mouse or keyboard input by the user during the period of time set by the [**IMsRdpClientAdvancedSettings::put\_MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) method.</span></span><br/>                                                |
| [<span data-ttu-id="786ac-182">**OnLeaveFullScreenMode**</span><span class="sxs-lookup"><span data-stu-id="786ac-182">**OnLeaveFullScreenMode**</span></span>](imstscaxevents-onleavefullscreenmode.md)                       | <span data-ttu-id="786ac-183">當用戶端離開全螢幕模式時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-183">Called when the client leaves full-screen mode.</span></span> <span data-ttu-id="786ac-184">例如，當使用者按下全螢幕模式 [快速鍵](terminal-services-shortcut-keys.md) 組合 (CTRL + ALT + BREAK) 時，就會呼叫此事件。</span><span class="sxs-lookup"><span data-stu-id="786ac-184">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span><br/>                                                                     |
| [<span data-ttu-id="786ac-185">**OnLoginComplete**</span><span class="sxs-lookup"><span data-stu-id="786ac-185">**OnLoginComplete**</span></span>](imstscaxevents-onlogincomplete.md)                                   | <span data-ttu-id="786ac-186">當用戶端控制項成功登入 RD 工作階段主機伺服器時呼叫，並遵循 Windows 登入對話方塊的顯示。</span><span class="sxs-lookup"><span data-stu-id="786ac-186">Called when the client control has successfully logged on to a RD Session Host server, following the display of the Windows Logon dialog box.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="786ac-187">**OnLogonError**</span><span class="sxs-lookup"><span data-stu-id="786ac-187">**OnLogonError**</span></span>](imstscaxevents-onlogonerror.md)                                         | <span data-ttu-id="786ac-188">發生登入錯誤或其他登入事件時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-188">Called when a logon error or other logon event occurs.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="786ac-189">**OnMouseInputModeChanged**</span><span class="sxs-lookup"><span data-stu-id="786ac-189">**OnMouseInputModeChanged**</span></span>](imstscaxevents-onmouseinputmodechanged.md)                   | <span data-ttu-id="786ac-190">當滑鼠輸入模式變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-190">Called when the mouse input mode has changed.</span></span><br/>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="786ac-191">**OnNetworkStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="786ac-191">**OnNetworkStatusChanged**</span></span>](imstscaxevents-onnetworkstatuschanged.md)                     | <span data-ttu-id="786ac-192">在網路狀態變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-192">Called when the network status has changed.</span></span><br/>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="786ac-193">**OnReceivedTSPublicKey**</span><span class="sxs-lookup"><span data-stu-id="786ac-193">**OnReceivedTSPublicKey**</span></span>](imstscaxevents-onreceivedtspublickey.md)                       | <span data-ttu-id="786ac-194">當用戶端從伺服器抓取公開金鑰時，在連接順序中呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-194">Called during the connection sequence when the client retrieves the public key from the server.</span></span> <span data-ttu-id="786ac-195">只有當 **NotifyTSPublicKey** 屬性為 **VARIANT \_ TRUE** 時，才會呼叫此事件。</span><span class="sxs-lookup"><span data-stu-id="786ac-195">This event is only called if the **NotifyTSPublicKey** property is **VARIANT\_TRUE**.</span></span><br/>                                                                                              |
| [<span data-ttu-id="786ac-196">**OnRemoteDesktopSizeChange**</span><span class="sxs-lookup"><span data-stu-id="786ac-196">**OnRemoteDesktopSizeChange**</span></span>](imstscaxevents-onremotedesktopsizechange.md)               | <span data-ttu-id="786ac-197">呼叫以表示遠端桌面上的用戶端控制項大小已變更，以回應用戶端控制作業。</span><span class="sxs-lookup"><span data-stu-id="786ac-197">Called to indicate that the size of the client control on the remote desktop has changed in response to a client control operation.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="786ac-198">**OnRemoteProgramDisplayed**</span><span class="sxs-lookup"><span data-stu-id="786ac-198">**OnRemoteProgramDisplayed**</span></span>](imstscaxevents-onremoteprogramdisplayed.md)                 | <span data-ttu-id="786ac-199">在顯示 RemoteApp 程式時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-199">Called when a RemoteApp program is displayed.</span></span><br/>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="786ac-200">**OnRemoteProgramResult**</span><span class="sxs-lookup"><span data-stu-id="786ac-200">**OnRemoteProgramResult**</span></span>](imstscaxevents-onremoteprogramresult.md)                       | <span data-ttu-id="786ac-201">當 RemoteApp 程式傳回結果給用戶端控制項時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-201">Called when a RemoteApp program returns a result to the client control.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="786ac-202">**OnRemoteWindowDisplayed**</span><span class="sxs-lookup"><span data-stu-id="786ac-202">**OnRemoteWindowDisplayed**</span></span>](imstscaxevents-onremotewindowdisplayed.md)                   | <span data-ttu-id="786ac-203">當 RemoteApp 視窗顯示時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-203">Called when a RemoteApp window is displayed.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="786ac-204">**OnRequestContainerMinimize**</span><span class="sxs-lookup"><span data-stu-id="786ac-204">**OnRequestContainerMinimize**</span></span>](imstscaxevents-onrequestcontainerminimize.md)             | <span data-ttu-id="786ac-205">當使用者在全螢幕模式下的連接列上按下 **最小化** 按鈕時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-205">Called when the user presses the **Minimize** button on the connection bar in full-screen mode.</span></span> <span data-ttu-id="786ac-206">引發此事件是容器應用程式本身最小化的要求。</span><span class="sxs-lookup"><span data-stu-id="786ac-206">The firing of this event is a request that the container application minimize itself.</span></span><br/>                                                                                              |
| [<span data-ttu-id="786ac-207">**OnRequestGoFullScreen**</span><span class="sxs-lookup"><span data-stu-id="786ac-207">**OnRequestGoFullScreen**</span></span>](imstscaxevents-onrequestgofullscreen.md)                       | <span data-ttu-id="786ac-208">當用戶端要求切換至全螢幕模式並呼叫 [**IMsTscAdvancedSettings：:p 使用 \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) 方法時呼叫，以將 **ContainerHandledFullScreen** 屬性設定為非零值。</span><span class="sxs-lookup"><span data-stu-id="786ac-208">Called when the client requests to switch to full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called to set the **ContainerHandledFullScreen** property to a nonzero value.</span></span><br/> |
| [<span data-ttu-id="786ac-209">**OnRequestLeaveFullScreen**</span><span class="sxs-lookup"><span data-stu-id="786ac-209">**OnRequestLeaveFullScreen**</span></span>](imstscaxevents-onrequestleavefullscreen.md)                 | <span data-ttu-id="786ac-210">當用戶端要求離開全螢幕模式，且 [**IMsTscAdvancedSettings：:p 的 \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) 屬性已設定為非零值時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-210">Called when the client requests to leave full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) property has been set to a nonzero value.</span></span><br/>                                                   |
| [<span data-ttu-id="786ac-211">**OnServiceMessageReceived**</span><span class="sxs-lookup"><span data-stu-id="786ac-211">**OnServiceMessageReceived**</span></span>](imstscaxevents-onservicemessagereceived.md)                 | <span data-ttu-id="786ac-212">當用戶端收到系統訊息時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-212">Called when the client receives a system message.</span></span><br/>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="786ac-213">**OnUserNameAcquired**</span><span class="sxs-lookup"><span data-stu-id="786ac-213">**OnUserNameAcquired**</span></span>](imstscaxevents-onusernameacquired.md)                             | <span data-ttu-id="786ac-214">當控制項取得使用者名稱時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-214">Called when the user name has been acquired by the control.</span></span><br/>                                                                                                                                                                                                                        |
| [<span data-ttu-id="786ac-215">**OnWarning**</span><span class="sxs-lookup"><span data-stu-id="786ac-215">**OnWarning**</span></span>](imstscaxevents-onwarning.md)                                               | <span data-ttu-id="786ac-216">當用戶端控制項遇到不嚴重的錯誤狀況時呼叫。</span><span class="sxs-lookup"><span data-stu-id="786ac-216">Called when the client control encounters an error condition that is not fatal.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="786ac-217">**重新連接**</span><span class="sxs-lookup"><span data-stu-id="786ac-217">**Reconnect**</span></span>](imsrdpclient8-reconnect.md)                                                | <span data-ttu-id="786ac-218">重新連接到具有新桌面寬度和高度的遠端會話。</span><span class="sxs-lookup"><span data-stu-id="786ac-218">Reconnects to the remote session with the new desktop width and height.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="786ac-219">**RequestClose**</span><span class="sxs-lookup"><span data-stu-id="786ac-219">**RequestClose**</span></span>](imsrdpclient-requestclose.md)                                           | <span data-ttu-id="786ac-220">要求正常關機用戶端控制項。</span><span class="sxs-lookup"><span data-stu-id="786ac-220">Requests a graceful shutdown of the client control.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="786ac-221">**ResetPassword**</span><span class="sxs-lookup"><span data-stu-id="786ac-221">**ResetPassword**</span></span>](imstscnonscriptable-resetpassword.md)                                  | <span data-ttu-id="786ac-222">重設控制項中的所有密碼狀態。</span><span class="sxs-lookup"><span data-stu-id="786ac-222">Resets all password states in the control.</span></span><br/>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="786ac-223">**SendKeys**</span><span class="sxs-lookup"><span data-stu-id="786ac-223">**SendKeys**</span></span>](imsrdpclientnonscriptable-sendkeys.md)                                      | <span data-ttu-id="786ac-224">將一連串的按鍵傳送到控制項。</span><span class="sxs-lookup"><span data-stu-id="786ac-224">Sends a series of keystrokes to the control.</span></span> <span data-ttu-id="786ac-225">按鍵是掃描程式碼形式，也就是實際實體索引鍵的鍵盤資料。</span><span class="sxs-lookup"><span data-stu-id="786ac-225">The keystrokes are in scan code form, which is the keyboard data from the actual physical keys.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="786ac-226">**SendOnVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="786ac-226">**SendOnVirtualChannel**</span></span>](imstscax-sendonvirtualchannel.md)                               | <span data-ttu-id="786ac-227">透過先前使用 [**IMsTscAx：： CreateVirtualChannels**](imstscax-createvirtualchannels.md) 方法建立的虛擬通道，將資料傳送至 RD 工作階段主機伺服器。</span><span class="sxs-lookup"><span data-stu-id="786ac-227">Sends data to the RD Session Host server over a virtual channel that was created previously by using the [**IMsTscAx::CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span><br/>                                                                                         |
| [<span data-ttu-id="786ac-228">**SendRemoteAction**</span><span class="sxs-lookup"><span data-stu-id="786ac-228">**SendRemoteAction**</span></span>](imsrdpclient8-sendremoteaction.md)                                  | <span data-ttu-id="786ac-229">使動作在遠端會話中執行。</span><span class="sxs-lookup"><span data-stu-id="786ac-229">Causes an action to be performed in the remote session.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="786ac-230">**SetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="786ac-230">**SetVirtualChannelOptions**</span></span>](imsrdpclient-setvirtualchanneloptions.md)                   | <span data-ttu-id="786ac-231">設定用戶端控制項的虛擬通道選項。</span><span class="sxs-lookup"><span data-stu-id="786ac-231">Sets the virtual channel options for the client control.</span></span><br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a><span data-ttu-id="786ac-232">屬性</span><span class="sxs-lookup"><span data-stu-id="786ac-232">Properties</span></span>

<span data-ttu-id="786ac-233">**MsRdpClient8** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="786ac-233">The **MsRdpClient8** class has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="786ac-234">屬性</span><span class="sxs-lookup"><span data-stu-id="786ac-234">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="786ac-235">存取類型</span><span class="sxs-lookup"><span data-stu-id="786ac-235">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="786ac-236">Description</span><span class="sxs-lookup"><span data-stu-id="786ac-236">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-237"><a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-237"><a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-238">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-238">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-239"><a href="imstscadvancedsettings-interface.md"><strong>IMsTscAdvancedSettings</strong></a>介面指標。</span><span class="sxs-lookup"><span data-stu-id="786ac-239">An <a href="imstscadvancedsettings-interface.md"><strong>IMsTscAdvancedSettings</strong></a> interface pointer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-240"><a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-240"><a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-241">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-241">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-242"><a href="imsrdpclientadvancedsettings-interface.md"><strong>IMsRdpClientAdvancedSettings</strong></a>介面的指標，用來設定用戶端控制項的 advanced 設定。</span><span class="sxs-lookup"><span data-stu-id="786ac-242">Pointer to the <a href="imsrdpclientadvancedsettings-interface.md"><strong>IMsRdpClientAdvancedSettings</strong></a> interface, used to set advanced settings for the client control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-243"><a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-243"><a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-244">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-244">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-245"><a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2</strong></a>介面的指標，用來設定用戶端控制項的 advanced 設定。</span><span class="sxs-lookup"><span data-stu-id="786ac-245">Pointer to the <a href="imsrdpclientadvancedsettings2.md"><strong>IMsRdpClientAdvancedSettings2</strong></a> interface, used to set advanced settings for the client control.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-246"><a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-246"><a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-247">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-247">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-248"><a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3</strong></a>介面的指標，用來設定用戶端控制項的 advanced 設定。</span><span class="sxs-lookup"><span data-stu-id="786ac-248">Pointer to the <a href="imsrdpclientadvancedsettings3.md"><strong>IMsRdpClientAdvancedSettings3</strong></a> interface, used to set advanced settings for the client control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-249"><a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-249"><a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-250">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-250">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-251"><a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4</strong></a>介面指標。</span><span class="sxs-lookup"><span data-stu-id="786ac-251">An <a href="imsrdpclientadvancedsettings4.md"><strong>IMsRdpClientAdvancedSettings4</strong></a> interface pointer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-252"><a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-252"><a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-253">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-253">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-254">要 <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>的介面。</span><span class="sxs-lookup"><span data-stu-id="786ac-254">The interface to <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-255"><a href="imsrdpclient6-advancedsettings7.md"><strong>AdvancedSettings7</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-255"><a href="imsrdpclient6-advancedsettings7.md"><strong>AdvancedSettings7</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-256">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-256">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-257">要 <a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6</strong></a>的介面。</span><span class="sxs-lookup"><span data-stu-id="786ac-257">The interface to <a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-258"><a href="imsrdpclient7-advancedsettings8.md"><strong>AdvancedSettings8</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-258"><a href="imsrdpclient7-advancedsettings8.md"><strong>AdvancedSettings8</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-259">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-259">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-260">支援 <a href="imsrdpclientadvancedsettings7.md"><strong>IMsRdpClientAdvancedSettings7</strong></a> 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="786ac-260">An object that supports the <a href="imsrdpclientadvancedsettings7.md"><strong>IMsRdpClientAdvancedSettings7</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-261"><a href="imsrdpclient8-advancedsettings9.md"><strong>AdvancedSettings9</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-261"><a href="imsrdpclient8-advancedsettings9.md"><strong>AdvancedSettings9</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-262">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-262">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-263">表示 settings 物件的 <a href="imsrdpclientadvancedsettings8.md"><strong>IMsRdpClientAdvancedSettings8</strong></a> 介面。</span><span class="sxs-lookup"><span data-stu-id="786ac-263">An <a href="imsrdpclientadvancedsettings8.md"><strong>IMsRdpClientAdvancedSettings8</strong></a> interface that represents the settings object.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-264"><a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>AllowCredentialSaving</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-264"><a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>AllowCredentialSaving</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-265">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-265">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-266">指定 [認證] 對話方塊是否顯示啟用儲存認證的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="786ac-266">Specifies whether the credentials dialog box displays a check box to enable the saving of credentials.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-267"><a href="imsrdpclientnonscriptable5-allowpromptingforcredentials.md"><strong>AllowPromptingForCredentials</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-267"><a href="imsrdpclientnonscriptable5-allowpromptingforcredentials.md"><strong>AllowPromptingForCredentials</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-268">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-268">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-269">指定遠端桌面 ActiveX 控制項是否可以提示使用者輸入認證。</span><span class="sxs-lookup"><span data-stu-id="786ac-269">Specifies whether the Remote Desktop ActiveX control can prompt the user for credentials.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-270"><a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-270"><a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-271">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-271">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-272">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="786ac-272">This property is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-273"><a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-273"><a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-274">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-274">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-275">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="786ac-275">This property is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-276"><a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-276"><a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-277">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-277">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-278">目前控制項的最大加密強度。</span><span class="sxs-lookup"><span data-stu-id="786ac-278">The maximum encryption strength of the current control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-279"><a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-279"><a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-280">唯寫</span><span class="sxs-lookup"><span data-stu-id="786ac-280">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-281">以純文字格式的遠端桌面 ActiveX 控制項密碼。</span><span class="sxs-lookup"><span data-stu-id="786ac-281">The Remote Desktop ActiveX control password, in plaintext format.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-282"><a href="imsrdpclient-colordepth.md"><strong>ColorDepth</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-282"><a href="imsrdpclient-colordepth.md"><strong>ColorDepth</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-283">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-283">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-284">目前控制項的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="786ac-284">Color depth of the current control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-285"><a href="imstscax-connected.md"><strong>連線</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-285"><a href="imstscax-connected.md"><strong>Connected</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-286">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-286">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-287">目前控制項的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="786ac-287">The connection state of the current control.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-288"><a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-288"><a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-289">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-289">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-290">控制項處於連接狀態時，在控制項的工作區中顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="786ac-290">Text that is displayed in the client area of the control while the control is in the connected state.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-291"><a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-291"><a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-292">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-292">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-293">控制項連接時，顯示在控制項中央的文字。</span><span class="sxs-lookup"><span data-stu-id="786ac-293">The text that appears centered in the control while the control is connecting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-294"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-294"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-295">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-295">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-296">要為連接列顯示的文字字串。</span><span class="sxs-lookup"><span data-stu-id="786ac-296">The text string to display for the connection bar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-297"><a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-297"><a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-298">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-298">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-299">目前的控制項在初始遠端桌面上的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="786ac-299">The current control's height, in pixels, on the initial remote desktop.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-300"><a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-300"><a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-301">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-301">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-302">目前的控制項寬度（以圖元為單位），在初始的遠端桌面。</span><span class="sxs-lookup"><span data-stu-id="786ac-302">The current control's width, in pixels, on the initial remote desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-303"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-303"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-304">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-304">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-305">可用於重新導向的 PnP 裝置集合。</span><span class="sxs-lookup"><span data-stu-id="786ac-305">The collection of PnP devices that are available for redirection.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-306"><a href="imsrdpclientnonscriptable5-disableconnectionbar.md"><strong>DisableConnectionBar</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-306"><a href="imsrdpclientnonscriptable5-disableconnectionbar.md"><strong>DisableConnectionBar</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-307">唯寫</span><span class="sxs-lookup"><span data-stu-id="786ac-307">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-308">指定遠端桌面 ActiveX 控制項是否應該停用連接列。</span><span class="sxs-lookup"><span data-stu-id="786ac-308">Specifies whether the Remote Desktop ActiveX control should disable the connection bar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-309"><a href="imsrdpclientnonscriptable5-disableremoteappcapscheck.md"><strong>DisableRemoteAppCapsCheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-309"><a href="imsrdpclientnonscriptable5-disableremoteappcapscheck.md"><strong>DisableRemoteAppCapsCheck</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-310">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-310">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-311">指定遠端桌面 ActiveX 控制項是否不應檢查伺服器的 RemoteApp 功能。</span><span class="sxs-lookup"><span data-stu-id="786ac-311">Specifies whether the Remote Desktop ActiveX control should not check the server for RemoteApp capabilities.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-312"><a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-312"><a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-313">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-313">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-314">在連接結束之前出現在控制項中央的文字。</span><span class="sxs-lookup"><span data-stu-id="786ac-314">The text that appears centered in the control before a connection is terminated.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-315"><a href="imstscax-domain.md"><strong>域</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-315"><a href="imstscax-domain.md"><strong>Domain</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-316">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-316">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-317">目前使用者登入的網域。</span><span class="sxs-lookup"><span data-stu-id="786ac-317">The domain to which the current user logs on.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-318"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-318"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-319">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-319">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-320">可用於重新導向的磁片磁碟機集合。</span><span class="sxs-lookup"><span data-stu-id="786ac-320">The collection of disk drives that is available for redirection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-321"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-321"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-322">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-322">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-323">指定是否啟用此連接的 CredSSP。</span><span class="sxs-lookup"><span data-stu-id="786ac-323">Specifies whether CredSSP is enabled for this connection.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-324"><a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-324"><a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-325">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-325">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-326">有關用戶端控制項中斷連接原因的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="786ac-326">Extended information about the client control's reason for disconnection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-327"><a href="imsrdpclient-fullscreen.md"><strong>FullScreen</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-327"><a href="imsrdpclient-fullscreen.md"><strong>FullScreen</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-328">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-328">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-329">指出控制項是否處於全螢幕模式。</span><span class="sxs-lookup"><span data-stu-id="786ac-329">Indicates whether the control is in full-screen mode.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-330"><a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-330"><a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-331">唯寫</span><span class="sxs-lookup"><span data-stu-id="786ac-331">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-332">當控制項處於全螢幕模式時，所顯示的視窗標題。</span><span class="sxs-lookup"><span data-stu-id="786ac-332">The window title displayed when the control is in full-screen mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-333"><a href="imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md"><strong>GetRemoteMonitorsBoundingBox</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-333"><a href="imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md"><strong>GetRemoteMonitorsBoundingBox</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-334">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-334">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-335">指定遠端監視的周框。</span><span class="sxs-lookup"><span data-stu-id="786ac-335">Specifies the bounding rectangle of the remote monitor.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-336"><a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-336"><a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-337">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-337">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-338">指出控制項是否已顯示水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="786ac-338">Indicates whether the control has displayed a horizontal scroll bar.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-339"><a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>LaunchedViaClientShellInterface</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-339"><a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>LaunchedViaClientShellInterface</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-340">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-340">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-341">指定使用者是否使用 RD Web 存取介面啟動用戶端控制項。</span><span class="sxs-lookup"><span data-stu-id="786ac-341">Specifies whether the user launched the client control by using the RD Web Access interface.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-342"><a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>MarkRdpSettingsSecure</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-342"><a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>MarkRdpSettingsSecure</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-343">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-343">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-344">指定是否將 RDP 設定標示為安全。</span><span class="sxs-lookup"><span data-stu-id="786ac-344">Specifies whether RDP settings are marked as secure.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-345"><a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-345"><a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-346">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-346">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-347">入口網站啟動器的用戶端設定。</span><span class="sxs-lookup"><span data-stu-id="786ac-347">The client settings for the web portal launcher.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-348"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-348"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-349">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-349">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-350">指定此連接是否支援 NegotiateSecurityLayer 設定。</span><span class="sxs-lookup"><span data-stu-id="786ac-350">Specifies whether the NegotiateSecurityLayer setting is supported for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="786ac-351">當 <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> 已啟用並存在於用戶端上，或當安全通訊端層 (SSL) 啟用使用者驗證時，會忽略 NegotiateSecurityLayer。</span><span class="sxs-lookup"><span data-stu-id="786ac-351">When <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> is enabled and present on the client, or when Secure Sockets Layer (SSL) is enabled with user authentication, NegotiateSecurityLayer is ignored.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-352"><a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-352"><a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-353">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-353">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-354">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="786ac-354">This property is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-355"><a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-355"><a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-356">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-356">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-357">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="786ac-357">This property is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-358"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-358"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-359">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-359">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-360">指定是否應顯示 [提示輸入認證] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="786ac-360">Specifies whether the prompt for credentials dialog box should be shown.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-361"><a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>PromptForCredsOnClient</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-361"><a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>PromptForCredsOnClient</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-362">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-362">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-363">指定用戶端控制項是否顯示提示輸入認證的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="786ac-363">Specifies whether the client control displays a dialog box that prompts for credentials.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-364"><a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>PublisherCertificateChain</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-364"><a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>PublisherCertificateChain</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-365">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-365">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-366">指定發行者的憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="786ac-366">Specifies the publisher certificate chain.</span></span> <span data-ttu-id="786ac-367">鏈會儲存在類型 VT_BYREF 的變數中，其中包含 <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="786ac-367">The chain is stored in a variant of type VT_BYREF that contains a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> structure.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-368"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-368"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-369">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-369">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-370">指定是否可重新導向會話中所列舉的動態連接 PnP 裝置。</span><span class="sxs-lookup"><span data-stu-id="786ac-370">Specifies whether dynamically attached PnP devices that are enumerated while in a session are available for redirection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-371"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-371"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-372">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-372">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-373">指定在會話中列舉的動態連接 PnP 磁片磁碟機是否可用於重新導向。</span><span class="sxs-lookup"><span data-stu-id="786ac-373">Specifies whether dynamically attached PnP drives that are enumerated while in a session are available for redirection.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-374"><a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>RedirectionWarningType</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-374"><a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>RedirectionWarningType</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-375">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-375">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-376">控制重新導向對話方塊的存在和外觀。</span><span class="sxs-lookup"><span data-stu-id="786ac-376">Controls the presence and appearance of the redirection dialog box.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-377"><a href="imsrdpclientnonscriptable5-remotemonitorcount.md"><strong>RemoteMonitorCount</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-377"><a href="imsrdpclientnonscriptable5-remotemonitorcount.md"><strong>RemoteMonitorCount</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-378">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-378">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-379">指定遠端監視的數目。</span><span class="sxs-lookup"><span data-stu-id="786ac-379">Specifies the number of remote monitors.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-380"><a href="imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md"><strong>RemoteMonitorLayoutMatchesLocal</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-380"><a href="imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md"><strong>RemoteMonitorLayoutMatchesLocal</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-381">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-381">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-382">指定遠端監視配置是否與本機監視器版面配置相同。</span><span class="sxs-lookup"><span data-stu-id="786ac-382">Specifies if the remote monitor layout is identical to the local monitor layout.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-383"><a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-383"><a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-384">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-384">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-385">用戶端 RemoteApp 設定。</span><span class="sxs-lookup"><span data-stu-id="786ac-385">The client RemoteApp setting.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-386"><a href="imsrdpclient7-remoteprogram2.md"><strong>RemoteProgram2</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-386"><a href="imsrdpclient7-remoteprogram2.md"><strong>RemoteProgram2</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-387">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-387">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-388">支援 <a href="itsremoteprogram2.md"><strong>ITSRemoteProgram2</strong></a> 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="786ac-388">An object that supports the <a href="itsremoteprogram2.md"><strong>ITSRemoteProgram2</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-389"><a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-389"><a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-390">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-390">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-391"><a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a>介面指標。</span><span class="sxs-lookup"><span data-stu-id="786ac-391">A <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> interface pointer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-392"><a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-392"><a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-393">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-393">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-394"><a href="imsrdpclientsecuredsettings-interface.md"><strong>IMsRdpClientSecuredSettings</strong></a>介面的指標，用來設定用戶端控制項的安全設定。</span><span class="sxs-lookup"><span data-stu-id="786ac-394">Pointer to the <a href="imsrdpclientsecuredsettings-interface.md"><strong>IMsRdpClientSecuredSettings</strong></a> interface, used to set secured settings for the client control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-395"><a href="imsrdpclient7-securedsettings3.md"><strong>SecuredSettings3</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-395"><a href="imsrdpclient7-securedsettings3.md"><strong>SecuredSettings3</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-396">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-396">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-397">支援 <a href="imsrdpclientsecuredsettings2.md"><strong>IMsRdpClientSecuredSettings2</strong></a> 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="786ac-397">An object that supports the <a href="imsrdpclientsecuredsettings2.md"><strong>IMsRdpClientSecuredSettings2</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-398"><a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-398"><a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-399">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-399">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-400">指出 <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> 介面是否可供使用。</span><span class="sxs-lookup"><span data-stu-id="786ac-400">Indicates whether the <a href="imstscsecuredsettings-interface.md"><strong>IMsTscSecuredSettings</strong></a> interface is available.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-401"><a href="imstscax-server.md"><strong>伺服器</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-401"><a href="imstscax-server.md"><strong>Server</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-402">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-402">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-403">目前控制項所連接的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="786ac-403">The name of the server to which the current control is connected.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-404"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-404"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-405">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-405">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-406">指定在啟動會話之前，是否應該顯示重新導向安全性警告對話方塊。</span><span class="sxs-lookup"><span data-stu-id="786ac-406">Specifies whether the redirection security warning dialog box should be shown before starting a session.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-407"><a href="imstscax-startconnected.md"><strong>StartConnected</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-407"><a href="imstscax-startconnected.md"><strong>StartConnected</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-408">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-408">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-409">指出控制項是否會在啟動時立即建立 RD 工作階段主機的伺服器連接。</span><span class="sxs-lookup"><span data-stu-id="786ac-409">Indicates whether the control will establish the RD Session Host server connection immediately upon startup.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-410"><a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-410"><a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-411">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-411">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-412">用戶端 RD 閘道設定。</span><span class="sxs-lookup"><span data-stu-id="786ac-412">The client RD Gateway setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-413"><a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-413"><a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-414">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-414">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-415">要 <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2</strong></a>的介面。</span><span class="sxs-lookup"><span data-stu-id="786ac-415">The interface to <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-416"><a href="imsrdpclient7-transportsettings3.md"><strong>TransportSettings3</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-416"><a href="imsrdpclient7-transportsettings3.md"><strong>TransportSettings3</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-417">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-417">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-418">支援 <a href="imsrdpclienttransportsettings3.md"><strong>IMsRdpClientTransportSettings3</strong></a> 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="786ac-418">An object that supports the <a href="imsrdpclienttransportsettings3.md"><strong>IMsRdpClientTransportSettings3</strong></a> interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-419"><a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>TrustedZoneSite</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-419"><a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>TrustedZoneSite</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-420">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-420">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-421">指定使用者啟動連線的網站是否位於用戶端電腦的 [信任的網站] 清單中。</span><span class="sxs-lookup"><span data-stu-id="786ac-421">Specifies whether the website from which the user launched the connection is in the trusted sites list of the client computer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-422"><a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-422"><a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-423">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-423">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-424">要作為控制項父視窗的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="786ac-424">The window handle to be the parent window for the control.</span></span> <span data-ttu-id="786ac-425">如此一來，控制項所顯示的任何視窗都能針對父應用程式所顯示的任何視窗適當地進行模式回應。</span><span class="sxs-lookup"><span data-stu-id="786ac-425">This allows any windows displayed by the control to be properly modal with respect to any windows displayed by the parent application.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-426"><a href="imsrdpclientnonscriptable5-usemultimon.md"><strong>UseMultimon</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-426"><a href="imsrdpclientnonscriptable5-usemultimon.md"><strong>UseMultimon</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-427">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-427">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-428">指定遠端桌面 ActiveX 控制項是否應該使用多個監視器。</span><span class="sxs-lookup"><span data-stu-id="786ac-428">Specifies whether the Remote Desktop ActiveX control should use multiple monitors.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-429"><a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>UseRedirectionServerName</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-429"><a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>UseRedirectionServerName</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-430">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-430">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-431">是否要使用重新導向伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="786ac-431">Whether to use the redirection server name.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-432"><a href="imstscax-username.md"><strong>使用者</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-432"><a href="imstscax-username.md"><strong>UserName</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-433">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-433">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-434">使用者名稱登入認證。</span><span class="sxs-lookup"><span data-stu-id="786ac-434">The user name logon credential.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-435"><a href="imstscax-version.md"><strong>版本</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-435"><a href="imstscax-version.md"><strong>Version</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-436">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-436">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-437">目前控制項的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="786ac-437">The version number of the current control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-438"><a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-438"><a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-439">唯讀</span><span class="sxs-lookup"><span data-stu-id="786ac-439">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-440">指出控制項是否顯示垂直捲動條。</span><span class="sxs-lookup"><span data-stu-id="786ac-440">Indicates whether the control displays a vertical scroll bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-441"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-441"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-442">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-442">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-443">指定在啟動會話之前，安全性警告對話方塊是否應包含關於剪貼簿重新導向的警告。</span><span class="sxs-lookup"><span data-stu-id="786ac-443">Specifies whether the security warning dialog box should include a warning about clipboard redirection before starting a session.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-444"><a href="imsrdpclientnonscriptable5-warnaboutdirectxredirection.md"><strong>WarnAboutDirectXRedirection</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-444"><a href="imsrdpclientnonscriptable5-warnaboutdirectxredirection.md"><strong>WarnAboutDirectXRedirection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-445">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-445">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-446">不會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="786ac-446">This property is not used.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="786ac-447"><a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>WarnAboutPrinterRedirection</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-447"><a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>WarnAboutPrinterRedirection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-448">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-448">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-449">指定在啟動會話之前，重新導向對話方塊是否顯示印表機重新導向的相關訊息。</span><span class="sxs-lookup"><span data-stu-id="786ac-449">Specifies whether the redirection dialog box displays a message about printer redirection before starting a session.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="786ac-450"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a></span><span class="sxs-lookup"><span data-stu-id="786ac-450"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-451">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="786ac-451">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="786ac-452">指定在啟動會話之前，安全性警告是否應包含有關將認證傳送至遠端伺服器的警告。</span><span class="sxs-lookup"><span data-stu-id="786ac-452">Specifies whether the security warning should include a warning about sending credentials to the remote server before starting a session.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="786ac-453">規格需求</span><span class="sxs-lookup"><span data-stu-id="786ac-453">Requirements</span></span>



| <span data-ttu-id="786ac-454">需求</span><span class="sxs-lookup"><span data-stu-id="786ac-454">Requirement</span></span> | <span data-ttu-id="786ac-455">值</span><span class="sxs-lookup"><span data-stu-id="786ac-455">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="786ac-456">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="786ac-456">Minimum supported client</span></span><br/> | <span data-ttu-id="786ac-457">Windows 8</span><span class="sxs-lookup"><span data-stu-id="786ac-457">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="786ac-458">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="786ac-458">Minimum supported server</span></span><br/> | <span data-ttu-id="786ac-459">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="786ac-459">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="786ac-460">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="786ac-460">Type library</span></span><br/>             | <dl> <span data-ttu-id="786ac-461"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="786ac-461"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="786ac-462">DLL</span><span class="sxs-lookup"><span data-stu-id="786ac-462">DLL</span></span><br/>                      | <dl> <span data-ttu-id="786ac-463"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="786ac-463"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="786ac-464">CLSID</span><span class="sxs-lookup"><span data-stu-id="786ac-464">CLSID</span></span><br/>                    | <span data-ttu-id="786ac-465">CLSID \_ MsRdpClient8 定義為5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="786ac-465">CLSID\_MsRdpClient8 is defined as 5F681803-2900-4C43-A1CC-CF405404A676</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="786ac-466">另請參閱</span><span class="sxs-lookup"><span data-stu-id="786ac-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="786ac-467">遠端桌面 ActiveX 控制項類別</span><span class="sxs-lookup"><span data-stu-id="786ac-467">Remote Desktop ActiveX control classes</span></span>](remote-desktop-activex-control-classes.md)
</dt> </dl>

