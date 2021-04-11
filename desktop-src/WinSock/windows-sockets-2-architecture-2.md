---
description: Windows 通訊端 2 (Winsock) 架構符合 Windows Open System 架構 (WOSA) 。
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Windows 通訊端2架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114300"
---
# <a name="windows-sockets-2-architecture"></a>Windows 通訊端2架構

Windows 通訊端2架構與 Windows Open System 架構 (WOSA) 相容，如下所示：

![windows 通訊端2架構](images/ovrvw2-1.png)

Winsock 會定義應用程式開發介面 (API) 之間的標準服務提供者介面 (SPI) ，以及其從 WS2 \_32.dll 和通訊協定堆疊匯出的函式。 因此，在 Windows 通訊端1.1 的情況下，Winsock 支援不限於 TCP/IP 通訊協定堆疊。

在 Windows 通訊端2架構中，堆疊廠商不需要或不需要提供自己的 WS2 \_32.dll，因為單一 WS2 \_32.dll 必須跨所有堆疊運作。 WS2 \_32.dll 和相容性填充碼的查看方式應該與作業系統元件相同。

 

 



