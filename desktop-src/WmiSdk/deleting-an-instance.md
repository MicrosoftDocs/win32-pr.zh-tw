---
description: 刪除實例是您可能會在 WMI 中執行的最常見刪除命令。
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: 刪除實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974617"
---
# <a name="deleting-an-instance"></a>刪除實例

刪除實例是您可能會在 WMI 中執行的最常見刪除命令。 就像刪除類別一樣，實際的命令相當簡單。 不過，根據您要刪除的實例類型而定，WMI 會有相當不同的執行方式。 如果實例是靜態的，WMI 就只會從 WMI 儲存機制中刪除實例。 如需從 WMI 儲存機制移除類別和實例的詳細資訊，請參閱 [**pragma deleteclass**](pragma-deleteclass.md) 預處理器命令。

如果實例是動態的，WMI 必須在負責下列類別的提供者上呼叫 [**IWbemServices：:D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) ：

-   擁有實例的類別。
-   擁有實例之類別的每個父類別。
-   擁有實例之類別的每個子類別。

刪除的成功與否取決於原始實例的最上層非抽象類別別。 如果任何最上層非抽象類別別的提供者成功完成刪除，作業就會成功。 如需詳細資訊，請參閱 [**IWbemServices：:D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance)的「備註」一節。

[適用于 WMI 的 COM API](com-api-for-wmi.md)有不同的方法可刪除實例和刪除物件。

下列程式說明如何使用 c + + 來刪除基類或衍生類別的實例。

**使用 c + + 刪除基類或衍生類別的實例**

-   請呼叫 [**iwbemservices：:D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) 或 [**Iwbemservices：:D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) 方法。

    顧名思義， [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) 會以非同步方式刪除實例，而 [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) 會以同步方式刪除實例。 若要使用 **DeleteInstanceAsync**，您也必須執行 [**IWbemObjectSink**](iwbemobjectsink.md) 物件。

> [!Note]  
> 由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)會使用相同的方法來刪除類別物件或實例。

下列程式描述如何使用 VBScript 來刪除基類或衍生類別的實例。

**使用 VBScript 刪除基類或衍生類別的實例**

-   呼叫 [**SWbemObject. Delete \_**](swbemobject-delete-.md)或 [**SWbemObject. DeleteAsync \_**](swbemobject-deleteasync-.md)方法。

    顧名思義， [**Delete \_**](swbemobject-delete-.md)會在 [**DeleteAsync \_**](swbemobject-deleteasync-.md)以非同步方式刪除實例時，以同步方式刪除實例。 如需以非同步方式刪除實例的詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

    下列範例說明如何使用 VBScript 刪除實例。

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> 由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

 

 



