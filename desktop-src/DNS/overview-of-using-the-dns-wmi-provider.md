---
title: 使用 DNS WMI 提供者的總覽
description: 下列一般步驟可讓您開始建立自己的腳本或使用 DNS WMI 提供者的程式。
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9eaa50e4ed1a237ed5b42abd4375ab301a2106498e929e42993cd634ca9ba18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077028"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a>使用 DNS WMI 提供者的總覽

下列一般步驟可讓您開始建立自己的腳本或使用 DNS WMI 提供者的程式。

**使用 DNS WMI 提供者建立腳本或程式**

1.  連線至 DNS WMI 提供者。
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > DNS WMI 提供者的命名空間一律會是 "root \\ microsoftdns"。

     

2.  取得 DNS 伺服器實例。
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  根據您想要執行的型別動作，取得 DNS 區域或記錄實例。
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  執行想要的動作：
    -   執行方法
    -   顯示內容
    -   修改屬性 (必須有讀取/寫入存取權) 

 

 




