---
description: 使用 CServiceConfig 設定 COM + 服務
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: 使用 CServiceConfig 設定 COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688703"
---
# <a name="configuring-com-services-with-cserviceconfig"></a>使用 CServiceConfig 設定 COM + 服務

[**CServiceConfig**](cserviceconfig.md)類別是用來設定可在沒有元件的情況下使用的 com + 服務。 它會匯總無限制執行緒封送處理器，讓它可以在不同的單元中使用。 若要設定個別的服務，您必須針對與服務相關聯的介面呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後呼叫該介面上的方法來建立適當的設定。 下表說明透過 **CServiceConfig** 類別所執行的介面。



| 介面                                                                         | 描述                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IServiceInheritanceConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | 類別的預設介面。 它可用來快速初始化許多 COM + 服務。<br/>                                                                                              |
| [**IServiceComTIIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | 用來設定 COM 交易整合器 (COMTI) 內建函式資訊。 COMTI 可讓開發人員將大型主機交易程式與以元件為基礎的應用程式整合。<br/> |
| [**IServiceIISIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | 用來設定 Internet Information Services (IIS) 內建函式的資訊。<br/>                                                                                                             |
| [**IServicePartitionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | 用來設定如何搭配服務使用 COM + 分割。<br/>                                                                                                                             |
| [**IServiceSxSConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | 用來設定並存元件。<br/>                                                                                                                                                    |
| [**IServiceSynchronizationConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | 用來設定 COM + 同步處理服務。<br/>                                                                                                                                              |
| [**IServiceThreadPoolConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | 用來設定 COM + 服務的執行緒集區。 只有在使用 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) 函數時，才能設定執行緒集區。<br/>                          |
| [**IServiceTrackerConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | 用來設定追蹤器屬性。 追蹤器是一種報告機制，可讓監視程式碼監看正在執行的程式碼。<br/>                                                         |
| [**IServiceTransactionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | 用來設定 COM + 交易服務。<br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a>元件服務系統管理工具

不適用。

## <a name="visual-basic"></a>Visual Basic

不適用。

## <a name="cc"></a>C/C++

下列程式碼片段說明如何建立和設定 [**CServiceConfig**](cserviceconfig.md) 物件，以使用 com + 交易。


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[透過 CoCreateActivity 使用 COM + 服務](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[透過 CoEnterServiceDomain 和 CoLeaveServiceDomain 使用 COM + 服務](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

