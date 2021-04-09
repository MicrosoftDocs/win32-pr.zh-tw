---
description: 透過 CoEnterServiceDomain 和 CoLeaveServiceDomain 使用 COM + 服務
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: 透過 CoEnterServiceDomain 和 CoLeaveServiceDomain 使用 COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111017"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a>透過 CoEnterServiceDomain 和 CoLeaveServiceDomain 使用 COM + 服務

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) 和 [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) 會一起用來圍繞在自己的內容中執行的程式碼區域，而且可以使用 com + 服務，而不需要 com + 元件。 此內容中使用的 COM + 服務是透過傳遞給 **CoEnterServiceDomain** 的 [**CServiceConfig**](cserviceconfig.md)物件來設定。 **CoEnterServiceDomain** 和 **CoLeaveServiceDomain** 所包圍的程式碼，其行為就如同在此內容中建立的物件上呼叫的方法一樣。

腳本應用程式可以使用這組函式來提供 COM + 服務的執行時間支援，而不需要元件。 例如，您可以開發腳本應用程式，以提供允許腳本寫入器在腳本中輸入及保留服務網域的標記。 當腳本引擎處理腳本並遇到標記時，可以使用預先設定的 [**CServiceConfig**](cserviceconfig.md)物件來呼叫 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) 、執行必要的程式碼，然後呼叫 [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)。

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

不適用。

## <a name="visual-basic"></a>Visual Basic

不適用。

## <a name="cc"></a>C/C++

下列程式碼片段說明如何在呼叫 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) 和 [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)之間使用 com + 服務。 為求簡單明瞭，會忽略錯誤處理。 此程式碼片段會使用在 [使用 CServiceConfig 設定 COM + 服務](configuring-com--services-with-cserviceconfig.md)時所建立和設定的 [**CServiceConfig**](cserviceconfig.md)物件。


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[使用 CServiceConfig 設定 COM + 服務](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[透過 CoCreateActivity 使用 COM + 服務](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



