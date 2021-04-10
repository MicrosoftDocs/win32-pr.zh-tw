---
title: IRemoteDesktopClientEvents 介面
description: 提供從伺服器接收用戶端控制項事件相關資訊的方法。
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- IRemoteDesktopClientEvents 介面遠端桌面服務
- IRemoteDesktopClientEvents 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025099"
---
# <a name="iremotedesktopclientevents-interface"></a><span data-ttu-id="68dbc-105">IRemoteDesktopClientEvents 介面</span><span class="sxs-lookup"><span data-stu-id="68dbc-105">IRemoteDesktopClientEvents interface</span></span>

<span data-ttu-id="68dbc-106">提供從伺服器接收用戶端控制項事件相關資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="68dbc-106">Provides methods that receive information from the server that are related to client control events.</span></span> <span data-ttu-id="68dbc-107">事件包括連線和中斷連接、全螢幕模式要求、成功登入，以及錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="68dbc-107">Events include connecting and disconnecting, full-screen mode requests, successful logon, and error conditions.</span></span>

## <a name="members"></a><span data-ttu-id="68dbc-108">成員</span><span class="sxs-lookup"><span data-stu-id="68dbc-108">Members</span></span>

<span data-ttu-id="68dbc-109">**IRemoteDesktopClientEvents** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="68dbc-109">The **IRemoteDesktopClientEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="68dbc-110">**IRemoteDesktopClientEvents** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="68dbc-110">**IRemoteDesktopClientEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="68dbc-111">方法</span><span class="sxs-lookup"><span data-stu-id="68dbc-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="68dbc-112">方法</span><span class="sxs-lookup"><span data-stu-id="68dbc-112">Methods</span></span>

<span data-ttu-id="68dbc-113">**IRemoteDesktopClientEvents** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="68dbc-113">The **IRemoteDesktopClientEvents** interface has these methods.</span></span>



| <span data-ttu-id="68dbc-114">方法</span><span class="sxs-lookup"><span data-stu-id="68dbc-114">Method</span></span>                                                                                      | <span data-ttu-id="68dbc-115">描述</span><span class="sxs-lookup"><span data-stu-id="68dbc-115">Description</span></span>                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68dbc-116">**OnAdminMessageReceived**</span><span class="sxs-lookup"><span data-stu-id="68dbc-116">**OnAdminMessageReceived**</span></span>](iremotedesktopclientevents-onadminmessagereceived.md)         | <span data-ttu-id="68dbc-117">當用戶端控制項收到系統管理訊息時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-117">Called when the client control receives an administrative message.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="68dbc-118">**OnAutoReconnected**</span><span class="sxs-lookup"><span data-stu-id="68dbc-118">**OnAutoReconnected**</span></span>](iremotedesktopclientevents-onautoreconnected.md)                   | <span data-ttu-id="68dbc-119">當用戶端控制項自動重新連接到遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-119">Called when the client control has automatically reconnected to a remote session.</span></span> <br/>                                                                       |
| [<span data-ttu-id="68dbc-120">**OnAutoReconnecting**</span><span class="sxs-lookup"><span data-stu-id="68dbc-120">**OnAutoReconnecting**</span></span>](iremotedesktopclientevents-onautoreconnecting.md)                 | <span data-ttu-id="68dbc-121">當用戶端控制項嘗試自動重新建立遠端會話的連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-121">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span> <br/>                                                  |
| [<span data-ttu-id="68dbc-122">**OnConnected**</span><span class="sxs-lookup"><span data-stu-id="68dbc-122">**OnConnected**</span></span>](iremotedesktopclientevents-onconnected.md)                               | <span data-ttu-id="68dbc-123">當用戶端控制項已連線到遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-123">Called when the client control has connected to a remote session.</span></span><br/>                                                                                        |
| [<span data-ttu-id="68dbc-124">**OnConnecting**</span><span class="sxs-lookup"><span data-stu-id="68dbc-124">**OnConnecting**</span></span>](iremotedesktopclientevents-onconnecting.md)                             | <span data-ttu-id="68dbc-125">當用戶端控制項嘗試建立遠端會話的連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-125">Called when the client control attempts to establish a connection to a remote session.</span></span> <br/>                                                                  |
| [<span data-ttu-id="68dbc-126">**OnDialogDismissed**</span><span class="sxs-lookup"><span data-stu-id="68dbc-126">**OnDialogDismissed**</span></span>](iremotedesktopclientevents-ondialogdismissed.md)                   | <span data-ttu-id="68dbc-127">在用戶端控制項顯示的對話方塊關閉之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-127">Called after a dialog box displayed by the client control is dismissed.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="68dbc-128">**OnDialogDisplaying**</span><span class="sxs-lookup"><span data-stu-id="68dbc-128">**OnDialogDisplaying**</span></span>](iremotedesktopclientevents-ondialogdisplaying.md)                 | <span data-ttu-id="68dbc-129">在控制項顯示對話方塊之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-129">Called before the control displays a dialog box.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="68dbc-130">**OnDisconnected**</span><span class="sxs-lookup"><span data-stu-id="68dbc-130">**OnDisconnected**</span></span>](iremotedesktopclientevents-ondisconnected.md)                         | <span data-ttu-id="68dbc-131">當用戶端控制項與遠端會話中斷連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-131">Called when the client control has been disconnected from a remote session.</span></span> <br/>                                                                             |
| [<span data-ttu-id="68dbc-132">**OnKeyCombinationPressed**</span><span class="sxs-lookup"><span data-stu-id="68dbc-132">**OnKeyCombinationPressed**</span></span>](iremotedesktopclientevents-onkeycombinationpressed.md)       | <span data-ttu-id="68dbc-133">在遠端會話中按下特殊按鍵組合時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-133">Called when special key combinations are pressed in the remote session.</span></span> <br/>                                                                                 |
| [<span data-ttu-id="68dbc-134">**OnLoginCompleted**</span><span class="sxs-lookup"><span data-stu-id="68dbc-134">**OnLoginCompleted**</span></span>](iremotedesktopclientevents-onlogincompleted.md)                     | <span data-ttu-id="68dbc-135">當用戶端控制項成功登入遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-135">Called when the client control has successfully logged on to a remote session.</span></span> <br/>                                                                          |
| [<span data-ttu-id="68dbc-136">**OnNetworkStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="68dbc-136">**OnNetworkStatusChanged**</span></span>](iremotedesktopclientevents-onnetworkstatuschanged.md)         | <span data-ttu-id="68dbc-137">在網路狀態變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-137">Called when the network status has changed.</span></span> <br/>                                                                                                             |
| [<span data-ttu-id="68dbc-138">**OnRemoteDesktopSizeChanged**</span><span class="sxs-lookup"><span data-stu-id="68dbc-138">**OnRemoteDesktopSizeChanged**</span></span>](iremotedesktopclientevents-onremotedesktopsizechanged.md) | <span data-ttu-id="68dbc-139">當遠端桌面大小變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-139">Called when the remote desktop size has changed.</span></span> <br/>                                                                                                        |
| [<span data-ttu-id="68dbc-140">**OnStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="68dbc-140">**OnStatusChanged**</span></span>](iremotedesktopclientevents-onstatuschanged.md)                       | <span data-ttu-id="68dbc-141">當用戶端控制項更新其狀態時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-141">Called when the client control has updated its status.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="68dbc-142">**OnTouchPointerCursorMoved**</span><span class="sxs-lookup"><span data-stu-id="68dbc-142">**OnTouchPointerCursorMoved**</span></span>](iremotedesktopclientevents-ontouchpointercursormoved.md)   | <span data-ttu-id="68dbc-143">當觸控指標游標已移動，且 [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) 屬性設定為 true 時呼叫。</span><span class="sxs-lookup"><span data-stu-id="68dbc-143">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="68dbc-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="68dbc-144">Requirements</span></span>



| <span data-ttu-id="68dbc-145">需求</span><span class="sxs-lookup"><span data-stu-id="68dbc-145">Requirement</span></span> | <span data-ttu-id="68dbc-146">值</span><span class="sxs-lookup"><span data-stu-id="68dbc-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68dbc-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68dbc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="68dbc-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="68dbc-148">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="68dbc-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68dbc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="68dbc-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68dbc-150">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="68dbc-151">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="68dbc-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="68dbc-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68dbc-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="68dbc-153">DLL</span><span class="sxs-lookup"><span data-stu-id="68dbc-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68dbc-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68dbc-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="68dbc-155">CLSID</span><span class="sxs-lookup"><span data-stu-id="68dbc-155">CLSID</span></span><br/>                    | <span data-ttu-id="68dbc-156">CLSID \_ RemoteDesktopClient 定義為 EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span><span class="sxs-lookup"><span data-stu-id="68dbc-156">CLSID\_RemoteDesktopClient is defined as EAB16C5D-EED1-4E95-868B-0FBA1B42C092</span></span><br/>       |
| <span data-ttu-id="68dbc-157">IID</span><span class="sxs-lookup"><span data-stu-id="68dbc-157">IID</span></span><br/>                      | <span data-ttu-id="68dbc-158">DIID \_ IRemoteDesktopClientEvents 定義為079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="68dbc-158">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68dbc-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68dbc-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68dbc-160">遠端桌面 ActiveX 控制項參考</span><span class="sxs-lookup"><span data-stu-id="68dbc-160">Remote Desktop ActiveX control reference</span></span>](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

