---
title: 非同步搜尋
description: 裝置搜尋工具物件可啟用同步和非同步搜尋。 非同步搜尋會立即將控制權交還給呼叫的應用程式。
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57377eb8ae5a49fc9bafe81f90b9ee7c602ae4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932491"
---
# <a name="asynchronous-searching"></a>非同步搜尋

裝置搜尋工具物件可啟用同步和非同步搜尋。 非同步搜尋會立即將控制權交還給呼叫的應用程式。 然後，應用程式會使用應用程式已註冊的回呼介面，在找到每個個別裝置時收到通知。

非同步搜尋最適合用於圖形使用者介面，以及執行連續監視的應用程式。

非同步搜尋的一般結構如下：

1.  建立搜尋物件
2.  開始搜尋
3.  接收回呼通知並採取適當的處理步驟。
4.  當不再需要搜尋時，請取消搜尋並釋放相關聯的物件。

> [!Note]  
> 在回呼程式碼中，應用程式無法釋出接收通知的物件，例如新的裝置，也無法取消搜尋。

 

## <a name="c-example"></a>C + + 範例

C + + 應用程式必須執行回呼物件以傳遞至搜尋。 請參閱 [c + + 中的非同步搜尋](searching-asynchronously-in-c-.md) ，以取得說明此動作的範例程式碼。

## <a name="vbscript-example"></a>VBScript 範例

VBScript 程式碼必須通過回呼函式的位址。


```VB
Sub DeviceFinderCallback (device, UDN, calltype)

  select case calltype
    Case 0
      output = "Found: " & vbCrLf
      output = output & "DisplayName: " & device.FriendlyName & vbCrLf
      output = output & "Type: " & device.Type & vbCrLf
      output = output & "UDN: " & device.UniqueDeviceName & vbCrLf
      MsgBox output

    Case 1
      MsgBox "device removed: " & UDN

    Case 2
      MsgBox "search complete"

    end select
End Sub

Dim devicefinder
Dim findData

Set devicefinder = CreateObject("UPnP.UPnPDeviceFinder")

Sub StartFind()
  findData = devicefinder.CreateAsyncFind("upnp:rootdevice", 0, _
   GetRef("DeviceFinderCallback"))

  devicefinder.StartAsyncFind(findData)
End Sub

Sub StopFind()
  deviceFinder.CancelAsyncFind(findData)
End Sub
```



 

 




