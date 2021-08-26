---
title: RAS 介面
description: 介面代表可透過 LAN 或 WAN 介面卡連線的網路。
ms.assetid: 26eec1af-43b4-4719-bec9-bc3f9b0341e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef716e0db05fe37a0a7d326fbf5f8da878a0628d1deec9e996fcc49d917cc051
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030138"
---
# <a name="ras-interfaces"></a>RAS 介面

介面代表可透過 LAN 或 WAN 介面卡連線的網路。 每個介面在路由器上都有唯一的識別碼。 作用中的介面有一個介面卡，可提供其所代表網路的連線能力。 非使用中的介面沒有提供連線能力的介面卡，除非系統管理員在介面已經有介面卡之後停用該介面。

將封包路由傳送至由介面表示的網路時，會導致路由器配置該介面的介面卡，並建立與遠端網路的 WAN 連線。 將介面卡配置給介面，稱為「系結」（ *binding*）。

介面是可管理的物件。 每個介面在適當 SNMP MIB 的介面表中會顯示為數據列。