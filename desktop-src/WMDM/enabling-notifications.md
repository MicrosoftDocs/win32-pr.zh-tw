---
title: 啟用通知
description: 啟用通知
ms.assetid: b4fc7714-a7d0-409f-a47c-4903bab883cc
keywords:
- Windows媒體裝置管理員，通知
- 裝置管理員，通知
- 程式設計指南，通知
- 桌面應用程式，通知
- 建立 Windows 媒體裝置管理員應用程式、通知
- 通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ab1b71482db78571f141b7042d8abc926b0d79ca2f487ee7dc961396993b9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585061"
---
# <a name="enabling-notifications"></a>啟用通知

Windows媒體裝置管理員宣告了四個介面，可讓應用程式在 COM 類別中執行以接收事件通知。 這些介面分為兩個群組，如下表所示。



| 介面                                                                                                                                                | 描述                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)                                                                                                            | 當裝置或存放裝置媒體已連線或中斷連線時，通知應用程式。                                                                                         |
| [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)<br/> [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)<br/> [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)<br/> | 一個非常簡單的通知系統，用來警示應用程式有關任何事件的進度。 應用程式不需要採取任何動作來回應這些訊息。 |



 

**IWMDMNotification**

當隨插即用裝置連線或與電腦中斷連線，以及隨插即用存放裝置媒體 (（例如快閃卡) 從裝置中插入或移除）時， **IWMDMNotification** 會警示應用程式。 這些通知可協助應用程式更新其使用者介面，以反映變更。

若要接收這些通知，您的應用程式必須註冊，才能使用 Platform SDK **IConnectionPointContainer** 和 **IConnectionPoint** 介面接收這些通知。 當您的應用程式啟動時，您的應用程式應該註冊以接收事件，並在關閉時取消註冊。 請依照下列步驟進行註冊，以接收這些通知。

1.  查詢您針對 **IConnectionPointContainer** 驗證應用程式時所收到的主要 **IWMDeviceManager** 介面。
2.  呼叫 **IConnectionPointContainer：： FindConnectionPoint** 來取得 **IWMDMNotification** 介面的容器連接點。
3.  藉由呼叫 **IConnectionPoint：： Advise** 來註冊以接收事件。 傳入用來執行 **IWMDMNotification** 的類別，並取出 cookie （識別您連接點的唯一識別碼）。 這必須儲存，稍後用來取消註冊事件通知。

下列 c + + 程式碼示範如何進行註冊，以接收來自 **IWMDMNotification** 的通知。


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



當您的應用程式關閉時，您必須向 **IConnectionPoint** 取消註冊，以指出它應該不會再傳送通知給您。 遵循下列步驟以取消註冊通知：

1.  查詢主要 **IWMDeviceManager** 介面以進行 **IConnectionPointContainer**。
2.  取得 **IWMDMNotification** 介面的連接點。
3.  藉由呼叫 IConnectionPoint：： Unadvise 來取消註冊您的應用程式，藉由呼叫 **：：**，傳遞您註冊接收事件時所收到的唯一識別碼。

下列 c + + 程式碼示範如何在應用程式關閉時取消註冊 **IWMDMNotification** 事件。


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



**使用 IWMDMProgress**

Windows媒體裝置管理員可在特定動作（例如內容傳輸、安全的時鐘取得，以及遇到 DRM 檔案資訊）時，傳送您的應用程式狀態消息。 您的應用程式可以使用這些訊息來監視事件的狀態，或取消事件。 若要使用這個介面，請執行 [**IWMDMProgress**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress)、 [**IWMDMProgress2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress2)或 [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)，然後將它當作參數傳遞至將接受進度訊息的方法。 請注意， **IWMDMProgress3** 是最上層的介面，因為它會提供指定要追蹤之動作的識別碼 GUID。 下列應用程式方法會接受進度介面 (對應的服務提供者方法應該能夠將通知傳送至已提交的介面) ：

[**IWMDMStorageControl：:D elete**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete)

[**IWMDMStorageControl：： Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert)

[**IWMDMStorageControl：： Move**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move)

[**IWMDMStorageControl：： Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read)

[**IWMDMStorageControl：： Rename**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename)

[**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)

[**IWMDMStorageGlobals：： Initialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-initialize)

[**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md)

這些方法的檔中提供了將介面傳遞至方法的範例。 如需執行回呼介面的範例，請參閱 **IWMDMProgress**、 **IWMDMProgress2** 或 **IWMDMProgress3** 方法的檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows 媒體裝置管理員應用程式**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 





