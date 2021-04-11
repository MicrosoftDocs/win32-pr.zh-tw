---
description: 在2006年8月之前，WS-MetadataExchange 定義了自己的 Get metadata exchange 方法，其適用于 Web 服務的裝置設定檔 (DPWS) 。
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: WS-MetadataExchange 和 WS-Transfer 規格合規性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ecad5224256f35b2157088ce091e8bd5751c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114840"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a><span data-ttu-id="dddcb-103">WS-MetadataExchange 和 WS-Transfer 規格合規性</span><span class="sxs-lookup"><span data-stu-id="dddcb-103">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>

<span data-ttu-id="dddcb-104">在2006年8月之前， [透過 ws-metadataexchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) 定義了自己的 [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange 方法，其 [適用于 Web 服務的裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) 。</span><span class="sxs-lookup"><span data-stu-id="dddcb-104">Before August 2006, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) defined its own [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange method, which was used by [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="dddcb-105">WS-MetadataExchange 規格1.1 版以 WS-Transfer 規格中定義的 Get 方法取代了此方法。</span><span class="sxs-lookup"><span data-stu-id="dddcb-105">The WS-MetadataExchange specification version 1.1 replaced this method with the Get method defined in the WS-Transfer specification.</span></span>

<span data-ttu-id="dddcb-106">在目前的模型中，WS-Transfer 會提供 [Get](get--metadata-exchange--http-request-and-message.md) 方法，而不會參考主體的類型。</span><span class="sxs-lookup"><span data-stu-id="dddcb-106">In the current model, WS-Transfer provides the [Get](get--metadata-exchange--http-request-and-message.md) method and makes no reference to the type of the body.</span></span> <span data-ttu-id="dddcb-107">WS-MetadataExchange 描述內文的格式，以及在單一回應中封裝多個中繼資料片段的機制，而 DPWS 則描述服務應該包含在中繼資料回應中的特定中繼資料部分。</span><span class="sxs-lookup"><span data-stu-id="dddcb-107">WS-MetadataExchange describes the format of the body and a mechanism for packaging multiple pieces of metadata in a single response, and DPWS describes specific pieces of metadata that a service should include in a metadata response.</span></span>

<span data-ttu-id="dddcb-108">WSDAPI 未完全支援 WS-Transfer 規格。</span><span class="sxs-lookup"><span data-stu-id="dddcb-108">WSDAPI does not fully support the WS-Transfer specification.</span></span> <span data-ttu-id="dddcb-109">因為裝置只需要 [Get](get--metadata-exchange--http-request-and-message.md) 方法，所以不會執行 WS-Transfer 的其他部分。</span><span class="sxs-lookup"><span data-stu-id="dddcb-109">Because only the [Get](get--metadata-exchange--http-request-and-message.md) method is required for devices, no other portions of WS-Transfer have been implemented.</span></span> <span data-ttu-id="dddcb-110">此外，WSDAPI 不會執行 WS-透過 ws-metadataexchange 中所述的選擇性 GetMetadata 方法。</span><span class="sxs-lookup"><span data-stu-id="dddcb-110">Also, WSDAPI does not implement the optional GetMetadata method described in WS-MetadataExchange.</span></span>

 

 



