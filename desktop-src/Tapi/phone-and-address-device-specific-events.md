---
description: 下列程式碼範例說明 address 和 phone 裝置事件的事件處理常式。 每個事件的程式碼會顯示如何建立事件介面，以及如何取得事件資料。
ms.assetid: 236d4e7f-865f-4b26-8da6-c86476588c47
title: 電話和位址裝置特定事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cf4c45eb7c7b933a36814f8eba8cd5cc39d8cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512384"
---
# <a name="phone-and-address-device-specific-events"></a><span data-ttu-id="09cdf-104">電話和位址裝置特定事件</span><span class="sxs-lookup"><span data-stu-id="09cdf-104">Phone and Address Device-specific Events</span></span>

<span data-ttu-id="09cdf-105">下列程式碼範例說明 address 和 phone 裝置事件的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="09cdf-105">The following code example illustrates an event handler for address and phone device events.</span></span> <span data-ttu-id="09cdf-106">每個事件的程式碼會顯示如何建立事件介面，以及如何取得事件資料。</span><span class="sxs-lookup"><span data-stu-id="09cdf-106">The code for each event shows how to create the event interface and how to retrieve the event data.</span></span>

``` syntax
HRESULT STDMETHODCALLTYPE CMyEventNotification::Event(
   TAPI_EVENT TapiEvent,
   IDispatch * pEvent
)
{
    HRESULT hr = S_OK;
    //...
    switch (TapiEvent) 
    {
        case TE_ADDRESSDEVSPECIFIC:
        {
            ITAddressDeviceSpecificEvent* pITADSEvent = NULL;

            hr = pEvent->QueryInterface( 
                               IID_ITAddressDeviceSpecificEvent,
                               (void **)(&pITADSEvent) );
            // If (hr != S_OK) process the error here...

            // Retrieve data received from the TSP.
            long lParam1=0;
            hr = pITADSEvent->get_lParam1(&lParam1);
            // If (hr != S_OK) process the error here...

            long lParam2=0;
            hr = pITADSEvent->get_lParam2(&lParam2);
            // If (hr != S_OK) process the error here...

            long lParam3=0; 
            hr = pITADSEvent->get_lParam3(&lParam3);
            // If (hr !=S_OK) process the error here...

            // Process the data here.
            // ...
            pITADSEvent->Release();
            break;
        }

        case TE_PHONEDEVSPECIFIC:
        {
            ITPhoneDeviceSpecificEvent* pITPhEvent = NULL;

            hr = pEvent->QueryInterface( 
                            IID_ITPhoneDeviceSpecificEvent,
                            (void **)(&pITPhEvent) );
            // If (hr != S_OK) process the error here...

            // Retrieve data received from the TSP.
            long lParam1=0;
            hr = pITPhEvent->get_lParam1(&lParam1);
            // If (hr != S_OK) process the error here...

            long lParam2=0;
            hr = pITPhEvent->get_lParam2(&lParam2);
            // If (hr != S_OK) process the error here...

            long lParam3=0;
            hr = pITPhEvent->get_lParam3(&lParam3);
            // If (hr != S_OK) process the error here...

            // Process the data here.
            //...
            pITPhEvent->Release();
            break;
        }
        //...
    } // end of switch 
    //...
}
```

 

 



