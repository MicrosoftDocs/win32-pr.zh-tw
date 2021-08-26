---
description: 存取集合的主要目的之一是從集合中移除專案。 您可以呼叫內含方法，從集合中移除專案。 Swbemobjectset 搭配使用或 SWbemMethodSet 無法使用這個方法。
ms.assetid: 4a71029c-9fe1-4348-9f78-daa345728e8d
ms.tgt_platform: multiple
title: 從 WMI 集合移除單一專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50364173aff9f28362878e84d5f3ddb496e430521dc5b1bb92bbc11e7e6b528c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995898"
---
# <a name="removing-a-single-item-from-a-wmi-collection"></a>從 WMI 集合移除單一專案

存取集合的主要目的之一是從集合中移除專案。 您可以呼叫 [**內含**](swbempropertyset-remove.md) 方法，從集合中移除專案。 [**Swbemobjectset 搭配使用**](swbemobjectset.md)或 [**SWbemMethodSet**](swbemmethodset.md)無法使用這個方法。

[**內含**](swbempropertyset.md)、 [**SWbemQualifierSet**](swbemqualifierset.md)和 [**SWbemNamedValueSet**](swbemnamedvalueset.md)中的名稱會移除專案。 不過， [**SWbemRefresher**](swbemrefresher.md) 中的專案會由索引移除，並由代表權限名稱的常數從 [**SWbemPrivilegeSet**](swbemprivilegeset.md) 中移除。

**若要從集合中移除專案**

-   下列程式碼範例示範如何使用 [**內含**](swbempropertyset-remove.md) 方法來移除專案。

    ```VB
    oclass.Properties_.Remove "Prop2"
    ```

    

    下列範例會在根預設命名空間中建立名為 "NewClass" 的新類別 \\ ，並在其中新增三個屬性。 腳本接著會使用前一個範例中的程式碼，刪除第二個屬性。

    ```VB
    ' Obtain an empty class and name it
    Const WBEM_CIMTYPE_STRING = 8
    Set objSWbemService = GetObject("winmgmts:root\default")
    Set objClass = objSWbemService.get()
    Wscript.Echo "Creating class NewClass"
    objClass.Path_.Class = "NewClass"

    ' Add three properties 
    For i = 1 to 3
        objClass.Properties_.Add "Prop" & i, WBEM_CIMTYPE_STRING
    Next
    Getprops()

    ' Remove the Prop2 property
    objClass.Properties_.Remove "Prop2"
    Wscript.Echo "Second property removed "
    Getprops()

    ' Write the changes to the class back
    objClass.Put_

    Sub Getprops()
        Wscript.Echo "Number of Properties = " _
            & objClass.Properties_.Count
        For Each prop in objClass.Properties_
            Wscript.Echo prop.name
        Next
    End Sub
    ```

    

如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)、 [存取集合](accessing-a-collection.md)，以及 [從集合中移除多個專案](removing-multiple-items-from-a-collection.md)。

 

 



