---
description: 如果您使用適用于 WMI 的腳本 API 來取得或儲存當地語系化的類別資訊，請將地區設定指定為「標記」的一部分。
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: 使用適用于 WMI 的腳本 API 來抓取修改過的類別
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47d01af2515b26ca308a1b258aa40508f227a0c1d0eaa5b2b332c1e7b3200420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130880"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a>使用適用于 WMI 的腳本 API 來抓取修改過的類別

如果您使用適用于 WMI 的腳本 API 來取得或儲存當地語系化的類別資訊，請將地區設定指定為「標記」的一部分。 或者，您可以在 *strLocale* 參數中提供 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md) 方法的地區設定名稱。 讀取或寫入修改過的類別時，表示您想要使用當地語系化的類別定義，方法是指定 [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) 做為您所呼叫之方法的 *iFlags* 參數旗標。 針對 PowerShell，您可以在 [>get-wmiobject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true)上使用 *-locale* 參數來指定地區設定。

下列程式碼範例示範如何使用 WMI 腳本的標記或-locale 參數來取得當地語系化的類別。


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





下列程式碼範例示範如何設定 locale 參數，並使用 [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) 旗標。


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> 由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

下表列出接受 [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) 旗標的方法。



| 同步方法                                                 | 非同步方法                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)   | [**SWbemServices. SubclassesOfAsync**](swbemservices-subclassesofasync.md)   |
| [**SWbemObject 子類別\_**](swbemobject-subclasses-.md)        | [**SWbemObject. SubclassesAsync\_**](swbemobject-subclassesasync-.md)        |
| [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)     | [**SWbemServices. InstancesOfAsync**](swbemservices-instancesofasync.md)     |
| [**SWbemObject 實例\_**](swbemobject-instances-.md)          | [**SWbemObject. InstancesAsync\_**](swbemobject-instancesasync-.md)          |
| [**SWbemServices.ExecQuery**](swbemservices-execquery.md)         | [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)         |
| [**SWbemServices。 Get**](swbemservices-get.md)                     | [**SWbemServices. GetAsync**](swbemservices-getasync.md)                     |
| [**SWbemObject。 Put\_**](swbemobject-put-.md)                      | [**SWbemObject. PutAsync\_**](swbemobject-putasync-.md)                      |
| [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)   | [**SWbemServices. ReferencesToAsync**](swbemservices-referencestoasync.md)   |
| [**SWbemObject 參考\_**](swbemobject-references-.md)        | [**SWbemObject. ReferencesAsync\_**](swbemobject-referencesasync-.md)        |
| [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md) | [**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md) |
| [**SWbemObject. Associators of\_**](swbemobject-associators-.md)      | [**SWbemObject. AssociatorsAsync\_**](swbemobject-associatorsasync-.md)      |



 

 

 
