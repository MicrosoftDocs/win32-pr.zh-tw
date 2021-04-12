---
description: 硬體提供者互動和行為
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: 硬體提供者互動和行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192291"
---
# <a name="hardware-provider-interactions-and-behaviors"></a><span data-ttu-id="7b62a-103">硬體提供者互動和行為</span><span class="sxs-lookup"><span data-stu-id="7b62a-103">Hardware Provider Interactions and Behaviors</span></span>

<span data-ttu-id="7b62a-104">硬體提供者可能會支援寫入時複製和/或完整複製鏡像 (差異和/或 plex) 陰影複製。</span><span class="sxs-lookup"><span data-stu-id="7b62a-104">Hardware providers may support copy-on-write and/or full copy mirror (differential and/or plex) shadow copies.</span></span> <span data-ttu-id="7b62a-105">陰影複製的資源配置應遵循 [**>ivssbackupcomponents：： SetCoNtext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext)中要求者所指定的內容，並以 [**\_ VSS \_ 快照集 \_ 內容**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)為陰影複製集進行列舉。</span><span class="sxs-lookup"><span data-stu-id="7b62a-105">Resource allocation for shadow copies should follow the context specified by the requester in [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerated by [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), for the shadow copy set.</span></span>

-   <span data-ttu-id="7b62a-106">如果要求者指定提供者所支援的陰影複製內容，則提供者應該使用該方法建立陰影複製。</span><span class="sxs-lookup"><span data-stu-id="7b62a-106">If the requester specifies a shadow copy context that is supported by the provider, the provider should create a shadow copy using that method.</span></span>
-   <span data-ttu-id="7b62a-107">如果要求者指定提供者不支援的陰影複製內容，則提供者不應嘗試建立陰影複製，並透過 [**IVssHardwareSnapshotProvider：： AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported)中的 *PbIsSupported* 參數傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="7b62a-107">If the requester specifies a shadow copy context that is not supported by the provider, then the provider should not attempt to create the shadow copy and return **FALSE** through the *pbIsSupported* parameter in [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span></span>
-   <span data-ttu-id="7b62a-108">如果要求者未明確指定陰影複製內容，則提供者應該使用合理的預設行為來建立陰影複製。</span><span class="sxs-lookup"><span data-stu-id="7b62a-108">If the requester does not explicitly specify a shadow copy context, then the provider should use reasonable default behavior for shadow copy creation.</span></span>

<span data-ttu-id="7b62a-109">與 SAN RAID 子系統相關聯的硬體提供者應該支援可轉移的陰影複製，以允許在 SAN 上的主機之間進行移動。</span><span class="sxs-lookup"><span data-stu-id="7b62a-109">Hardware providers associated with SAN RAID subsystems should support transportable shadow copies to allow movement between hosts on a SAN.</span></span>

<span data-ttu-id="7b62a-110">在 SAN 上的多部機器上執行的硬體提供者，但管理相同的 RAID 子系統並不需要在 SAN 上的提供者之間協調。</span><span class="sxs-lookup"><span data-stu-id="7b62a-110">Hardware providers running on multiple machines on a SAN yet managing the same RAID subsystem do not need to coordinate between providers on a SAN.</span></span> <span data-ttu-id="7b62a-111">協調器會維持任何必要的狀態。</span><span class="sxs-lookup"><span data-stu-id="7b62a-111">The coordinator maintains any necessary state.</span></span> <span data-ttu-id="7b62a-112">可辨識的狀態有兩種：</span><span class="sxs-lookup"><span data-stu-id="7b62a-112">Two kinds of state are recognized:</span></span>

-   <span data-ttu-id="7b62a-113">支援資料存取硬體陰影複製上所含磁片區所需的狀態。</span><span class="sxs-lookup"><span data-stu-id="7b62a-113">State necessary to support data access to the volumes contained on a hardware shadow copy.</span></span> <span data-ttu-id="7b62a-114">這包括將磁片區標記為唯讀或隱藏。</span><span class="sxs-lookup"><span data-stu-id="7b62a-114">This includes any tagging of a volume as read-only or hidden.</span></span> <span data-ttu-id="7b62a-115">此狀態必須位於硬體 LUN 上，並與 LUN 一起移動。</span><span class="sxs-lookup"><span data-stu-id="7b62a-115">This state must be on the hardware LUN and travel with the LUN.</span></span> <span data-ttu-id="7b62a-116">此狀態會在開機 epoch 和/或裝置探索之間保留。</span><span class="sxs-lookup"><span data-stu-id="7b62a-116">This state is preserved across boot epochs and/or device discovery.</span></span> <span data-ttu-id="7b62a-117">VSS 會在陰影複製的存留期內管理此狀態。</span><span class="sxs-lookup"><span data-stu-id="7b62a-117">VSS manages this state for the lifetime of the shadow copy.</span></span>
-   <span data-ttu-id="7b62a-118">將特定磁片區辨識為陰影複製集一部分所需的狀態。</span><span class="sxs-lookup"><span data-stu-id="7b62a-118">State necessary to recognize a specific volume as part of a shadow copy set.</span></span> <span data-ttu-id="7b62a-119">此狀態是由 VSS 與最初建立陰影複製集的要求者一起保存。</span><span class="sxs-lookup"><span data-stu-id="7b62a-119">This state is persisted by VSS in conjunction with the requester that originally created the shadow copy set.</span></span>

<span data-ttu-id="7b62a-120">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="7b62a-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="7b62a-121">陰影複製建立程式</span><span class="sxs-lookup"><span data-stu-id="7b62a-121">The Shadow Copy Creation Process</span></span>](the-shadow-copy-creation-process.md)
-   [<span data-ttu-id="7b62a-122">陰影複製提供者的必要行為</span><span class="sxs-lookup"><span data-stu-id="7b62a-122">Required Behaviors for Shadow Copy Providers</span></span>](required-behaviors-for-shadow-copy-providers.md)
-   [<span data-ttu-id="7b62a-123">陰影複製提供者中的狀態轉換</span><span class="sxs-lookup"><span data-stu-id="7b62a-123">State Transitions in shadow copy providers</span></span>](state-transitions-in-shadow-copy-providers.md)
-   [<span data-ttu-id="7b62a-124">陰影複製提供者中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="7b62a-124">Error Handling in shadow copy providers</span></span>](error-handling-in-shadow-copy-providers.md)

 

 



