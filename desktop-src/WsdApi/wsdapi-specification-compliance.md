---
description: 裝置上的 web 服務 API (WSDAPI) 支援 Windows Vista 上的 Web 服務 (DPWS) 的裝置設定檔，可在 Windows 電腦與網路連線裝置之間進行 Web 服務 () 通訊。
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: WSDAPI 規格合規性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192898"
---
# <a name="wsdapi-specification-compliance"></a><span data-ttu-id="82b9b-103">WSDAPI 規格合規性</span><span class="sxs-lookup"><span data-stu-id="82b9b-103">WSDAPI Specification Compliance</span></span>

<span data-ttu-id="82b9b-104">裝置上的 web 服務 API (WSDAPI) 支援 Windows Vista 上的 Web 服務 (DPWS) 的 [裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) ，可在 windows 電腦與網路連線裝置之間進行 web 服務 () 通訊。</span><span class="sxs-lookup"><span data-stu-id="82b9b-104">Web Services on Devices API (WSDAPI) provides support for the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) on Windows Vista, which enables Web Services (WS) communication between Windows-based PCs and network connected devices.</span></span> <span data-ttu-id="82b9b-105">DPWS 組合了基本的 WS 規格，例如 [ws-事件](https://schemas.xmlsoap.org/ws/2004/08/eventing/)、 [Ws-atomictransaction 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)和 [ws-透過 ws-metadataexchange](https://schemas.xmlsoap.org/ws/2004/09/mex/)，並增強或限制其為資源受限的裝置提供一組基本的功能。</span><span class="sxs-lookup"><span data-stu-id="82b9b-105">DPWS assembles basic WS specifications, such as [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), and [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), and enhances or constrains them to provide a baseline set of capabilities for resource-constrained devices.</span></span> <span data-ttu-id="82b9b-106">此基準規格包含必要的功能，例如透過中繼資料描述裝置屬性的能力，以及選用的功能，例如基於安全性理由拒絕特定訊息的能力。</span><span class="sxs-lookup"><span data-stu-id="82b9b-106">This baseline specification contains required functionality, such as the ability to describe properties of the device through metadata, and optional functionality, such as the ability to reject specific messages for security reasons.</span></span>

<span data-ttu-id="82b9b-107">Windows Vista 中的 WSDAPI 實作為第一版的 DPWS 明確支援，而且是 DPWS 的非受控執行，其與其他 Web 服務的執行方式不同， (例如 [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) 或 [ws-management](https://schemas.xmlsoap.org/ws/2005/06/management/)) 。</span><span class="sxs-lookup"><span data-stu-id="82b9b-107">The WSDAPI implementation in Windows Vista is the first release of explicit support for the DPWS, and is an unmanaged implementation of DPWS that is separate and distinct from other Web Services implementations (such as the [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) or [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span></span>

<span data-ttu-id="82b9b-108">下列主題是裝置製造商和其他裝置實作者的相關主題，可建立與以 Windows 為基礎的 WSDAPI 用戶端和主機交互操作的裝置，而不需使用 WSDAPI。</span><span class="sxs-lookup"><span data-stu-id="82b9b-108">The following topics are of interest to device manufacturers and other device implementers that create devices that interoperate with Windows-based WSDAPI clients and hosts without using WSDAPI.</span></span> <span data-ttu-id="82b9b-109">這些主題會描述相對於基礎規格的 WSDAPI 執行。</span><span class="sxs-lookup"><span data-stu-id="82b9b-109">These topics describe the implementation of WSDAPI relative to the underlying specifications.</span></span> <span data-ttu-id="82b9b-110">其中涵蓋了執行必要功能、選擇性功能，以及未在規格中定義的其他功能。</span><span class="sxs-lookup"><span data-stu-id="82b9b-110">They cover the implementation of required functionality, optional functionality, and additional functionality not defined in the specification.</span></span>

-   [<span data-ttu-id="82b9b-111">DPWS 規格合規性</span><span class="sxs-lookup"><span data-stu-id="82b9b-111">DPWS Specification Compliance</span></span>](dpws-specification-compliance.md)
-   [<span data-ttu-id="82b9b-112">WS-探索規格合規性</span><span class="sxs-lookup"><span data-stu-id="82b9b-112">WS-Discovery Specification Compliance</span></span>](ws-discovery-specification-compliance.md)
-   [<span data-ttu-id="82b9b-113">透過 ws-metadataexchange 和 WS-Transfer 規格合規性</span><span class="sxs-lookup"><span data-stu-id="82b9b-113">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [<span data-ttu-id="82b9b-114">其他 WS-Discovery 功能</span><span class="sxs-lookup"><span data-stu-id="82b9b-114">Additional WS-Discovery Functionality</span></span>](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="82b9b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="82b9b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82b9b-116">WSD 裝置開發</span><span class="sxs-lookup"><span data-stu-id="82b9b-116">WSD Device Development</span></span>](wsd-device-development.md)
</dt> <dt>

[<span data-ttu-id="82b9b-117">WSD 裝置實行建議</span><span class="sxs-lookup"><span data-stu-id="82b9b-117">WSD Device Implementation Recommendations</span></span>](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
