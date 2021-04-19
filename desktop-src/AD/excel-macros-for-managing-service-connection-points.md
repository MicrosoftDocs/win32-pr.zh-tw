---
title: 用於管理服務連接點的 Excel 宏
description: 您可以使用簡單的 Excel 宏來管理服務連接點。
ms.assetid: da8a7363-6814-4c26-b259-53e6f6ba98cd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69bc3561962b063c9128d46934d3cb87b84e0a24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968619"
---
# <a name="excel-macros-for-managing-service-connection-points"></a>用於管理服務連接點的 Excel 宏

您可以使用簡單的 Excel 宏來管理服務連接點。

下列 Excel 宏會顯示建立新服務連接點的最低需求。


```VB
Option Explicit

Private Sub p_CreateExampleSCP()

    Dim oAdSysInfo As ADSystemInfo
    Set oAdSysInfo = CreateObject("ADSystemInfo")
    
    Dim objComputer As ActiveDs.IADsContainer
    Set objComputer = GetObject("LDAP://" + oAdSysInfo.ComputerName)
    
    Dim IADsSCP As ActiveDs.IADs
    Set IADsSCP = objComputer.Create("ServiceConnectionPoint", _
                                "CN=Example SCP")
    
    IADsSCP.PutEx 2, "serviceBindingInformation", _
                    Array( _
                        " - UNC connection to Service", _
                        " - WS-Man connection to service" _
                    )
                    
    IADsSCP.PutEx 2, "Keywords", _
                    Array( _
                        "KW1=A kewyrowd value" _
                    )
                    
    IADsSCP.SetInfo

End Sub
```



下列 Excel 宏顯示如何刪除範例服務連接點。


```VB
Option Explicit

Private Sub p_DeleteExampleScp()
    Dim oAdSysInfo As ADSystemInfo
    Set oAdSysInfo = CreateObject("ADSystemInfo")
    
    Dim objComputer As ActiveDs.IADsContainer
    Set objComputer = GetObject("LDAP://" + oAdSysInfo.ComputerName)

    objComputer.Delete "ServiceConnectionPoint", _
                        "CN=Example SCP"

End Sub
```



 

 




