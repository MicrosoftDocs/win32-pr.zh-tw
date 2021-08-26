---
description: 有兩種方式可以實作為類別提供者：將介面實作為推入提供者，或做為提取提供者。
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: 執行類別提供者的主要介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3ef1b31e1228b832e4d23945f3af0c4df223ddd3edebdd1ec6e34e0e0e8d449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030438"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a>執行類別提供者的主要介面

有兩種方式可以實作為類別提供者：將介面實作為推入提供者，或做為提取提供者。

本主題將討論下列各節：

-   [執行推播類別提供者的主要介面](#implementing-the-primary-interface-for-a-push-class-provider)
-   [執行提取類別提供者的主要介面](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a>執行推播類別提供者的主要介面

雖然所有提供者都是將 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) 用於初始化，以及至少一個其他介面作為主要介面，但推送提供者只會執行 **IWbemProviderInit**。

確定您的執行會執行下列工作：

-   抓取適當的類別資料。
-   將資料放在 WMI 存放庫中。
-   刪除過時的資料。

完成初始化程式之後，WMI 會處理屬於推送提供者之類別的所有應用程式要求，而不需要任何進一步的提供者互動。 之後，推送提供者會有效地做為 WMI 的用戶端，而不是提供者。 如需執行 [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)的詳細資訊，請參閱 [初始化提供者](initializing-a-provider.md)。

> [!Note]  
> 呼叫 WMI 以建立、更新或移除推送提供者中的資料時，請將 *lFlags* 參數設定為在所有 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)方法的呼叫中包含 **WBEM \_ 旗標擁有者 \_ \_ 更新** 旗標。

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a>執行提取類別提供者的主要介面

類別提取提供者應該將 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 實作為主要介面。 **IWbemServices** 介面支援資料抓取、資料更新、資料移除、列舉和查詢處理。 不過，因為 **iwbemservices** 也是由應用程式和提供者用來要求 WMI 服務，所以 **iwbemservices** 包含許多與類別提供者無關的方法。 您的執行必須分別透過 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) 和 [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) 方法支援類別抓取和列舉。 下表列出可為類別提供者執行的其他非同步 **IWbemServices** 方法。



| 方法                                                     | 功能      |
|------------------------------------------------------------|--------------|
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | 修改 |
| [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | 刪除     |



 

> [!Note]  
> 由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

您的類別提供者應該提供存根執行，以傳回不支援您的功能集之所有其他 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)方法的 **WBEM \_ E \_ 提供者 \_ \_** 。 具體而言，WMI 不支援類別提供者的查詢處理。 因此，類別提供者必須傳回無法執行 [**IWbemServices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)的 **WBEM \_ E \_ 提供者 \_ \_** 、將其 **QuerySupportLevels** 登錄屬性設為 **Null** 或兩者。

類別提供者所執行的介面非常類似于執行個體提供者和方法提供者的介面。 事實上，單一提供者可以執行所有方法並正確註冊，以作為三種類型的提供者。

 

 



