---
title: 描述元堆積的配置摘要
description: 下表摘要說明著色器和非著色器可見堆積支援的相關資訊。
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfef479e88e5c77df0732113597a4742ecb909c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335564"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="9aa11-103">描述元堆積的配置摘要</span><span class="sxs-lookup"><span data-stu-id="9aa11-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="9aa11-104">下表摘要說明著色器和非著色器可見堆積支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9aa11-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="9aa11-105">著色器可見描述元堆積</span><span class="sxs-lookup"><span data-stu-id="9aa11-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="9aa11-106">非著色器可見描述元堆積</span><span class="sxs-lookup"><span data-stu-id="9aa11-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa11-107">**支援的堆積類型**</span><span class="sxs-lookup"><span data-stu-id="9aa11-107">**Heap Types Supported**</span></span>          | <span data-ttu-id="9aa11-108">CBV \_ SRV \_ UAV、取樣器</span><span class="sxs-lookup"><span data-stu-id="9aa11-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="9aa11-109">全部</span><span class="sxs-lookup"><span data-stu-id="9aa11-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9aa11-110">**支援的 CPU 頁面屬性**</span><span class="sxs-lookup"><span data-stu-id="9aa11-110">**CPU Page Properties Supported**</span></span> | <span data-ttu-id="9aa11-111">無法 \_ 使用、寫入 \_ 組合</span><span class="sxs-lookup"><span data-stu-id="9aa11-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="9aa11-112">\_回寫</span><span class="sxs-lookup"><span data-stu-id="9aa11-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="9aa11-113">**依應用程式的常駐管理**</span><span class="sxs-lookup"><span data-stu-id="9aa11-113">**Residency Management By App**</span></span>   | <span data-ttu-id="9aa11-114">是，應用程式負責</span><span class="sxs-lookup"><span data-stu-id="9aa11-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="9aa11-115">不適用 (不會) 可見的 GPU。</span><span class="sxs-lookup"><span data-stu-id="9aa11-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="9aa11-116">**描述項編輯支援**</span><span class="sxs-lookup"><span data-stu-id="9aa11-116">**Descriptor Edit Support**</span></span>       | <span data-ttu-id="9aa11-117">只有在 CPU 可見時，透過命令清單更新和/或 CPU 複製複製目的地。</span><span class="sxs-lookup"><span data-stu-id="9aa11-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="9aa11-118">僅 CPU 讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="9aa11-118">CPU read and write only.</span></span> <span data-ttu-id="9aa11-119">沒有直接的 GPU 存取權。</span><span class="sxs-lookup"><span data-stu-id="9aa11-119">No direct GPU access.</span></span> <span data-ttu-id="9aa11-120">可用於立即 CPU 複製 (作為來源和目的地) 。</span><span class="sxs-lookup"><span data-stu-id="9aa11-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="9aa11-121">可以用來做為命令清單上的更新來源-這會在命令清單記錄期間將描述項複製到命令清單儲存體中。</span><span class="sxs-lookup"><span data-stu-id="9aa11-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="9aa11-122">執行時，會將儲存的複本複製到目的地，這必須是著色器可見的堆積。</span><span class="sxs-lookup"><span data-stu-id="9aa11-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9aa11-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="9aa11-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aa11-124">描述元堆積</span><span class="sxs-lookup"><span data-stu-id="9aa11-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




