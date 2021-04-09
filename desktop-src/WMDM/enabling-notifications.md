---
title: 啟用通知
description: 啟用通知
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Windows Media 裝置管理員，通知
- 裝置管理員，通知
- 程式設計指南，通知
- 桌面應用程式，通知
- 建立 Windows Media 裝置管理員應用程式，通知
- 通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618356c9d63d20a8b6b14e6c99072074cfc75073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672664"
---
# <a name="enabling-notifications"></a><span data-ttu-id="85736-109">啟用通知</span><span class="sxs-lookup"><span data-stu-id="85736-109">Enabling Notifications</span></span>

<span data-ttu-id="85736-110">Windows Media 裝置管理員宣告了四個介面，可讓應用程式在 COM 類別中執行以接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="85736-110">Windows Media Device Manager declares four interfaces that an application can implement in a COM class to receive event notifications.</span></span> <span data-ttu-id="85736-111">這些介面分為兩個群組，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="85736-111">These interfaces fall into two groups, as shown in the following table.</span></span>



| <span data-ttu-id="85736-112">介面</span><span class="sxs-lookup"><span data-stu-id="85736-112">Interfaces</span></span>                                                                                                                                                | <span data-ttu-id="85736-113">Description</span><span class="sxs-lookup"><span data-stu-id="85736-113">Description</span></span>                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85736-114">**IWMDMNotification**</span><span class="sxs-lookup"><span data-stu-id="85736-114">**IWMDMNotification**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | <span data-ttu-id="85736-115">當裝置或存放裝置媒體已連線或中斷連線時，通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="85736-115">Notifies the application when devices or storage media are connected or disconnected.</span></span>                                                                                         |
| [<span data-ttu-id="85736-116">**IWMDMProgress**</span><span class="sxs-lookup"><span data-stu-id="85736-116">**IWMDMProgress**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [<span data-ttu-id="85736-117">**IWMDMProgress2**</span><span class="sxs-lookup"><span data-stu-id="85736-117">**IWMDMProgress2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [<span data-ttu-id="85736-118">**IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="85736-118">**IWMDMProgress3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | <span data-ttu-id="85736-119">一個非常簡單的通知系統，用來警示應用程式有關任何事件的進度。</span><span class="sxs-lookup"><span data-stu-id="85736-119">A very simple notification system to alert an application about the progress of any event.</span></span> <span data-ttu-id="85736-120">應用程式不需要採取任何動作來回應這些訊息。</span><span class="sxs-lookup"><span data-stu-id="85736-120">The application is not required to take any actions in response to these messages.</span></span> |



 

<span data-ttu-id="85736-121">**IWMDMNotification**</span><span class="sxs-lookup"><span data-stu-id="85736-121">**IWMDMNotification**</span></span>

<span data-ttu-id="85736-122">當隨插即用裝置連線或與電腦中斷連線，以及隨插即用存放裝置媒體 (（例如快閃卡) 從裝置中插入或移除）時， **IWMDMNotification** 會警示應用程式。</span><span class="sxs-lookup"><span data-stu-id="85736-122">**IWMDMNotification** alerts the application when Plug and Play devices are connected or disconnected from the computer, as well as when Plug and Play storage media (such as flash cards) are inserted or removed from the device.</span></span> <span data-ttu-id="85736-123">這些通知可協助應用程式更新其使用者介面，以反映變更。</span><span class="sxs-lookup"><span data-stu-id="85736-123">These notifications can help the application update its user interface to reflect changes.</span></span>

<span data-ttu-id="85736-124">若要接收這些通知，您的應用程式必須註冊，才能使用 Platform SDK **IConnectionPointContainer** 和 **IConnectionPoint** 介面接收這些通知。</span><span class="sxs-lookup"><span data-stu-id="85736-124">In order to receive these notifications, your application must register to receive them using the Platform SDK **IConnectionPointContainer** and **IConnectionPoint** interfaces.</span></span> <span data-ttu-id="85736-125">當您的應用程式啟動時，您的應用程式應該註冊以接收事件，並在關閉時取消註冊。</span><span class="sxs-lookup"><span data-stu-id="85736-125">Your application should register to receive events when it starts up, and unregister when it closes.</span></span> <span data-ttu-id="85736-126">請依照下列步驟進行註冊，以接收這些通知。</span><span class="sxs-lookup"><span data-stu-id="85736-126">Follow these steps to register to receive these notifications.</span></span>

1.  <span data-ttu-id="85736-127">查詢您針對 **IConnectionPointContainer** 驗證應用程式時所收到的主要 **IWMDeviceManager** 介面。</span><span class="sxs-lookup"><span data-stu-id="85736-127">Query the main **IWMDeviceManager** interface you received when you authenticated your application for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="85736-128">呼叫 **IConnectionPointContainer：： FindConnectionPoint** 來取得 **IWMDMNotification** 介面的容器連接點。</span><span class="sxs-lookup"><span data-stu-id="85736-128">Call **IConnectionPointContainer::FindConnectionPoint** to retrieve a container connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="85736-129">藉由呼叫 **IConnectionPoint：： Advise** 來註冊以接收事件。</span><span class="sxs-lookup"><span data-stu-id="85736-129">Register to receive events by calling **IConnectionPoint::Advise**.</span></span> <span data-ttu-id="85736-130">傳入用來執行 **IWMDMNotification** 的類別，並取出 cookie （識別您連接點的唯一識別碼）。</span><span class="sxs-lookup"><span data-stu-id="85736-130">Pass in the class that implements **IWMDMNotification**, and retrieve a cookie, a unique ID that identifies your connection point.</span></span> <span data-ttu-id="85736-131">這必須儲存，稍後用來取消註冊事件通知。</span><span class="sxs-lookup"><span data-stu-id="85736-131">This must be stored, and used later to unregister for event notifications.</span></span>

<span data-ttu-id="85736-132">下列 c + + 程式碼示範如何進行註冊，以接收來自 **IWMDMNotification** 的通知。</span><span class="sxs-lookup"><span data-stu-id="85736-132">The following C++ code demonstrates how you can register to receive notifications from **IWMDMNotification**.</span></span>


```C++
HRESULT CWMDMController::RegisterForNotifications()
{
    HRESULT hr = S_OK;
    CComPtr<IConnectionPointContainer> pConxnPointCont;
    CComPtr<IConnectionPoint> pIConnPoint;

    // Get the IConnectionPointContainer interface from IWMDeviceManager.
    if (SUCCEEDED (hr = m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer, (void**) & pConxnPointCont)))
    {
        // Get a connection point from the container.
        if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
        {
            // Add ourselves as a callback handler for the connection point.
            // If we succeeded, indicate that by storing the connection point ID.
            DWORD dwCookie;
            if (SUCCEEDED (hr = pIConnPoint->Advise((IUnknown*)((IWMDMNotification*)this), &dwCookie)))
            {
                m_dwNotificationCookie = dwCookie;
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="85736-133">當您的應用程式關閉時，您必須向 **IConnectionPoint** 取消註冊，以指出它應該不會再傳送通知給您。</span><span class="sxs-lookup"><span data-stu-id="85736-133">When your application closes, you must unregister with **IConnectionPoint** to indicate that it should no longer send you notifications.</span></span> <span data-ttu-id="85736-134">遵循下列步驟以取消註冊通知：</span><span class="sxs-lookup"><span data-stu-id="85736-134">Follow these steps to unregister for notifications:</span></span>

1.  <span data-ttu-id="85736-135">查詢主要 **IWMDeviceManager** 介面以進行 **IConnectionPointContainer**。</span><span class="sxs-lookup"><span data-stu-id="85736-135">Query the main **IWMDeviceManager** interface for **IConnectionPointContainer**.</span></span>
2.  <span data-ttu-id="85736-136">取得 **IWMDMNotification** 介面的連接點。</span><span class="sxs-lookup"><span data-stu-id="85736-136">Get a connection point for **IWMDMNotification** interfaces.</span></span>
3.  <span data-ttu-id="85736-137">藉由呼叫 IConnectionPoint：： Unadvise 來取消註冊您的應用程式，藉由呼叫 **：：**，傳遞您註冊接收事件時所收到的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="85736-137">Unregister your application for event notifications by calling **IConnectionPoint::Unadvise**, passing in the unique ID received when you registered to receive events.</span></span>

<span data-ttu-id="85736-138">下列 c + + 程式碼示範如何在應用程式關閉時取消註冊 **IWMDMNotification** 事件。</span><span class="sxs-lookup"><span data-stu-id="85736-138">The following C++ code shows how to unregister for **IWMDMNotification** events when your application closes.</span></span>


```C++
HRESULT CWMDMController::UnregisterForNotifications()
{
    HRESULT hr = S_FALSE;

    // On class initialization, we initialized the handle to -1 as a flag 
    // to indicate we had not yet registered for notifications. If registration 
    // never happened, don't bother to unregister.
    if (-1 != m_dwNotificationCookie)
    {
        CComPtr<IConnectionPointContainer> pConxnPointCont;
        CComPtr<IConnectionPoint> pIConnPoint;

        // Get the connection point container from IWMDeviceManager. 
        if (SUCCEEDED (hr = 
           m_IWMDMDeviceMgr->QueryInterface(IID_IConnectionPointContainer,
           (void**) & pConxnPointCont)))
        {
            // Get a connection point from the container.
            if (SUCCEEDED (hr = pConxnPointCont->FindConnectionPoint(IID_IWMDMNotification, &pIConnPoint)))
            {
                // Remove ourselves as a callback from the connection point.
                // If successful, reset the ID to a flag value.
                if (SUCCEEDED (hr = 
                    pIConnPoint->Unadvise(m_dwNotificationCookie)))
                {
                    m_dwNotificationCookie = -1;
                    hr = S_OK;
                }
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="85736-139">**使用 IWMDMProgress**</span><span class="sxs-lookup"><span data-stu-id="85736-139">**Using IWMDMProgress**</span></span>

<span data-ttu-id="85736-140">Windows Media 裝置管理員可在特定動作（例如內容傳輸、安全的時鐘取得，以及遇到 DRM 檔案資訊）時，傳送您的應用程式狀態消息。</span><span class="sxs-lookup"><span data-stu-id="85736-140">Windows Media Device Manager can send your application status messages when specific actions, such as content transfer, secure clock acquisition, and encountering DRM file information, occur.</span></span> <span data-ttu-id="85736-141">您的應用程式可以使用這些訊息來監視事件的狀態，或取消事件。</span><span class="sxs-lookup"><span data-stu-id="85736-141">Your application can use these messages to monitor the status of the event or cancel an event.</span></span> <span data-ttu-id="85736-142">若要使用這個介面，請執行 [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)、 [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)或 [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)，然後將它當作參數傳遞至將接受進度訊息的方法。</span><span class="sxs-lookup"><span data-stu-id="85736-142">To use this interface, implement [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress), [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2), or [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3), and pass it in as a parameter to a method that will accept a progress message.</span></span> <span data-ttu-id="85736-143">請注意， **IWMDMProgress3** 是最上層的介面，因為它會提供指定要追蹤之動作的識別碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="85736-143">Note that **IWMDMProgress3** is the superior interface because it provides an identification GUID that specifies what action is being tracked.</span></span> <span data-ttu-id="85736-144">下列應用程式方法會接受進度介面 (對應的服務提供者方法應該能夠將通知傳送至已提交的介面) ：</span><span class="sxs-lookup"><span data-stu-id="85736-144">The following application methods accept a progress interface (the corresponding service provider methods should be able to send notifications to a submitted interface):</span></span>

[<span data-ttu-id="85736-145">**IWMDMStorageControl：:D elete**</span><span class="sxs-lookup"><span data-stu-id="85736-145">**IWMDMStorageControl::Delete**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[<span data-ttu-id="85736-146">**IWMDMStorageControl：： Insert**</span><span class="sxs-lookup"><span data-stu-id="85736-146">**IWMDMStorageControl::Insert**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[<span data-ttu-id="85736-147">**IWMDMStorageControl：： Move**</span><span class="sxs-lookup"><span data-stu-id="85736-147">**IWMDMStorageControl::Move**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[<span data-ttu-id="85736-148">**IWMDMStorageControl：： Read**</span><span class="sxs-lookup"><span data-stu-id="85736-148">**IWMDMStorageControl::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[<span data-ttu-id="85736-149">**IWMDMStorageControl：： Rename**</span><span class="sxs-lookup"><span data-stu-id="85736-149">**IWMDMStorageControl::Rename**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[<span data-ttu-id="85736-150">**IWMDMStorageControl2::Insert2**</span><span class="sxs-lookup"><span data-stu-id="85736-150">**IWMDMStorageControl2::Insert2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[<span data-ttu-id="85736-151">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="85736-151">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[<span data-ttu-id="85736-152">**IWMDMStorageGlobals：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="85736-152">**IWMDMStorageGlobals::Initialize**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[<span data-ttu-id="85736-153">**IWMDRMDeviceApp::AcquireDeviceData**</span><span class="sxs-lookup"><span data-stu-id="85736-153">**IWMDRMDeviceApp::AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)

<span data-ttu-id="85736-154">這些方法的檔中提供了將介面傳遞至方法的範例。</span><span class="sxs-lookup"><span data-stu-id="85736-154">Examples of passing an interface into a method are given in the documentation for these methods.</span></span> <span data-ttu-id="85736-155">如需執行回呼介面的範例，請參閱 **IWMDMProgress**、 **IWMDMProgress2** 或 **IWMDMProgress3** 方法的檔。</span><span class="sxs-lookup"><span data-stu-id="85736-155">For examples of implementing the callback interfaces, see the documentation for the methods of **IWMDMProgress**, **IWMDMProgress2**, or **IWMDMProgress3**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85736-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="85736-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85736-157">**建立 Windows Media 裝置管理員應用程式**</span><span class="sxs-lookup"><span data-stu-id="85736-157">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





