---
description: 此範例程式碼來自 ( ICE08) 的 ICE 自訂動作。 ICE 會驗證元件資料表中的每個元件都有唯一的 GUID。 如果元件資料表不存在，則不會進行驗證。
ms.assetid: 785c3fd6-7120-4532-b055-b73a9a44f75d
title: VBScript 中的範例 ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a21ce87547923cca67b115f1f5c9ea93c4cfac6676924e9ad88e7f1d2b332d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996308"
---
# <a name="sample-ice-in-vbscript"></a>VBScript 中的範例 ICE

此範例程式碼來自 ( [ICE08](ice08.md)) 的 ICE 自訂動作。 ICE 會驗證 [元件資料表](component-table.md) 中的每個元件都有唯一的 [GUID](guid.md)。 如果元件資料表不存在，則不會進行驗證。


```VB
Function ICE08()

'Give creation data
Set recInfo=Installer.CreateRecord(1)
recInfo.StringData(0)="ICE08" & Chr(9) & "3" 
    & Chr(9) & "Created 05/21/98 by <insert 
    author's name here>"
Message &h03000000, recInfo

'Give last modification date
recInfo.StringData(0)="ICE08" & Chr(9) & "3" 
    & Chr(9) & "Modified 05/21/98 by <insert 
    author's name here>"
Message &h03000000, recInfo

'Give description of test
recInfo.StringData(0)="ICE08" & Chr(9) & "3" 
    & Chr(9) & "Checks for duplicate GUIDs 
    in Component table"
Message &h03000000, recInfo

'Is there a Component table in the database?
iStat = Database.TablePersistent("Component")
If 1 <> iStat Then
recInfo.StringData(0)="ICE08" & Chr(9) & "2" 
    & Chr(9) & "Table: 'Component' missing. 
    ICE08 cannot continue its validation." 
    & Chr(9) & "https://mypage2"
Message &h03000000, recInfo
ICE08 = 1
Exit Function
End If

'process component table
Set view=Database.OpenView("SELECT 
    `Component`,`ComponentId` FROM 
    `Component` ORDER BY `ComponentId`")
view.Execute
Do
Set rec=view.Fetch
If rec Is Nothing Then Exit Do

'compare for duplicate 
If lastGuid=rec.StringData(2) Then
rec.StringData(0)="ICE08" & Chr(9) 
    & "1" & Chr(9) & "Component: [1] 
    has a duplicate GUID: [2]" & Chr(9) 
    & "https://mypage2" & Chr(9) & 
    "Component" & Chr(9) & "ComponentId" & Chr(9) & "[1]"
Message &h03000000,rec
End If

'set for next compare
lastGuid=rec.StringData(2)
Loop

'Return iesSuccess 
ICE08 = 1

End Function
```



 

 



