---
description: SWbemRefresher 物件是容器物件，可重新整理所有新增至該物件之物件的資料。 新增的物件集合，SWbemRefreshableItem 實例所代表的每個專案都可以被視為集合和列舉。
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: 'SWbemRefresher 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945673"
---
# <a name="swbemrefresher-object"></a>SWbemRefresher 物件

**SWbemRefresher** 物件是一個容器物件，可重新整理所有新增至該物件之物件的資料。 可以在容器中新增或移除單一實例和實例枚舉器。 新增的物件集合、 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 實例所代表的每個專案都可以被視為集合和列舉。 來自任何類別的 WMI 實例都可以加入至 **SWbemRefresher** 物件。 即使實例資料的提供者不是高效能的提供者，重新整理程式物件仍可以更新重新 [**整理呼叫上的資料**](swbemrefresher-refresh.md) 。 如果資料是透過高效能提供者所提供，而且 [**AutoReconnect**](swbemrefresher-autoreconnect.md) 屬性為 **TRUE**，則 **SWbemRefresher** 物件會嘗試重新建立與資料提供者的連接中斷。 這個物件可以由 VBScript **CreateObject** 呼叫建立。

您可以呼叫 [**SWbemRefresher**](swbemrefresher-refresh.md)或 [**SWbemObjectEx \_**](swbemobjectex-refresh-.md)方法來執行重新整理作業。

## <a name="members"></a>成員

**SWbemRefresher** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemRefresher** 物件有這些方法。



| 方法                                        | 描述                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**添加**](swbemrefresher-add.md)             | 將新的可重新整理物件加入至重新整理器物件中的集合。<br/>                   |
| [**AddEnum**](swbemrefresher-addenum.md)     | 將新的枚舉器加入至複習物件。<br/>                                             |
| [**DeleteAll**](swbemrefresher-deleteall.md) | 從複習物件中的集合移除所有專案。<br/>                             |
| [**項目**](swbemrefresher-item.md)           | 從集合傳回指定的複習專案。<br/>                                    |
| [**重新整理**](swbemrefresher-refresh.md)     | 更新複習物件中包含的所有專案。<br/>                          |
| [**移除**](swbemrefresher-remove.md)       | 從複習中移除重新整理者專案物件或具有指定索引的物件集。<br/> |



 

### <a name="properties"></a>屬性

**SWbemRefresher** 物件具有這些屬性。



| 屬性                                                         | 存取類型          | Description                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**AutoReconnect**](swbemrefresher-autoreconnect.md)<br/> | 唯讀<br/> | 指出如果連接中斷，重新整理程式是否會自動重新連接至遠端提供者。<br/> |
| [**計數**](swbemrefresher-count.md)<br/>                 | 唯讀<br/> | 包含複習物件中的專案數。<br/>                                                      |



 

## <a name="examples"></a>範例

下列範例說明如何建立 **SWbemRefresher** 物件，並使用 [**Add**](swbemrefresher-add.md) 和 [**AddEnum**](swbemrefresher-addenum.md) 方法來儲存單一實例和列舉實例、重新整理資料，以及使用 Item 屬性來取得 [**SWbemRefreshableItem**](swbemrefreshableitem.md) 物件。


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




