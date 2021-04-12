---
title: 遠端桌面虛擬化介面
description: 遠端桌面虛擬化 API 支援下列介面。
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315739"
---
# <a name="remote-desktop-virtualization-interfaces"></a><span data-ttu-id="036a1-103">遠端桌面虛擬化介面</span><span class="sxs-lookup"><span data-stu-id="036a1-103">Remote Desktop Virtualization Interfaces</span></span>

<span data-ttu-id="036a1-104">遠端桌面虛擬化 API 支援下列介面。</span><span class="sxs-lookup"><span data-stu-id="036a1-104">The Remote Desktop Virtualization API supports the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="036a1-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="036a1-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="036a1-106">**ITsSbBaseNotifySink**</span><span class="sxs-lookup"><span data-stu-id="036a1-106">**ITsSbBaseNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

<span data-ttu-id="036a1-107">公開向遠端桌面連線代理人 (RD 連線代理人) 報告狀態和錯誤訊息的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-107">Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-108">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="036a1-108">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

<span data-ttu-id="036a1-109">公開方法和屬性，這些方法和屬性會儲存來自遠端桌面連線 (RDC) 用戶端的連入連線要求的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="036a1-109">Exposes methods and properties that store state information about an incoming connection request from a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-110">**ITsSbClientConnectionPropertySet**</span><span class="sxs-lookup"><span data-stu-id="036a1-110">**ITsSbClientConnectionPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

<span data-ttu-id="036a1-111">可以用來適當地定義用戶端連接的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="036a1-111">Can be used to define custom properties of a client connection as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-112">**ITsSbEnvironment**</span><span class="sxs-lookup"><span data-stu-id="036a1-112">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

<span data-ttu-id="036a1-113">公開方法和屬性，其中包含裝載目的電腦之環境的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="036a1-113">Exposes methods and properties that contain information about the environment that hosts the target computer.</span></span> <span data-ttu-id="036a1-114">此介面可用來儲存裝載虛擬機器之實體伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="036a1-114">This interface can be used to store information about a physical server that hosts virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-115">**ITsSbEnvironmentPropertySet**</span><span class="sxs-lookup"><span data-stu-id="036a1-115">**ITsSbEnvironmentPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

<span data-ttu-id="036a1-116">可以用來定義適當的裝載目的電腦之環境的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="036a1-116">Can be used to define custom properties of an environment that hosts target computers as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-117">**ITsSbFilterPluginStore**</span><span class="sxs-lookup"><span data-stu-id="036a1-117">**ITsSbFilterPluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

<span data-ttu-id="036a1-118">篩選外掛程式存放區</span><span class="sxs-lookup"><span data-stu-id="036a1-118">Filter Plugin Store</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-119">**ITsSbGenericNotifySink**</span><span class="sxs-lookup"><span data-stu-id="036a1-119">**ITsSbGenericNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

<span data-ttu-id="036a1-120">公開向 RD 連線代理人報告完成並取得等候時間的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-120">Exposes methods that reports completion to and gets wait time from the RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-121">**ITsSbGlobalStore**</span><span class="sxs-lookup"><span data-stu-id="036a1-121">**ITsSbGlobalStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

<span data-ttu-id="036a1-122">公開查詢已新增至 RD 連線代理人存放區之目的電腦、會話、環境和伺服器陣列的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-122">Exposes methods that query for target computers, sessions, environments, and farms that have been added to the RD Connection Broker store.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-123">**ITsSbLoadBalanceResult**</span><span class="sxs-lookup"><span data-stu-id="036a1-123">**ITsSbLoadBalanceResult**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

<span data-ttu-id="036a1-124">公開方法和屬性，這些方法和屬性會儲存負載平衡演算法所傳回的目標名稱。</span><span class="sxs-lookup"><span data-stu-id="036a1-124">Exposes methods and properties that store the target name returned by a load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-125">**ITsSbLoadBalancing**</span><span class="sxs-lookup"><span data-stu-id="036a1-125">**ITsSbLoadBalancing**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

<span data-ttu-id="036a1-126">公開可用來提供自訂負載平衡演算法的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-126">Exposes methods you can use to provide a custom load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-127">**ITsSbLoadBalancingNotifySink**</span><span class="sxs-lookup"><span data-stu-id="036a1-127">**ITsSbLoadBalancingNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

<span data-ttu-id="036a1-128">公開方法，以將負載平衡演算法的結果傳回 RD 連線代理人。</span><span class="sxs-lookup"><span data-stu-id="036a1-128">Exposes methods that return the result of a load-balancing algorithm to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-129">**ITsSbOrchestration**</span><span class="sxs-lookup"><span data-stu-id="036a1-129">**ITsSbOrchestration**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

<span data-ttu-id="036a1-130">公開 RD 連線代理人用來確保在將用戶端重新導向至該目標之前，已備妥目標的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-130">Exposes methods that RD Connection Broker uses to ensure that the target is ready before a client is redirected to it.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-131">**ITsSbOrchestrationNotifySink**</span><span class="sxs-lookup"><span data-stu-id="036a1-131">**ITsSbOrchestrationNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

<span data-ttu-id="036a1-132">公開將 [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) 物件傳回 RD 連線代理人的方法，以成功準備連接的目標。</span><span class="sxs-lookup"><span data-stu-id="036a1-132">Exposes methods that return an [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) object to RD Connection Broker after the target is successfully prepared for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-133">**ITsSbPlacement**</span><span class="sxs-lookup"><span data-stu-id="036a1-133">**ITsSbPlacement**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

<span data-ttu-id="036a1-134">公開可在裝載虛擬機器) 的電腦上準備環境 (的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-134">Exposes methods that prepare the environment (the computer that hosts the virtual machine).</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-135">**ITsSbPlacementNotifySink**</span><span class="sxs-lookup"><span data-stu-id="036a1-135">**ITsSbPlacementNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

<span data-ttu-id="036a1-136">公開方法，以傳回 RD 連線代理人環境的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="036a1-136">Exposes methods that return information about environments to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-137">**ITsSbPlugin**</span><span class="sxs-lookup"><span data-stu-id="036a1-137">**ITsSbPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

<span data-ttu-id="036a1-138">公開初始化和終止外掛程式的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-138">Exposes methods that initialize and terminate plug-ins.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-139">**ITsSbPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="036a1-139">**ITsSbPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

<span data-ttu-id="036a1-140">公開通知 RD 連線代理人有關外掛程式初始化或終止的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-140">Exposes methods that notify RD Connection Broker about initialization or termination of a plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-141">**ITsSbPluginPropertySet**</span><span class="sxs-lookup"><span data-stu-id="036a1-141">**ITsSbPluginPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

<span data-ttu-id="036a1-142">可以用來定義適當的自訂外掛程式屬性。</span><span class="sxs-lookup"><span data-stu-id="036a1-142">Can be used to define custom plug-in properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-143">**ITsSbPropertySet**</span><span class="sxs-lookup"><span data-stu-id="036a1-143">**ITsSbPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

<span data-ttu-id="036a1-144">可以用來定義適當的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="036a1-144">Can be used to define custom properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-145">**ITsSbProvider**</span><span class="sxs-lookup"><span data-stu-id="036a1-145">**ITsSbProvider**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

<span data-ttu-id="036a1-146">公開方法，以建立遠端桌面虛擬化所使用之物件的預設執行。</span><span class="sxs-lookup"><span data-stu-id="036a1-146">Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-147">**ITsSbProvisioning**</span><span class="sxs-lookup"><span data-stu-id="036a1-147">**ITsSbProvisioning**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

<span data-ttu-id="036a1-148">公開建立和維護虛擬機器的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-148">Exposes methods that create and maintain virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-149">**ITsSbProvisioningPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="036a1-149">**ITsSbProvisioningPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

<span data-ttu-id="036a1-150">公開通知 RD 連線代理人有關布建虛擬機器的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-150">Exposes methods that notify RD Connection Broker about the provisioning of virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-151">**ITsSbResourceNotification**</span><span class="sxs-lookup"><span data-stu-id="036a1-151">**ITsSbResourceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

<span data-ttu-id="036a1-152">公開 RD 連線代理人用來通知外掛程式發生在會話、目標和用戶端連線物件中之任何狀態變更的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-152">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-153">**ITsSbResourceNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="036a1-153">**ITsSbResourceNotificationEx**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

<span data-ttu-id="036a1-154">公開 RD 連線代理人用來通知外掛程式發生在會話、目標和用戶端連線物件中之任何狀態變更的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-154">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-155">**ITsSbResourcePlugin**</span><span class="sxs-lookup"><span data-stu-id="036a1-155">**ITsSbResourcePlugin**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

<span data-ttu-id="036a1-156">公開擴充 RD 連線代理人功能的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-156">Exposes methods that extend the capabilities of RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-157">**ITsSbResourcePluginStore**</span><span class="sxs-lookup"><span data-stu-id="036a1-157">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

<span data-ttu-id="036a1-158">公開可讓資源外掛程式儲存物件（例如會話和目標）的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-158">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-159">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="036a1-159">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> <dd>

<span data-ttu-id="036a1-160">公開可讓資源外掛程式儲存物件（例如會話和目標）的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-160">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-161">**ITsSbServiceNotification**</span><span class="sxs-lookup"><span data-stu-id="036a1-161">**ITsSbServiceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

<span data-ttu-id="036a1-162">公開 RD 連線代理人用來通知外掛程式 RD 連線代理人本身發生之狀態變更的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-162">Exposes methods that RD Connection Broker uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-163">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="036a1-163">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

<span data-ttu-id="036a1-164">公開屬性，這些屬性會儲存使用者會話的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="036a1-164">Exposes properties that store information about a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-165">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="036a1-165">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

<span data-ttu-id="036a1-166">公開屬性，這些屬性會儲存目標的設定和狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="036a1-166">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-167">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="036a1-167">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dd>

<span data-ttu-id="036a1-168">公開屬性，這些屬性會儲存目標的設定和狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="036a1-168">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-169">**ITsSbTargetPropertySet**</span><span class="sxs-lookup"><span data-stu-id="036a1-169">**ITsSbTargetPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

<span data-ttu-id="036a1-170">衍生自這個介面，以定義自訂目標屬性集。</span><span class="sxs-lookup"><span data-stu-id="036a1-170">Derive from this interface to define a custom target property set.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-171">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="036a1-171">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

<span data-ttu-id="036a1-172">公開遠端桌面連線代理人用來設定外掛程式佇列的屬性。</span><span class="sxs-lookup"><span data-stu-id="036a1-172">Exposes properties that the Remote Desktop Connection Broker uses to set a plugin’s queue.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-173">**ITsSbTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="036a1-173">**ITsSbTaskPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

<span data-ttu-id="036a1-174">公開更新遠端桌面連線代理人外掛程式工作佇列的方法。</span><span class="sxs-lookup"><span data-stu-id="036a1-174">Exposes methods that update the queue of tasks for Remote Desktop Connection Broker plugins.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-175">**ITsSbTaskPluginNotifySink**</span><span class="sxs-lookup"><span data-stu-id="036a1-175">**ITsSbTaskPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

<span data-ttu-id="036a1-176">公開方法，以報告有關要 RD 連線代理人之工作的狀態和錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="036a1-176">Exposes methods that report status and error messages about tasks to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="036a1-177">**IWTSSBPlugin**</span><span class="sxs-lookup"><span data-stu-id="036a1-177">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

<span data-ttu-id="036a1-178">用來擴充終端機服務會話代理人 (TS 會話代理人) 的功能。</span><span class="sxs-lookup"><span data-stu-id="036a1-178">Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker).</span></span> <span data-ttu-id="036a1-179">當您想要提供可覆寫 TS 會話代理人重新導向邏輯的外掛程式時，請執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="036a1-179">Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.</span></span>

</dd> </dl>

 

 