---
description: CoCreateActivity 函式是用來將 batch 工作提交至 COM + 系統。 它允許以腳本為基礎的應用程式支援整個應用程式的 COM + 服務設定。
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: 透過 CoCreateActivity 使用 COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b5452c99fa431e7c1927646eec7ad9b5e5fa930f3ba7d0bf242df7690325db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128660"
---
# <a name="using-com-services-through-cocreateactivity"></a>透過 CoCreateActivity 使用 COM + 服務

[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)函式是用來將 batch 工作提交至 com + 系統。 它允許以腳本為基礎的應用程式支援整個應用程式的 COM + 服務設定。

所需的 COM + 服務是透過傳遞給函式的 [**CServiceConfig**](cserviceconfig.md) 物件來設定。 函數會建立活動物件，並傳回該物件的 [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) 介面。 您可以分別使用 **IServiceActivity** 的 [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall)或 [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall)方法，以同步或非同步方式提交批次工作。 [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall)介面的指標會傳遞至這些方法的每一個，而批次工作則是由開發人員在 **IServiceCall** 介面的 [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall)方法中執行。

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

不適用。

## <a name="visual-basic"></a>Visual Basic

不適用。

## <a name="cc"></a>C/C++

下列程式碼片段說明如何透過 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)使用 com + 服務。 為求簡單明瞭，會忽略錯誤處理。 此程式碼片段會使用在 [使用 CServiceConfig 設定 COM + 服務](configuring-com--services-with-cserviceconfig.md)時所建立和設定的 [**CServiceConfig**](cserviceconfig.md)物件。


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[使用 CServiceConfig 設定 COM + 服務](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[透過 CoEnterServiceDomain 和 CoLeaveServiceDomain 使用 COM + 服務](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



