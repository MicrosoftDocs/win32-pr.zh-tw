---
description: 服務品質 (QoS) 是透過 Windows Server 2003、Windows XP 及 Windows 2000 支援的各種 QoS 元件在 Windows 中執行。
ms.assetid: e55b085f-6f72-4aa4-a8b0-b7609b9010dc
title: Windows 通訊端 2 SPI 中的服務品質
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87d37f2e30e0a4fb296fc340353e2f4d85b5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977262"
---
# <a name="quality-of-service-in-the-windows-sockets-2-spi"></a><span data-ttu-id="df455-103">Windows 通訊端 2 SPI 中的服務品質</span><span class="sxs-lookup"><span data-stu-id="df455-103">Quality of Service in the Windows Sockets 2 SPI</span></span>

<span data-ttu-id="df455-104">服務品質 (QoS) 是透過 Windows Server 2003、Windows XP 及 Windows 2000 支援的各種 QoS 元件在 Windows 中執行。</span><span class="sxs-lookup"><span data-stu-id="df455-104">Quality of Service (QoS) is implemented in Windows through various QoS components supported on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="df455-105">QoS 及其元件的詳細說明，位於 Microsoft Windows 軟體開發套件 (SDK) 的服務品質專屬區段中。</span><span class="sxs-lookup"><span data-stu-id="df455-105">A detailed explanation of QoS and its components is located in a section dedicated to Quality of Service, located in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="df455-106">本 QoS 章節將說明每個 QoS 元件，以及它在 QoS 程式中扮演的角色，並提供額外的指導方針，讓您能夠執行具備 QoS 功能的應用程式和服務。</span><span class="sxs-lookup"><span data-stu-id="df455-106">Each QoS component, and the role it plays in the QoS implementation, is explained in this QoS section, with additional guidance provided for the implementation of QoS-enabled applications and services.</span></span> <span data-ttu-id="df455-107">如需詳細資訊，請參閱 Windows SDK 的 [服務品質 (QoS) ](/previous-versions/windows/desktop/qos/qos-start-page) 一節。</span><span class="sxs-lookup"><span data-stu-id="df455-107">Please see the [Quality of Service (QoS)](/previous-versions/windows/desktop/qos/qos-start-page) section of the Windows SDK for more detailed information.</span></span>

<span data-ttu-id="df455-108">本節說明 Winsock 開發人員可用的服務功能品質。</span><span class="sxs-lookup"><span data-stu-id="df455-108">This section describes Quality of Service capabilities available to Winsock developers.</span></span> <span data-ttu-id="df455-109">下列清單說明本節中的主題：</span><span class="sxs-lookup"><span data-stu-id="df455-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="df455-110">使用量模型</span><span class="sxs-lookup"><span data-stu-id="df455-110">Usage Model</span></span>](usage-model-2.md)
-   [<span data-ttu-id="df455-111">QoS 更新</span><span class="sxs-lookup"><span data-stu-id="df455-111">QoS Updates</span></span>](qos-updates-2.md)
-   [<span data-ttu-id="df455-112">SPI 中的預設值</span><span class="sxs-lookup"><span data-stu-id="df455-112">Default Values in the SPI</span></span>](default-values-in-the-spi-2.md)
-   [<span data-ttu-id="df455-113">SPI 中的 QoS 範本</span><span class="sxs-lookup"><span data-stu-id="df455-113">QoS Templates in the SPI</span></span>](qos-templates-in-the-spi-2.md)

## <a name="related-topics"></a><span data-ttu-id="df455-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="df455-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df455-115">服務品質 (QoS)</span><span class="sxs-lookup"><span data-stu-id="df455-115">Quality of Service (QoS)</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> <dt>

<span data-ttu-id="df455-116">[什麼是 QoS？](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="df455-116">[What Is QoS?](/previous-versions/windows/it-pro/windows-server-2003/cc757120(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="df455-117">Winsock ATM QoS 擴充功能</span><span class="sxs-lookup"><span data-stu-id="df455-117">Winsock ATM QoS Extension</span></span>](winsock-atm-qos-extension.md)
</dt> <dt>

[<span data-ttu-id="df455-118">**Winsock IOCTLs**</span><span class="sxs-lookup"><span data-stu-id="df455-118">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
