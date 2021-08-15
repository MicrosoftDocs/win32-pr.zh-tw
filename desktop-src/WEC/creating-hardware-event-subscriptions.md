---
title: 建立硬體事件訂閱
description: 在已安裝「基礎板管理控制器」 (BMC) 的電腦上，系統事件記錄檔會引發硬體事件並記錄在系統事件記錄檔 (SEL) ，也就是儲存在非動態記憶體的 BMC 事件存放區。
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ee32d590143ed8a1ffacec6f59ad3b3094c2d2a22d0df66b0cb0d3521f83e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751110"
---
# <a name="creating-hardware-event-subscriptions"></a>建立硬體事件訂閱

在已安裝「基礎板管理控制器」 (BMC) 的電腦上，系統事件記錄檔會引發硬體事件並記錄在系統事件記錄檔 (SEL) ，也就是儲存在非動態記憶體的 BMC 事件存放區。 若要使用事件檢視器在 Windows Server 2008 上讀取這些硬體事件，您必須建立事件的訂用帳戶。 硬體事件訂用帳戶只會在 Windows Server 2008 上運作。

下列程式定義如何建立 SEL 事件訂用帳戶來取出硬體事件：

1.  將下列 XML 儲存在 .xml 檔案中 (在此範例中，檔案的名稱 Wsmanselrg.xml) 。 此 XML 會定義訂用帳戶。

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  在命令提示字元視窗中執行下列命令，以建立事件訂用帳戶 (Wecutil.exe 程式位於% SYSTEMROOT% \\ System32 目錄中。 ) ：

    **>Wecutil cs** *<path> \\wsmanselrg.xml*

3.  在命令提示字元視窗中執行下列命令，以確定訂用帳戶為使用中狀態：

    **>Wecutil gr** *wsmanselrg*

BMC 是在本機與伺服器連接的微控制器。 Bmc 的感應器會監視伺服器的實體狀態，以及可透過網路通訊的個別網路連線（即使伺服器已離線）。 您可以透過智慧型平臺管理介面 (IPMI) WMI 提供者來存取 BMC 資料。 如需有關 IPMI 提供者的詳細資訊，請參閱 [Ipmi 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)。

電腦必須安裝 BMC 和 IPMI 提供者，才能讓事件訂用帳戶運作。 針對 Windows Server 2008 上執行的電腦，預設會安裝 IPMI 提供者。 如果無法使用 BMC，則無法安裝 IPMI 驅動程式，且訂用帳戶執行時間狀態一律會顯示錯誤 (0x8004001-WMI 一般失敗) 。

 

 