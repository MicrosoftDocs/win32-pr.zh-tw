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
# <a name="windows-sockets-2-architecture"></a><span data-ttu-id="acfaa-103">Windows 通訊端2架構</span><span class="sxs-lookup"><span data-stu-id="acfaa-103">Windows Sockets 2 Architecture</span></span>

<span data-ttu-id="acfaa-104">Windows 通訊端2架構與 Windows Open System 架構 (WOSA) 相容，如下所示：</span><span class="sxs-lookup"><span data-stu-id="acfaa-104">The Windows Sockets 2 architecture is compliant with the Windows Open System Architecture (WOSA), as illustrated below:</span></span>

![windows 通訊端2架構](images/ovrvw2-1.png)

<span data-ttu-id="acfaa-106">Winsock 會定義應用程式開發介面 (API) 之間的標準服務提供者介面 (SPI) ，以及其從 WS2 \_32.dll 和通訊協定堆疊匯出的函式。</span><span class="sxs-lookup"><span data-stu-id="acfaa-106">Winsock defines a standard service provider interface (SPI) between the application programming interface (API), with its functions exported from WS2\_32.dll and the protocol stacks.</span></span> <span data-ttu-id="acfaa-107">因此，在 Windows 通訊端1.1 的情況下，Winsock 支援不限於 TCP/IP 通訊協定堆疊。</span><span class="sxs-lookup"><span data-stu-id="acfaa-107">Consequently, Winsock support is not limited to TCP/IP protocol stacks as is the case for Windows Sockets 1.1.</span></span>

<span data-ttu-id="acfaa-108">在 Windows 通訊端2架構中，堆疊廠商不需要或不需要提供自己的 WS2 \_32.dll，因為單一 WS2 \_32.dll 必須跨所有堆疊運作。</span><span class="sxs-lookup"><span data-stu-id="acfaa-108">With the Windows Sockets 2 architecture, it is not necessary or desirable, for stack vendors to supply their own implementation of WS2\_32.dll, since a single WS2\_32.dll must work across all stacks.</span></span> <span data-ttu-id="acfaa-109">WS2 \_32.dll 和相容性填充碼的查看方式應該與作業系統元件相同。</span><span class="sxs-lookup"><span data-stu-id="acfaa-109">The WS2\_32.dll and compatibility shims should be viewed in the same way as an operating system component.</span></span>

 

 



