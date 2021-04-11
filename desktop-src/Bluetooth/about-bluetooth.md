---
title: 關於藍牙
description: 藍牙是一種業界標準的通訊協定，可讓許多裝置（包括電腦、印表機、行動電話及掌上型裝置）進行無線連線。
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- 藍牙藍牙，說明
- 藍牙藍牙，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023089"
---
# <a name="about-bluetooth"></a><span data-ttu-id="35888-105">關於藍牙</span><span class="sxs-lookup"><span data-stu-id="35888-105">About Bluetooth</span></span>

<span data-ttu-id="35888-106">藍牙是一種業界標準的通訊協定，可讓許多裝置（包括電腦、印表機、行動電話及掌上型裝置）進行無線連線。</span><span class="sxs-lookup"><span data-stu-id="35888-106">Bluetooth is an industry-standard protocol that enables wireless connectivity for a multitude of devices, including computers, printers, mobile phones, and handheld devices.</span></span>

<span data-ttu-id="35888-107">藍牙的主要功能包括：</span><span class="sxs-lookup"><span data-stu-id="35888-107">Key Bluetooth features include:</span></span>

-   <span data-ttu-id="35888-108">低成本、低功率耗用量無線通訊協定，具有業界標準的支援和全球接受。</span><span class="sxs-lookup"><span data-stu-id="35888-108">A low-cost, low-power consumption wireless protocol with industry-standard support and worldwide acceptance.</span></span>
-   <span data-ttu-id="35888-109">一種定義熟悉的程式設計介面，可讓開發人員用來快速開發或移植應用程式。</span><span class="sxs-lookup"><span data-stu-id="35888-109">A defined and familiar programming interface that developers can use to quickly develop or port applications.</span></span>
-   <span data-ttu-id="35888-110">官方網站和業界合作的組織，可解釋、升級及標準化藍牙技術。</span><span class="sxs-lookup"><span data-stu-id="35888-110">An official Web site and an industry-wide cooperative organization that explains, promotes, and standardizes Bluetooth technology.</span></span> <span data-ttu-id="35888-111">如需詳細資訊，請參閱 [www.bluetooth.com](https://www.bluetooth.com/)。</span><span class="sxs-lookup"><span data-stu-id="35888-111">For more information, see [www.bluetooth.com](https://www.bluetooth.com/).</span></span>

<span data-ttu-id="35888-112">Windows 上的藍牙提供的核心服務，與傳輸控制通訊協定所公開的服務 (TCP/IP) 的 TCP 部分。</span><span class="sxs-lookup"><span data-stu-id="35888-112">Bluetooth on Windows provides core services that are similar to those exposed by Transmission Control Protocol (the TCP part of TCP/IP).</span></span> <span data-ttu-id="35888-113">就像許多網路通訊協定和服務一樣，藍牙連線能力和資料傳輸是透過 Windows 通訊端函式呼叫來撰寫，並使用常見的 Windows 通訊端程式設計技術和特定的藍牙延伸模組。</span><span class="sxs-lookup"><span data-stu-id="35888-113">Like many networking protocols and services, Bluetooth connectivity and data transfer are programmed through Windows Sockets function calls, using common Windows Sockets programming techniques and specific Bluetooth extensions.</span></span> <span data-ttu-id="35888-114">不過，由於有線、固定網路和無線臨機網路之間有顯著的差異，因此藍牙提供了像是服務/裝置探索和通知等延伸模組，可讓應用程式在無線環境中正常運作。</span><span class="sxs-lookup"><span data-stu-id="35888-114">However, because significant differences exist between a wired, fixed network and a wireless ad-hoc network, Bluetooth provides extensions such as service/device discovery and notification that enable applications to operate properly in the wireless environment.</span></span> <span data-ttu-id="35888-115">這些延伸模組也 pave 了簡單移植到類似的技術（例如 IrDA 或未來的無線傳輸）的方式。</span><span class="sxs-lookup"><span data-stu-id="35888-115">These extensions also pave the way for simple porting to similar technologies, such as IrDA, or future wireless transports.</span></span>

<span data-ttu-id="35888-116">Microsoft 會在 windows xp Service Pack 1 (SP1) 和更新版本、Windows XP Embedded （含 Service Pack 2）和 Windows CE 上提供藍牙支援。</span><span class="sxs-lookup"><span data-stu-id="35888-116">Microsoft provides support for Bluetooth on Windows XP with Service Pack 1 (SP1) and later, on Windows XP Embedded with Service Pack 2, and on Windows CE.</span></span> <span data-ttu-id="35888-117">在 Windows XP 上執行的藍牙應用程式應該能夠在包含必要相依性的 Windows XP Embedded 執行時間映射上執行。</span><span class="sxs-lookup"><span data-stu-id="35888-117">Bluetooth applications that run on Windows XP should be able to run on a Windows XP Embedded-based run-time image that includes the required dependencies.</span></span> <span data-ttu-id="35888-118">如需 Windows XP Embedded 的詳細資訊，請參閱 MSDN 上的 Windows XP Embedded 說明文件。</span><span class="sxs-lookup"><span data-stu-id="35888-118">For more information about Windows XP Embedded, see the Windows XP Embedded Help documentation on MSDN.</span></span> <span data-ttu-id="35888-119">如需 Windows CE 程式設計的詳細資訊，請參閱 Windows CE SDK。</span><span class="sxs-lookup"><span data-stu-id="35888-119">For more information about Windows CE programming, consult the Windows CE SDK.</span></span>

<span data-ttu-id="35888-120">Microsoft 提供兩種在 Windows 上進行藍牙程式設計的方法：</span><span class="sxs-lookup"><span data-stu-id="35888-120">Microsoft provides two approaches for programming Bluetooth on Windows:</span></span>

-   <span data-ttu-id="35888-121">使用 Windows 通訊端介面</span><span class="sxs-lookup"><span data-stu-id="35888-121">Using the Windows Sockets interface</span></span>
-   <span data-ttu-id="35888-122">使用 nonsocket 藍牙介面直接管理裝置</span><span class="sxs-lookup"><span data-stu-id="35888-122">Managing devices directly by using nonsocket Bluetooth interfaces</span></span>

<span data-ttu-id="35888-123">本節提供下列主題中這兩種方法的總覽資訊。</span><span class="sxs-lookup"><span data-stu-id="35888-123">This section provides overview information about both of these approaches in the following topics.</span></span> <span data-ttu-id="35888-124">如需使用 Windows 通訊端 API 元素來設計藍牙的詳細資訊，請參閱 [使用 Windows 通訊端進行藍牙程式設計](bluetooth-programming-with-windows-sockets.md)。</span><span class="sxs-lookup"><span data-stu-id="35888-124">For more information about using Windows Sockets API elements to program Bluetooth, see [Bluetooth Programming with Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span></span>



| <span data-ttu-id="35888-125">區段</span><span class="sxs-lookup"><span data-stu-id="35888-125">Section</span></span>                                                                                | <span data-ttu-id="35888-126">Content</span><span class="sxs-lookup"><span data-stu-id="35888-126">Content</span></span>                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="35888-127">適用於藍牙的 Windows 通訊端支援</span><span class="sxs-lookup"><span data-stu-id="35888-127">Windows Sockets Support for Bluetooth</span></span>](windows-sockets-support-for-bluetooth.md)     | <span data-ttu-id="35888-128">描述藍牙與 Windows 通訊端之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="35888-128">Describes the relationship between Bluetooth and Windows Sockets.</span></span> |
| [<span data-ttu-id="35888-129">管理藍牙裝置和服務</span><span class="sxs-lookup"><span data-stu-id="35888-129">Managing Bluetooth Devices and Services</span></span>](managing-bluetooth-devices-and-services.md) | <span data-ttu-id="35888-130">說明如何管理藍牙裝置和服務。</span><span class="sxs-lookup"><span data-stu-id="35888-130">Describes how to manage Bluetooth devices and services.</span></span>           |



 

 

 




