---
title: 執行執行個體提供者主要介面
description: 執行個體提供者會使用 IWbemServices 的非同步方法做為 WMI 的主要介面。
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971502"
---
# <a name="implementing-an-instance-provider-primary-interface"></a>執行執行個體提供者主要介面

執行個體提供者會使用 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 的非同步方法做為 WMI 的主要介面。 藉由只執行滿足您執行個體提供者需求的方法，您可以減少您花費在撰寫程式碼的資源數量。 不過，藉由針對其他類型的提供者來執行保留的方法，您可以減少您撰寫的提供者數目。

由於應用程式和提供者也會使用它來要求 WMI 的服務，因此， [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 包含許多與執行個體提供者無關的方法。 下表列出可為執行個體提供者執行的 **IWbemServices** 方法。



| 方法                                                                   | 功能          |
|--------------------------------------------------------------------------|------------------|
| [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | 重建        |
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | 修改     |
| [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | 刪除         |
| [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | 列舉型別      |
| [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | 查詢處理 |



 

針對您未使用的方法，您的提供者可以提供可傳回無法使用 **WBEM \_ E \_ 提供 \_ 者 \_** 的存根執行。 這包括上表未列出的所有 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 方法。

單一提供者可以透過適當的方式註冊和執行所有相關的方法，以同時作為類別、實例和方法提供者。 如需詳細資訊，請參閱 [撰寫類別提供者](writing-a-class-provider.md) 和 [撰寫方法提供者](writing-a-method-provider.md)。

 

 



