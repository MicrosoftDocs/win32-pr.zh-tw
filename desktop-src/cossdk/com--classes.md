---
description: 以下是 COM + 類別。
ms.assetid: 236725f6-16a3-4209-a9e3-a127c1d7243a
title: COM + 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626c3dfdae542b602cf27a8d8be5cb69dde5910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111685"
---
# <a name="com-classes"></a>COM + 類別

以下是 COM + 類別。



| 類別                                                            | 描述                                                                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppDomainHelper**](appdomainhelper.md)                       | 將 managed 物件系結至應用程式域，也就是應用程式執行所在的隔離環境。                                                                                                                           |
| [**ClrAssemblyLocator**](clrassemblylocator.md)                 | 使用 .NET Framework common language runtime 中的 managed 程式碼時，捕獲元件的相關資訊。                                                                                                                          |
| [**CServiceConfig**](cserviceconfig.md)                         | 指定和設定在呼叫 [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) 或 [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)時所輸入的服務網域中要使用的服務。                     |
| [**SecurityCallCoNtext**](securitycallcontext.md)               | 提供存取目前呼叫的安全性內容，其中包含物件呼叫端的相關資訊。                                                                                                                           |
| [**SecurityCallers**](securitycallers.md)                       | 提供呼叫端集合中個別呼叫端的相關資訊。 集合代表以目前呼叫結尾的呼叫鏈，而集合中的每個呼叫端都代表一個呼叫端的身分識別。 |
| [**SecurityIdentity**](securityidentity.md)                     | 提供安全性資訊集合的存取，代表呼叫者的身分識別。 使用這個類別，您可以在屬於安全性呼叫內容一部分的呼叫端中找出特定的呼叫端。                 |
| [**SharedProperty**](sharedproperty.md)                         | 設定或抓取共用屬性的值。                                                                                                                                                                                       |
| [**SharedPropertyGroup**](sharedpropertygroup.md)               | 建立並存取共用屬性群組中的共用屬性。                                                                                                                                                                  |
| [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) | 建立共用屬性群組，並取得現有共用屬性群組的存取權。                                                                                                                                                 |
| [**TransactionCoNtext**](transactioncontext.md)                 | 建立可開始交易的泛型交易式物件。                                                                                                                                                                       |
| [**TransactionCoNtextEx**](transactioncontextex.md)             | 建立可開始交易的泛型交易式物件。 藉由呼叫這個類別的方法，您可以在單一交易中撰寫多個 COM 物件的工作，並明確地認可或中止交易。        |



 

 

 



