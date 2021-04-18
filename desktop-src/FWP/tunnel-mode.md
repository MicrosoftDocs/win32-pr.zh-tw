---
title: 通道模式
description: 通道模式 IPsec 原則案例可用來對兩個通道端點之間的所有相符流量套用 IPsec 通道模式保護。
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301531"
---
# <a name="tunnel-mode"></a><span data-ttu-id="dd1c5-103">通道模式</span><span class="sxs-lookup"><span data-stu-id="dd1c5-103">Tunnel Mode</span></span>

<span data-ttu-id="dd1c5-104">通道模式 IPsec 原則案例可用來對兩個通道端點之間的所有相符流量套用 IPsec 通道模式保護。</span><span class="sxs-lookup"><span data-stu-id="dd1c5-104">The Tunnel Mode IPsec policy scenario is used to apply IPsec tunnel mode protection for all matching traffic between two tunnel endpoints.</span></span>

<span data-ttu-id="dd1c5-105">此原則案例通常用來保護多個分公司子網之間的流量，並在網際網路上對應的閘道之間轉送。</span><span class="sxs-lookup"><span data-stu-id="dd1c5-105">This policy scenario is typically used to protect traffic between multiple branch-office subnets, when it gets forwarded between the corresponding gateways on the Internet.</span></span> <span data-ttu-id="dd1c5-106">它也可以用來保護兩部主機電腦（也稱為點對點通道）之間的端對端通訊。</span><span class="sxs-lookup"><span data-stu-id="dd1c5-106">It can also be used to secure end-to-end communication between two host machines, also referred to as point-to-point tunnels.</span></span>

<span data-ttu-id="dd1c5-107">若要使用 Windows 篩選平台 (WFP) 來執行通道模式原則，請呼叫 [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) 函式，以代表呼叫端在適當層級具現化適當的通道模式篩選。</span><span class="sxs-lookup"><span data-stu-id="dd1c5-107">To implement Tunnel Mode policy using the Windows Filtering Platform (WFP), call the [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) function that instantiates the appropriate tunnel mode filters at the appropriate layers on behalf of the caller.</span></span> <span data-ttu-id="dd1c5-108">呼叫端必須指定主要模式、快速模式提供者內容，以及描述通道內應保護之流量的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="dd1c5-108">The caller needs to specify the Main Mode, Quick Mode provider contexts, and the filter conditions describing the traffic that should be secured inside the tunnel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd1c5-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd1c5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd1c5-110">範例程式碼：使用通道模式</span><span class="sxs-lookup"><span data-stu-id="dd1c5-110">Sample code: Using Tunnel Mode</span></span>](using-tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="dd1c5-111">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="dd1c5-111">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




