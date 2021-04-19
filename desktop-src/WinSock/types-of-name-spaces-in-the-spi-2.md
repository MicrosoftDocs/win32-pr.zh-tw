---
description: Windows 通訊端中的三種命名空間類型 (Winsock) SPI 包含動態、靜態和持續性的命名空間。
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: SPI 中的命名空間類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983806"
---
# <a name="types-of-namespaces-in-the-spi"></a>SPI 中的命名空間類型

有三種不同類型的命名空間，可在其中註冊服務：

-   動態
-   Static
-   持續性

動態命名空間可讓服務即時註冊命名空間，並讓用戶端在執行時間探索可用的服務。 動態命名空間經常依賴廣播來指出網路服務的持續可用性。 動態命名空間的範例包括 NetWare 環境內使用的 SAP 命名空間，以及 AppleTalk 使用的 NBP 命名空間。

靜態命名空間需要預先註冊所有服務，也就是建立命名空間的時候。 DNS 是靜態命名空間的範例。 雖然有程式設計方式來解析名稱，但沒有程式設計方式可註冊名稱。

持續性命名空間可讓服務即時註冊命名空間。 但不同于動態命名空間，持續性命名空間會保留靜態儲存體中的註冊資訊，在此情況下，它會一直保留到服務要求移除時為止。 持續性的命名空間是由目錄服務（例如 X. 500 和 NDS (NetWare 目錄服務) ）所 typified。 這些環境可讓您新增、刪除和修改服務屬性。 此外，代表目錄服務內之服務的服務物件可以有各種與服務相關聯的屬性。 用戶端應用程式最重要的屬性是服務的定址資訊。

 

 



