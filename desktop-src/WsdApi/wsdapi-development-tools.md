---
description: Windows SDK 中包含的 WSDAPI 開發工具 (WSD CodeGen、WSD Debug 主控制項和 WSD Debug 用戶端) 讓開發人員建立及偵測 WSDAPI 用戶端與裝置。
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: WSDAPI 開發工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977824"
---
# <a name="wsdapi-development-tools"></a><span data-ttu-id="21259-103">WSDAPI 開發工具</span><span class="sxs-lookup"><span data-stu-id="21259-103">WSDAPI Development Tools</span></span>

<span data-ttu-id="21259-104">Windows SDK 中包含的 WSDAPI 開發工具 (WSD CodeGen、WSD Debug 主控制項和 WSD Debug 用戶端) 讓開發人員建立及偵測 WSDAPI 用戶端與裝置。</span><span class="sxs-lookup"><span data-stu-id="21259-104">The WSDAPI development tools included in the Windows SDK (WSD CodeGen, WSD Debug Host, and WSD Debug Client) enable developers to create and debug WSDAPI-based clients and devices.</span></span> <span data-ttu-id="21259-105">無法使用這些工具的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="21259-105">The source code for these tools is not available.</span></span> <span data-ttu-id="21259-106">SDK 工具位於下列目錄： <Windows SDK Install Folder> \\ Bin。</span><span class="sxs-lookup"><span data-stu-id="21259-106">SDK tools are located in the following directory: <Windows SDK Install Folder>\\Bin.</span></span>

<span data-ttu-id="21259-107">WSD CodeGen (wsdcodegen.exe) 會將 WSDL 合約轉換成產生的 c + + 程式碼，讓開發人員可以直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="21259-107">WSD CodeGen (wsdcodegen.exe) converts a WSDL contract into generated C++ code, which developers can call directly into.</span></span> <span data-ttu-id="21259-108">它會處理資料序列化和線路標記法，讓開發人員可以專注于設計應用程式。</span><span class="sxs-lookup"><span data-stu-id="21259-108">It handles the data serialization and wire representation so developers can focus on designing applications.</span></span> <span data-ttu-id="21259-109">如需 WSD CodeGen 的詳細資訊，請參閱 [裝置上的 Web 服務程式碼](web-services-for-devices-code-generator.md)產生器。</span><span class="sxs-lookup"><span data-stu-id="21259-109">For more information about WSD CodeGen, see [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="21259-110">這項工具適用于 Microsoft Windows 軟體開發套件 (SDK) 以及 Windows 驅動程式套件 (WDK) 。</span><span class="sxs-lookup"><span data-stu-id="21259-110">This tool is available in the Microsoft Windows Software Development Kit (SDK) and in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="21259-111">WSD Debug Host (wsddebug \_host.exe) 和 WSD Debug 用戶端 (wsddebug \_client.exe) 工具可協助開發人員進行用戶端和主機的調試。</span><span class="sxs-lookup"><span data-stu-id="21259-111">The WSD Debug Host (wsddebug\_host.exe) and WSD Debug Client (wsddebug\_client.exe) tools help developers debug their clients and hosts.</span></span> <span data-ttu-id="21259-112">這些工具可用來驗證和檢查 WS-Discovery 和中繼資料交換流量。</span><span class="sxs-lookup"><span data-stu-id="21259-112">These tools can be used to verify and inspect WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="21259-113">如需 WSD Debug 主控制項和 WSD 偵錯工具用戶端的詳細資訊，請參閱 [調試](debugging-tools.md)程式。</span><span class="sxs-lookup"><span data-stu-id="21259-113">For more information about WSD Debug Host and WSD Debug Client, see [Debugging Tools](debugging-tools.md).</span></span> <span data-ttu-id="21259-114">這些工具僅適用于 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="21259-114">These tools are available only in the Windows SDK.</span></span>

<span data-ttu-id="21259-115">有一個額外的開發工具，名為 [ [WSDAPI 基本互通性工具] (WSDBIT) ](https://msdn.microsoft.com/library/cc264250.aspx)，只會在 WDK 中提供。</span><span class="sxs-lookup"><span data-stu-id="21259-115">There is an additional development tool, named [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), that is available only in the WDK.</span></span> <span data-ttu-id="21259-116">這項工具是用來測試服務方法、訊息傳輸優化機制 (MTOM) 、附件或 WS-事件。</span><span class="sxs-lookup"><span data-stu-id="21259-116">This tool is used for testing service methods, Message Transmission Optimization Mechanism (MTOM), attachments or WS-Eventing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21259-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="21259-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21259-118">Windows 上的 WSD 應用程式開發</span><span class="sxs-lookup"><span data-stu-id="21259-118">WSD Application Development on Windows</span></span>](wsd-application-development-on-windows.md)
</dt> <dt>

[<span data-ttu-id="21259-119">裝置上的 Web 服務程式碼產生器</span><span class="sxs-lookup"><span data-stu-id="21259-119">Web Services on Devices Code Generator</span></span>](web-services-for-devices-code-generator.md)
</dt> <dt>

[<span data-ttu-id="21259-120">WSDAPI 基本互通性工具 (WSDBIT) </span><span class="sxs-lookup"><span data-stu-id="21259-120">WSDAPI Basic Interoperability Tool (WSDBIT)</span></span>](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[<span data-ttu-id="21259-121">調試工具</span><span class="sxs-lookup"><span data-stu-id="21259-121">Debugging Tools</span></span>](debugging-tools.md)
</dt> </dl>

 

 



