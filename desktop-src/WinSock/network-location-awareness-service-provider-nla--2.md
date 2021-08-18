---
description: 執行 Microsoft Windows 的個人電腦通常有許多網路連線，例如多個網路介面卡 (NIC) 連接到不同的網路，或是實體網路連線與撥號連線。
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: '網路定位知悉服務供應商 (NLA) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7378aff6f51f2785671f1d424a4721f9cd77fad22d60554746f9427d7f24f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132091"
---
# <a name="network-location-awareness-service-provider-nla"></a>網路定位知悉服務供應商 (NLA) 

執行 Microsoft Windows 的個人電腦通常有許多網路連線，例如多個網路介面卡 (NIC) 連接到不同的網路，或是實體網路連線與撥號連線。 Windows通訊端已有能力列舉可用的網路介面一段時間，但先前無法使用一些有關網路連線的重要資訊。 這包括 Windows 電腦所連接的邏輯網路，或多個介面是否連線到相同網路等資訊。

網路定位知悉服務供應商（通常稱為 NLA）可讓 Windows 通訊端2應用程式識別 Windows 電腦附加的邏輯網路。 此外，NLA 還可讓 Windows 通訊端應用程式識別指定應用程式儲存特定資訊的實體網路介面。 NLA 會實作為泛型 Windows 通訊端2名稱解析服務提供者。

 

 



