---
description: 硬體提供者會執行 IVssProviderCreateSnapshotSet 和 IVssHardwareSnapshotProvider 介面。
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: 開發 VSS 硬體提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca6e9775eb6ee4ee5f16451f51f29cc1c87b300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195067"
---
# <a name="developing-vss-hardware-providers"></a><span data-ttu-id="732b5-103">開發 VSS 硬體提供者</span><span class="sxs-lookup"><span data-stu-id="732b5-103">Developing VSS Hardware Providers</span></span>

<span data-ttu-id="732b5-104">硬體提供者會執行 [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) 和 [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="732b5-104">Hardware providers implement the [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) and [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) interfaces.</span></span> <span data-ttu-id="732b5-105">**IVssProviderCreateSnapshotSet** 會實行陰影複製狀態的排序。</span><span class="sxs-lookup"><span data-stu-id="732b5-105">**IVssProviderCreateSnapshotSet** implements the shadow copy state sequencing.</span></span> <span data-ttu-id="732b5-106">**IVssHardwareSnapshotProvider** 會在 LUN 抽象上運作。</span><span class="sxs-lookup"><span data-stu-id="732b5-106">**IVssHardwareSnapshotProvider** operates on a LUN abstraction.</span></span> <span data-ttu-id="732b5-107">提供者必須實作為跨進程的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="732b5-107">Providers must be implemented as an out-of-process COM server.</span></span> <span data-ttu-id="732b5-108">提供者會使用提供者特定的機制 (通常私用 IOCTLs) 與具現化陰影複製 Lun 的儲存子系統進行通訊。</span><span class="sxs-lookup"><span data-stu-id="732b5-108">Providers use provider-specific mechanisms (often private IOCTLs) to communicate with the storage subsystem that instantiates the shadow copy LUNs.</span></span>

-   [<span data-ttu-id="732b5-109">陰影複製提供者註冊和載入</span><span class="sxs-lookup"><span data-stu-id="732b5-109">Shadow Copy Provider Registration and Loading</span></span>](shadow-copy-provider-registration-and-loading.md)
-   [<span data-ttu-id="732b5-110">為提供者建立陰影複製</span><span class="sxs-lookup"><span data-stu-id="732b5-110">Shadow Copy Creation for Providers</span></span>](shadow-copy-creation-for-providers.md)
-   [<span data-ttu-id="732b5-111">硬體提供者互動和行為</span><span class="sxs-lookup"><span data-stu-id="732b5-111">Hardware Provider Interactions and Behaviors</span></span>](hardware-provider-interactions-and-behaviors.md)

 

 



