---
title: IRemoteDesktopClientEvents 方法
description: IRemoteDesktopClientEvents 介面會公開下列方法。
ms.assetid: D8035924-736D-495D-BF78-950DAEB69774
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe59ebb3eb2fb077b53074024100c4f0861cf197
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315499"
---
# <a name="iremotedesktopclientevents-methods"></a><span data-ttu-id="fdbfd-103">IRemoteDesktopClientEvents 方法</span><span class="sxs-lookup"><span data-stu-id="fdbfd-103">IRemoteDesktopClientEvents methods</span></span>

<span data-ttu-id="fdbfd-104">[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-104">The [**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fdbfd-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="fdbfd-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="fdbfd-106">**OnConnecting 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-106">**OnConnecting method**</span></span>](iremotedesktopclientevents-onconnecting.md)
</dt> <dd>

<span data-ttu-id="fdbfd-107">當用戶端控制項嘗試建立遠端會話的連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-107">Called when the client control attempts to establish a connection to a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-108">**OnConnected 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-108">**OnConnected method**</span></span>](iremotedesktopclientevents-onconnected.md)
</dt> <dd>

<span data-ttu-id="fdbfd-109">當用戶端控制項已連線到遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-109">Called when the client control has connected to a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-110">**OnLoginCompleted 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-110">**OnLoginCompleted method**</span></span>](iremotedesktopclientevents-onlogincompleted.md)
</dt> <dd>

<span data-ttu-id="fdbfd-111">當用戶端控制項成功登入遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-111">Called when the client control has successfully logged on to a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-112">**OnDisconnected 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-112">**OnDisconnected method**</span></span>](iremotedesktopclientevents-ondisconnected.md)
</dt> <dd>

<span data-ttu-id="fdbfd-113">當用戶端控制項與遠端會話中斷連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-113">Called when the client control has been disconnected from a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-114">**OnStatusChanged 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-114">**OnStatusChanged method**</span></span>](iremotedesktopclientevents-onstatuschanged.md)
</dt> <dd>

<span data-ttu-id="fdbfd-115">當用戶端控制項更新其狀態時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-115">Called when the client control has updated its status.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-116">**OnAutoReconnecting 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-116">**OnAutoReconnecting method**</span></span>](iremotedesktopclientevents-onautoreconnecting.md)
</dt> <dd>

<span data-ttu-id="fdbfd-117">當用戶端控制項嘗試自動重新建立遠端會話的連接時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-117">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-118">**OnAutoReconnected 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-118">**OnAutoReconnected method**</span></span>](iremotedesktopclientevents-onautoreconnected.md)
</dt> <dd>

<span data-ttu-id="fdbfd-119">當用戶端控制項自動重新連接到遠端會話時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-119">Called when the client control has automatically reconnected to a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-120">**OnDialogDisplaying 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-120">**OnDialogDisplaying method**</span></span>](iremotedesktopclientevents-ondialogdisplaying.md)
</dt> <dd>

<span data-ttu-id="fdbfd-121">在控制項顯示對話方塊之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-121">Called before the control displays a dialog box.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-122">**OnDialogDismissed 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-122">**OnDialogDismissed method**</span></span>](iremotedesktopclientevents-ondialogdismissed.md)
</dt> <dd>

<span data-ttu-id="fdbfd-123">在用戶端控制項顯示的對話方塊關閉之後呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-123">Called after a dialog box displayed by the client control is dismissed.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-124">**OnNetworkStatusChanged 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-124">**OnNetworkStatusChanged method**</span></span>](iremotedesktopclientevents-onnetworkstatuschanged.md)
</dt> <dd>

<span data-ttu-id="fdbfd-125">在網路狀態變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-125">Called when the network status has changed.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-126">**OnAdminMessageReceived 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-126">**OnAdminMessageReceived method**</span></span>](iremotedesktopclientevents-onadminmessagereceived.md)
</dt> <dd>

<span data-ttu-id="fdbfd-127">當用戶端控制項收到系統管理訊息時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-127">Called when the client control receives an administrative message.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-128">**OnKeyCombinationPressed 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-128">**OnKeyCombinationPressed method**</span></span>](iremotedesktopclientevents-onkeycombinationpressed.md)
</dt> <dd>

<span data-ttu-id="fdbfd-129">在遠端會話中按下特殊按鍵組合時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-129">Called when special key combinations are pressed in the remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-130">**OnRemoteDesktopSizeChanged 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-130">**OnRemoteDesktopSizeChanged method**</span></span>](iremotedesktopclientevents-onremotedesktopsizechanged.md)
</dt> <dd>

<span data-ttu-id="fdbfd-131">當遠端桌面大小變更時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-131">Called when the remote desktop size has changed.</span></span>

</dd> <dt>

[<span data-ttu-id="fdbfd-132">**OnTouchPointerCursorMoved 方法**</span><span class="sxs-lookup"><span data-stu-id="fdbfd-132">**OnTouchPointerCursorMoved method**</span></span>](iremotedesktopclientevents-ontouchpointercursormoved.md)
</dt> <dd>

<span data-ttu-id="fdbfd-133">當觸控指標游標已移動，且 [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) 屬性設定為 true 時呼叫。</span><span class="sxs-lookup"><span data-stu-id="fdbfd-133">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span>

</dd> </dl>

 

 