---
title: RemoteDesktopClient 類別
description: 會執行 Microsoft Windows Store 應用程式的遠端桌面用戶端控制-第1版。
ms.assetid: 0910883A-BD49-4908-8423-1FC280E0FE0C
ms.tgt_platform: multiple
keywords:
- RemoteDesktopClient 類別遠端桌面服務
- RemoteDesktopClient 類別遠端桌面服務，說明
topic_type:
- apiref
api_name:
- RemoteDesktopClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb10b23f52f53e2d89fd5a81449818a8fe374116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934110"
---
# <a name="remotedesktopclient-class"></a><span data-ttu-id="464e7-105">RemoteDesktopClient 類別</span><span class="sxs-lookup"><span data-stu-id="464e7-105">RemoteDesktopClient class</span></span>

<span data-ttu-id="464e7-106">實行 Microsoft Windows Store 應用程式遠端桌面用戶端控制-第1版</span><span class="sxs-lookup"><span data-stu-id="464e7-106">Implements the Microsoft Windows Store App Remote Desktop Client Control - version 1</span></span>

<span data-ttu-id="464e7-107">這個類別會執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="464e7-107">This class implements the following interfaces.</span></span>

-   [<span data-ttu-id="464e7-108">**IRemoteDesktopClient**</span><span class="sxs-lookup"><span data-stu-id="464e7-108">**IRemoteDesktopClient**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
-   [<span data-ttu-id="464e7-109">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="464e7-109">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)

<span data-ttu-id="464e7-110">**RemoteDesktopClient** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="464e7-110">**RemoteDesktopClient** has these types of members:</span></span>

-   [<span data-ttu-id="464e7-111">方法</span><span class="sxs-lookup"><span data-stu-id="464e7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="464e7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="464e7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="464e7-113">方法</span><span class="sxs-lookup"><span data-stu-id="464e7-113">Methods</span></span>

<span data-ttu-id="464e7-114">**RemoteDesktopClient** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="464e7-114">The **RemoteDesktopClient** class has these methods.</span></span>



| <span data-ttu-id="464e7-115">方法</span><span class="sxs-lookup"><span data-stu-id="464e7-115">Method</span></span>                                                                                      | <span data-ttu-id="464e7-116">描述</span><span class="sxs-lookup"><span data-stu-id="464e7-116">Description</span></span>                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="464e7-117">**attachEvent**</span><span class="sxs-lookup"><span data-stu-id="464e7-117">**attachEvent**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)                                     | <span data-ttu-id="464e7-118">將事件處理常式附加至事件。</span><span class="sxs-lookup"><span data-stu-id="464e7-118">Attaches an event handler to an event.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="464e7-119">**連接**</span><span class="sxs-lookup"><span data-stu-id="464e7-119">**Connect**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)                                             | <span data-ttu-id="464e7-120">使用目前在遠端桌面通訊協定 (RDP) 應用程式容器用戶端控制上設定的屬性來起始連線。</span><span class="sxs-lookup"><span data-stu-id="464e7-120">Initiates a connection by using the properties currently set on the Remote Desktop Protocol (RDP) app container client control.</span></span><br/>                         |
| [<span data-ttu-id="464e7-121">**DeleteSavedCredentials**</span><span class="sxs-lookup"><span data-stu-id="464e7-121">**DeleteSavedCredentials**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)               | <span data-ttu-id="464e7-122">刪除指定遠端電腦的已儲存認證。</span><span class="sxs-lookup"><span data-stu-id="464e7-122">Deletes saved credentials for the specified remote computer.</span></span><br/>                                                                                            |
| [<span data-ttu-id="464e7-123">**Vemap.detachevent**</span><span class="sxs-lookup"><span data-stu-id="464e7-123">**detachEvent**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)                                     | <span data-ttu-id="464e7-124">從事件卸離事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="464e7-124">Detaches an event handler from an event.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="464e7-125">**中斷連線**</span><span class="sxs-lookup"><span data-stu-id="464e7-125">**Disconnect**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)                                       | <span data-ttu-id="464e7-126">中斷使用中連接。</span><span class="sxs-lookup"><span data-stu-id="464e7-126">Disconnects the active connection.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="464e7-127">**OnAdminMessageReceived**</span><span class="sxs-lookup"><span data-stu-id="464e7-127">**OnAdminMessageReceived**</span></span>](iremotedesktopclientevents-onadminmessagereceived.md)         | <span data-ttu-id="464e7-128">當用戶端控制項收到系統管理訊息時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-128">Called when the client control receives an administrative message.</span></span><br/>                                                                                      |
| [<span data-ttu-id="464e7-129">**OnAutoReconnected**</span><span class="sxs-lookup"><span data-stu-id="464e7-129">**OnAutoReconnected**</span></span>](iremotedesktopclientevents-onautoreconnected.md)                   | <span data-ttu-id="464e7-130">當用戶端控制項自動重新連接到遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-130">Called when the client control has automatically reconnected to a remote session.</span></span><br/>                                                                       |
| [<span data-ttu-id="464e7-131">**OnAutoReconnecting**</span><span class="sxs-lookup"><span data-stu-id="464e7-131">**OnAutoReconnecting**</span></span>](iremotedesktopclientevents-onautoreconnecting.md)                 | <span data-ttu-id="464e7-132">當用戶端控制項嘗試自動重新建立遠端會話的連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-132">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span><br/>                                                  |
| [<span data-ttu-id="464e7-133">**OnConnected**</span><span class="sxs-lookup"><span data-stu-id="464e7-133">**OnConnected**</span></span>](iremotedesktopclientevents-onconnected.md)                               | <span data-ttu-id="464e7-134">當用戶端控制項已連線到遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-134">Called when the client control has connected to a remote session.</span></span><br/>                                                                                       |
| [<span data-ttu-id="464e7-135">**OnConnecting**</span><span class="sxs-lookup"><span data-stu-id="464e7-135">**OnConnecting**</span></span>](iremotedesktopclientevents-onconnecting.md)                             | <span data-ttu-id="464e7-136">當用戶端控制項嘗試建立遠端會話的連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-136">Called when the client control attempts to establish a connection to a remote session.</span></span><br/>                                                                  |
| [<span data-ttu-id="464e7-137">**OnDialogDismissed**</span><span class="sxs-lookup"><span data-stu-id="464e7-137">**OnDialogDismissed**</span></span>](iremotedesktopclientevents-ondialogdismissed.md)                   | <span data-ttu-id="464e7-138">在用戶端控制項顯示的對話方塊關閉之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-138">Called after a dialog box displayed by the client control is dismissed.</span></span><br/>                                                                                 |
| [<span data-ttu-id="464e7-139">**OnDialogDisplaying**</span><span class="sxs-lookup"><span data-stu-id="464e7-139">**OnDialogDisplaying**</span></span>](iremotedesktopclientevents-ondialogdisplaying.md)                 | <span data-ttu-id="464e7-140">在控制項顯示對話方塊之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-140">Called before the control displays a dialog box.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="464e7-141">**OnDisconnected**</span><span class="sxs-lookup"><span data-stu-id="464e7-141">**OnDisconnected**</span></span>](iremotedesktopclientevents-ondisconnected.md)                         | <span data-ttu-id="464e7-142">當用戶端控制項與遠端會話中斷連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-142">Called when the client control has been disconnected from a remote session.</span></span><br/>                                                                             |
| [<span data-ttu-id="464e7-143">**OnKeyCombinationPressed**</span><span class="sxs-lookup"><span data-stu-id="464e7-143">**OnKeyCombinationPressed**</span></span>](iremotedesktopclientevents-onkeycombinationpressed.md)       | <span data-ttu-id="464e7-144">在遠端會話中按下特殊按鍵組合時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-144">Called when special key combinations are pressed in the remote session.</span></span><br/>                                                                                 |
| [<span data-ttu-id="464e7-145">**OnLoginCompleted**</span><span class="sxs-lookup"><span data-stu-id="464e7-145">**OnLoginCompleted**</span></span>](iremotedesktopclientevents-onlogincompleted.md)                     | <span data-ttu-id="464e7-146">當用戶端控制項成功登入遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-146">Called when the client control has successfully logged on to a remote session.</span></span><br/>                                                                          |
| [<span data-ttu-id="464e7-147">**OnNetworkStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="464e7-147">**OnNetworkStatusChanged**</span></span>](iremotedesktopclientevents-onnetworkstatuschanged.md)         | <span data-ttu-id="464e7-148">在網路狀態變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-148">Called when the network status has changed.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="464e7-149">**OnRemoteDesktopSizeChanged**</span><span class="sxs-lookup"><span data-stu-id="464e7-149">**OnRemoteDesktopSizeChanged**</span></span>](iremotedesktopclientevents-onremotedesktopsizechanged.md) | <span data-ttu-id="464e7-150">當遠端桌面大小變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-150">Called when the remote desktop size has changed.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="464e7-151">**OnStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="464e7-151">**OnStatusChanged**</span></span>](iremotedesktopclientevents-onstatuschanged.md)                       | <span data-ttu-id="464e7-152">當用戶端控制項更新其狀態時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-152">Called when the client control has updated its status.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="464e7-153">**OnTouchPointerCursorMoved**</span><span class="sxs-lookup"><span data-stu-id="464e7-153">**OnTouchPointerCursorMoved**</span></span>](iremotedesktopclientevents-ontouchpointercursormoved.md)   | <span data-ttu-id="464e7-154">當觸控指標游標已移動，且 [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) 屬性設定為 true 時呼叫。</span><span class="sxs-lookup"><span data-stu-id="464e7-154">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span><br/> |
| [<span data-ttu-id="464e7-155">**重新連接**</span><span class="sxs-lookup"><span data-stu-id="464e7-155">**Reconnect**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)                                         | <span data-ttu-id="464e7-156">起始自動重新連線遠端桌面通訊協定 (RDP) 應用程式容器用戶端控制項，以將會話納入新的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="464e7-156">Initiates an automatic reconnection of the Remote Desktop Protocol (RDP) app container client control to fit the session to the new width and height.</span></span><br/>   |
| [<span data-ttu-id="464e7-157">**UpdateSessionDisplaySettings**</span><span class="sxs-lookup"><span data-stu-id="464e7-157">**UpdateSessionDisplaySettings**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)   | <span data-ttu-id="464e7-158">更新遠端桌面通訊協定 (RDP) 應用程式容器用戶端控制的寬度和高度設定。</span><span class="sxs-lookup"><span data-stu-id="464e7-158">Updates the width and height settings for the Remote Desktop Protocol (RDP) app container client control.</span></span><br/>                                               |



 

### <a name="properties"></a><span data-ttu-id="464e7-159">屬性</span><span class="sxs-lookup"><span data-stu-id="464e7-159">Properties</span></span>

<span data-ttu-id="464e7-160">**RemoteDesktopClient** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="464e7-160">The **RemoteDesktopClient** class has these properties.</span></span>



| <span data-ttu-id="464e7-161">屬性</span><span class="sxs-lookup"><span data-stu-id="464e7-161">Property</span></span>                                                             | <span data-ttu-id="464e7-162">存取類型</span><span class="sxs-lookup"><span data-stu-id="464e7-162">Access type</span></span>          | <span data-ttu-id="464e7-163">Description</span><span class="sxs-lookup"><span data-stu-id="464e7-163">Description</span></span>                                                                                                                                                            |
|:---------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="464e7-164">**行動**</span><span class="sxs-lookup"><span data-stu-id="464e7-164">**Actions**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions)<br/>           | <span data-ttu-id="464e7-165">唯讀</span><span class="sxs-lookup"><span data-stu-id="464e7-165">Read-only</span></span><br/> | <span data-ttu-id="464e7-166">抓取遠端桌面通訊協定 (RDP) 應用程式容器用戶端的動作物件。</span><span class="sxs-lookup"><span data-stu-id="464e7-166">Retrieves the actions object for the Remote Desktop Protocol (RDP) app container client.</span></span><br/>                                                                    |
| [<span data-ttu-id="464e7-167">**設定**</span><span class="sxs-lookup"><span data-stu-id="464e7-167">**Settings**</span></span>](iremotedesktopclient-settings.md)<br/>         | <span data-ttu-id="464e7-168">唯讀</span><span class="sxs-lookup"><span data-stu-id="464e7-168">Read-only</span></span><br/> | <span data-ttu-id="464e7-169">抓取遠端桌面通訊協定 (RDP) 應用程式容器用戶端的設定物件。</span><span class="sxs-lookup"><span data-stu-id="464e7-169">Retrieves the settings object for the Remote Desktop Protocol (RDP) app container client.</span></span><br/>                                                                   |
| [<span data-ttu-id="464e7-170">**TouchPointer**</span><span class="sxs-lookup"><span data-stu-id="464e7-170">**TouchPointer**</span></span>](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer)<br/> | <span data-ttu-id="464e7-171">唯讀</span><span class="sxs-lookup"><span data-stu-id="464e7-171">Read-only</span></span><br/> | <span data-ttu-id="464e7-172">包含遠端桌面通訊協定 (RDP) 應用程式容器用戶端的 [**RemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) 物件。</span><span class="sxs-lookup"><span data-stu-id="464e7-172">Contains the [**RemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) object for the Remote Desktop Protocol (RDP) app container client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="464e7-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="464e7-173">Requirements</span></span>



| <span data-ttu-id="464e7-174">需求</span><span class="sxs-lookup"><span data-stu-id="464e7-174">Requirement</span></span> | <span data-ttu-id="464e7-175">值</span><span class="sxs-lookup"><span data-stu-id="464e7-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="464e7-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="464e7-176">Minimum supported client</span></span><br/> | <span data-ttu-id="464e7-177">Windows 8</span><span class="sxs-lookup"><span data-stu-id="464e7-177">Windows 8</span></span><br/>                                                                     |
| <span data-ttu-id="464e7-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="464e7-178">Minimum supported server</span></span><br/> | <span data-ttu-id="464e7-179">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="464e7-179">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="464e7-180">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="464e7-180">Type library</span></span><br/>             | <dl> <span data-ttu-id="464e7-181"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="464e7-181"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="464e7-182">DLL</span><span class="sxs-lookup"><span data-stu-id="464e7-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="464e7-183"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="464e7-183"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="464e7-184">CLSID</span><span class="sxs-lookup"><span data-stu-id="464e7-184">CLSID</span></span><br/>                    | <span data-ttu-id="464e7-185">CLSID \_ RemoteDesktopClient 定義為 EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span><span class="sxs-lookup"><span data-stu-id="464e7-185">CLSID\_RemoteDesktopClient is defined as EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="464e7-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="464e7-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="464e7-187">遠端桌面 ActiveX 控制項類別</span><span class="sxs-lookup"><span data-stu-id="464e7-187">Remote Desktop ActiveX control classes</span></span>](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

