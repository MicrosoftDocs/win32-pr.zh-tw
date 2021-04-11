---
description: 分散式應用程式的 SSPI 選項
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: 分散式應用程式的 SSPI 選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847673"
---
# <a name="sspi-options-for-distributed-applications"></a><span data-ttu-id="9842e-103">分散式應用程式的 SSPI 選項</span><span class="sxs-lookup"><span data-stu-id="9842e-103">SSPI Options for Distributed Applications</span></span>

<span data-ttu-id="9842e-104">開發人員有許多選項可建立分散式應用程式。</span><span class="sxs-lookup"><span data-stu-id="9842e-104">Developers have many options for building distributed applications.</span></span> <span data-ttu-id="9842e-105">[*安全性支援提供者介面*](../secgloss/s-gly.md) (SSPI) 在應用層級通訊協定和 [*安全性通訊協定*](../secgloss/s-gly.md)之間提供抽象層。</span><span class="sxs-lookup"><span data-stu-id="9842e-105">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) provides an abstraction layer between application-level protocols and [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="9842e-106">應用程式可以透過數種方式來利用 SSPI 安全性通訊協定：</span><span class="sxs-lookup"><span data-stu-id="9842e-106">Applications can take advantage of the SSPI security protocols in several ways:</span></span>

-   <span data-ttu-id="9842e-107">針對傳統的通訊端型應用程式) 直接呼叫 SSPI 常式 (。</span><span class="sxs-lookup"><span data-stu-id="9842e-107">Call SSPI routines directly (for traditional, socket-based applications).</span></span>

    <span data-ttu-id="9842e-108">常式會使用要求/回應訊息來執行 [*應用程式協定，此通訊協定*](../secgloss/a-gly.md) 會攜帶 SSPI 安全性相關資料。</span><span class="sxs-lookup"><span data-stu-id="9842e-108">The routines use request/response messages to implement the [*application protocol*](../secgloss/a-gly.md) that carries SSPI security-related data.</span></span>

-   <span data-ttu-id="9842e-109">使用 COM 來呼叫在較低層級使用已驗證的 RPC 和 SSPI 所執行的安全性選項。</span><span class="sxs-lookup"><span data-stu-id="9842e-109">Use COM to call security options that are implemented by using authenticated RPC and SSPI at lower levels.</span></span>

    <span data-ttu-id="9842e-110">這些應用程式不會直接呼叫 SSPI 函數。</span><span class="sxs-lookup"><span data-stu-id="9842e-110">These applications do not call SSPI functions directly.</span></span>

-   <span data-ttu-id="9842e-111">使用 [Windows 通訊端 2](../winsock/windows-sockets-start-page-2.md) (WinSock) 搭配擴充的 WinSock 介面，以允許傳輸提供者使用安全性功能。</span><span class="sxs-lookup"><span data-stu-id="9842e-111">Use [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) with the extended WinSock interface to allow transport providers to use security features.</span></span>

    <span data-ttu-id="9842e-112">這種方法會將 [*安全性支援提供者*](../secgloss/s-gly.md) (SSP) 整合到網路堆疊中，並透過通用介面提供安全性與傳輸服務。</span><span class="sxs-lookup"><span data-stu-id="9842e-112">This approach integrates the [*security support provider*](../secgloss/s-gly.md) (SSP) into the network stack and provides both security and transport services through a common interface.</span></span>

-   <span data-ttu-id="9842e-113">使用 [Windows 網際網路延伸模組 API](../wininet/portal.md) (WinInet) 以及設計來支援網際網路安全性通訊協定（例如 [*安全通訊端層*](../secgloss/s-gly.md) (SSL) 通訊協定）的介面。</span><span class="sxs-lookup"><span data-stu-id="9842e-113">Use the [Windows Internet Extensions API](../wininet/portal.md) (WinInet) and an interface designed to support Internet security protocols such as the [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL) protocol.</span></span>

    <span data-ttu-id="9842e-114">應用程式會將 SSPI 介面用於 [安全通道](secure-channel.md) (Schannel) 安全性提供者來實行 WinInet 安全性。</span><span class="sxs-lookup"><span data-stu-id="9842e-114">Applications use the SSPI interface to the [Secure Channel](secure-channel.md) (Schannel) security provider to implement WinInet security.</span></span> <span data-ttu-id="9842e-115">Schannel 是 Microsoft 的 SSL 執行。</span><span class="sxs-lookup"><span data-stu-id="9842e-115">Schannel is the Microsoft implementation of SSL.</span></span>

<span data-ttu-id="9842e-116">數個 SSPI 函式會傳回代表各種物件存留期的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="9842e-116">Several SSPI functions return time stamps that represent the life span of various objects.</span></span> <span data-ttu-id="9842e-117">[*安全性套件*](../secgloss/s-gly.md) 可以維持時間，並以不同的方式提供時間戳記，但使用本地時間可簡化使用 SSPI 函式的應用程式工作。</span><span class="sxs-lookup"><span data-stu-id="9842e-117">[*Security packages*](../secgloss/s-gly.md) can maintain time and provide time stamps in different ways, but using local time simplifies the work of applications that use SSPI functions.</span></span>

 

 
