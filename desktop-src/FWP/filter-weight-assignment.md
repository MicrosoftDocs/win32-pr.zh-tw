---
title: 篩選器加權指派
description: Windows 篩選平台 (WFP) 中的每個篩選都有相關聯的權數，可在篩選仲裁期間使用。
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/26/2020
ms.locfileid: "104374825"
---
# <a name="filter-weight-assignment"></a><span data-ttu-id="2c81c-103">篩選器加權指派</span><span class="sxs-lookup"><span data-stu-id="2c81c-103">Filter Weight Assignment</span></span>

<span data-ttu-id="2c81c-104">Windows 篩選平台 (WFP) 中的每個篩選都有相關聯的權數，可在 [篩選仲裁](filter-arbitration.md)期間使用。</span><span class="sxs-lookup"><span data-stu-id="2c81c-104">Every filter in the Windows Filtering Platform (WFP) has an associated weight, which is used during [filter arbitration](filter-arbitration.md).</span></span>

<span data-ttu-id="2c81c-105">基底篩選引擎 (BFE) 所使用的篩選權數屬於類型的 [**.Fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)。</span><span class="sxs-lookup"><span data-stu-id="2c81c-105">The filter weight used by the Base Filtering Engine (BFE) is of type [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="2c81c-106">呼叫端在新增篩選時有三個選項。</span><span class="sxs-lookup"><span data-stu-id="2c81c-106">Callers have three options when adding filters.</span></span>

-   <span data-ttu-id="2c81c-107">將權數設定為 [**.Fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)。</span><span class="sxs-lookup"><span data-stu-id="2c81c-107">Set the weight to an [**FWP\_UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="2c81c-108">BFE 使用提供的權數。</span><span class="sxs-lookup"><span data-stu-id="2c81c-108">BFE uses the supplied weight as is.</span></span>
-   <span data-ttu-id="2c81c-109">將權數設為 [**\_ 空**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)的。</span><span class="sxs-lookup"><span data-stu-id="2c81c-109">Set the weight to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="2c81c-110">BFE 會自動產生範圍 \[ 0、2⁶⁰) 的加權。</span><span class="sxs-lookup"><span data-stu-id="2c81c-110">BFE automatically generates a weight in the range \[0, 2⁶⁰).</span></span>
-   <span data-ttu-id="2c81c-111">將權數設定為範圍0、15中的 [**.Fwp \_ UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="2c81c-111">Set the weight to an [**FWP\_UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) in the range \[0, 15\].</span></span> <span data-ttu-id="2c81c-112">BFE 使用提供的權數作為權數範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c81c-112">BFE uses the supplied weight as a weight range identifier.</span></span>

    <span data-ttu-id="2c81c-113">BFE 會自動產生低序位60位 (完全如同權數已設定為 [**.Fwp \_ 空白**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)) ，然後使用提供的值來設定4個高序位位。</span><span class="sxs-lookup"><span data-stu-id="2c81c-113">BFE automatically generates the low-order 60 bits (exactly as if the weight had been set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)), and then uses the supplied value to set the 4 high-order bits.</span></span> <span data-ttu-id="2c81c-114">這可讓呼叫者手動將權數空間分割成16個範圍，同時仍然在範圍內使用自動加權。</span><span class="sxs-lookup"><span data-stu-id="2c81c-114">This allows callers to manually divide the weight space into 16 ranges, while still using automatic weighting within a range.</span></span>

> [!Note]  
> <span data-ttu-id="2c81c-115">當兩個以上的標注都在相同的子層級註冊時，當相同的加權指派給篩選器時，可能會發生問題。</span><span class="sxs-lookup"><span data-stu-id="2c81c-115">When two or more callouts are registered at the same sublayer, problems may occur when the same weight is assigned to the filters.</span></span> <span data-ttu-id="2c81c-116">使用 [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0)來建立自己的子層，可避免這個問題。</span><span class="sxs-lookup"><span data-stu-id="2c81c-116">This issue can be prevented by having callouts create their own sublayer by using [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2c81c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c81c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c81c-118">**篩選權數識別碼**</span><span class="sxs-lookup"><span data-stu-id="2c81c-118">**Filter Weight Identifiers**</span></span>](filter-weight-identifiers.md)
</dt> </dl>

 

 




