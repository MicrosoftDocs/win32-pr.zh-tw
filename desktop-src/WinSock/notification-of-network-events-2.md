---
description: 資料傳輸服務提供者最重要的責任之一，就是在發生某些網路事件時，提供用戶端的指示。
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: 網路事件的通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6fb24f746cbb03860bbd28c1028d92d7865a29c44baedaf2c227cb48536cd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794758"
---
# <a name="notification-of-network-events"></a>網路事件的通知

資料傳輸服務提供者最重要的責任之一，就是在發生某些網路事件時，提供用戶端的指示。 定義的網路事件清單包含下列各項：

-   **FD \_連接**-遠端主機或多播會話的連接已完成。
-   **FD \_接受**-遠端主機正在進行連線要求。
-   **FD \_讀取**-網路資料已抵達，可供讀取。
-   **FD \_寫入**：服務提供者的緩衝區中已有空間可供使用，因此現在可能會傳送額外的資料。
-   **FD \_OOB**-頻外資料可供讀取。
-   **FD \_關閉**-遠端主機已關閉連接。
-   **FD \_QOS**-已協商的 qos 層級發生變更。
-   **FD \_將 \_ QOS 分組**（保留）。
-   **FD \_路由 \_ 介面 \_ 變更**：應用來存取 **SIO \_ 路由 \_ 介面 \_ 變更 IOCTL** 中指定之目的地的本機介面已變更。
-   **FD \_位址 \_ 清單 \_ 變更**-應用程式可以系結的本機地址清單已變更。

以上列舉的網路事件集有時稱為 **FD \_ XXX** 事件。 根據用戶端要求通知的方式，可能會有幾種方式指出出現一或多個這類網路事件。

 

 



