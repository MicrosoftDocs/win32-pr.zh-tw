---
description: Windows 通訊端 2 (Winsock) 架構符合 Windows 開放式系統架構 (WOSA) 的規範。
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Windows通訊端2架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ad3dd29f692df94e1f66c13c00c75eeca36fb04d18c5f2e95e67b91773698f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569150"
---
# <a name="windows-sockets-2-architecture"></a>Windows通訊端2架構

Windows 通訊端2架構符合 Windows 開放式系統架構 (WOSA) ，如下所示：

![windows 通訊端2架構](images/ovrvw2-1.png)

Winsock 會定義應用程式開發介面 (API) 之間的標準服務提供者介面 (SPI) ，以及其從 WS2 \_32.dll 和通訊協定堆疊匯出的函式。 因此，在 Windows 通訊端1.1 的情況下，Winsock 支援不限於 tcp/ip 通訊協定堆疊。

在 Windows 通訊端2架構中，堆疊供應商不需要或不想要提供自己的 WS232.dll 實作為 \_ ，因為單一 WS2 \_32.dll 必須跨所有堆疊運作。 WS2 \_32.dll 和相容性填充碼的查看方式應該與作業系統元件相同。

 

 



