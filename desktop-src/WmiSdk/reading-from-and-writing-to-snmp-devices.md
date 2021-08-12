---
description: 您可以在 WMI SMIR (SNMP 模組資訊存放庫) 中，讀取或寫入其對應的類別實例，以存取 SNMP 裝置。
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: 讀取和寫入 SNMP 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0419a5fc426c183ee1eb89a957a0c2f6a210ecd9b5d4612b6c4deb4e0f775a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554253"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a>讀取和寫入 SNMP 裝置

您可以在 WMI SMIR (SNMP 模組資訊存放庫) 中，讀取或寫入其對應的類別實例，以存取 SNMP 裝置。 當您使用相同類型的多個裝置時，為了提高效率，請將一個 SNMP 裝置類型的 Mib 載入 SMIR 中。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

選取下列其中一個選項，以在與每個 SNMP 裝置通訊之前，先更新實例的內容資訊，以讀取或寫入每一種 SNMP 裝置類型。

-   參考特定裝置時，請使用 DNS 名稱，而非 IP 位址。

    下列範例顯示如何使用特定裝置的 DNS 名稱。

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   建立不同的命名空間，並使用 AgentAddress 實例辨識符號將裝置位址與命名空間物件建立關聯，以便將命名空間永久系結至裝置。 在此情況下，您不需要指定內容物件資訊。
-   從 SNMP 裝置讀取。

    下列範例會在裝置類別上執行 Get 作業。

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   寫入 SNMP 裝置。

    下列範例會在裝置類別上執行設定作業。

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

相互關聯的類別是指當發生列舉時，指定的 SNMP 裝置可支援的類別。 相互關聯會影響從 SMIR 傳回的一組類別。 Noncorrelated 列舉會傳回 SMIR 中所有出現的類別，不論裝置是否支援它們。 如需有關使用 WMI 相互關聯技術的詳細資訊，請參閱 [WMI SNMP 類別相互關聯](wmi-snmp-class-correlation.md)。

 

 



