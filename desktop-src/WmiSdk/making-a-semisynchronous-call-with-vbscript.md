---
description: 提供半同步存取功能，以及進行半同步方法呼叫的程式碼範例。
ms.assetid: 3eae38e8-6a63-45c0-99b0-94e25ddbc5a8
ms.tgt_platform: multiple
title: 使用 VBScript 進行半同步呼叫
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e875a269d2cf1cd4e3b40d5c84d42ffb97dc35a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975196"
---
# <a name="making-a-semisynchronous-call-with-vbscript"></a>使用 VBScript 進行半同步呼叫

某些 WMI 方法可以傳回大型集合，使腳本停止回應。 在腳本中，會使用 [半同步存取] 為預設值，而 Windows Management Instrumentation (WMI) 針對可傳回大型物件集合的呼叫（例如下列 [**SWbemServices**](swbemservices.md)方法）設定 **wbemFlagReturnImmediately** ： [**InstancesOf**](swbemservices-instancesof.md)、 [**SubclassesOf**](swbemservices-subclassesof.md)、 [**ExecQuery**](swbemservices-execquery.md)、 [**AssociatorsOf**](swbemservices-associatorsof.md)和 [**ReferencesTo**](swbemservices-referencesto.md)。

在 *IFlags* 參數中使用 **wbemFlagReturnImmediately** 集的每半使用者存取，也是呼叫的預設值，可以傳回下列 [**SWbemObject**](swbemobject.md)方法的大型物件集： [**\_ 實例**](swbemobject-instances-.md)、子 [**\_ 類別**](swbemobject-subclasses-.md)、 [**associators of \_**](swbemobject-associators-.md)和 [**參考 \_**](swbemobject-references-.md)。

若要在處理大型物件集合時減少 WMI 記憶體資源使用量，請在 *IFlags* 參數中包含 **wbemFlagForwardOnly** 的值。 使用 **wbemFlagForwardOnly** 會導致 WMI 建立順向列舉值，而不允許倒轉集合並再次存取專案。

WMI 會將每個物件的記憶體排除在 **每個** 語句處理物件時。 在取得集合的呼叫上設定 **wbemFlagForwardOnly** 旗標時，您無法呼叫集合的 **Count** 方法。 請注意， *IFlags* 參數預設會針對 [**SWbemServices.ExeCNotificationQuery**](swbemservices-execnotificationquery.md)方法設定 **wbemFlagReturnImmediately** 和 **wbemFlagForwardOnly** 。

下列程式描述如何使用 VBScript 進行半執行呼叫。

**在 VBScript 中進行半同步呼叫**

1.  將 *IFlags* 參數設定為 [wbemFlagReturnImmediately](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)的值。
2.  使用 *iFlags* 值，對 [**SWbemServices.ExeCQuery**](swbemservices-execquery.md)或 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)進行一般同步呼叫。
3.  如果您想要將呼叫所傳回的物件視為集合，請使用 **每個** 列舉語法，例如 VBScript。 傳回每個物件時，會將它視為集合中的下一個專案來處理。
4.  將 **wbemFlagReturnImmediately** 的值與 **wbemFlagForwardOnly** 的值結合，以建立順向列舉值。 這個 OR 運算的十進位值是48。 這些常數定義于 Visual Basic 的 >wbemdisp.tlb .tlb 類型程式庫中。 大部分的指令碼語言都會使用數值或定義常數。 如需詳細資訊，請參閱 [WbemFlagEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)。

下列程式碼範例示範如何進行半執行方法呼叫。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。


```VB
wbemFlagReturnImmediately = 16
wbemFlagForwardOnly = 32
IFlags = wbemFlagReturnImmediately + wbemFlagForwardOnly
WScript.Echo IFlags
Set objWMIService = GetObject("winmgmts:root\cimv2")
' Query for all the Win32_Process objects on the 
'     local computer and use forward-only enumerator
Set colProcesses = objWMIService.ExecQuery("SELECT Name FROM Win32_Process",,IFlags)
' Receive each object as it arrives
For Each objProcess in colProcesses
    WScript.Echo objProcess.Name
Next
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[呼叫方法](calling-a-method.md)
</dt> </dl>

 

 



