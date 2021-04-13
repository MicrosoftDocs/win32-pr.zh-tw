---
title: D1104 可能的洩漏
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: Factory 已釋放，但從它建立的介面仍在運作中。 雖然在釋放 factory 之後釋放資源是有效的，但這種情況可能表示記憶體流失。
keywords:
- D1104 可能的洩漏 Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312195"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="5f6e3-105">D1104：可能的洩漏</span><span class="sxs-lookup"><span data-stu-id="5f6e3-105">D1104: Possible Leak</span></span>

<span data-ttu-id="5f6e3-106">已釋放 factory 處理站， \[  \] 但 \[  \] 從它建立的介面介面仍在運作中。</span><span class="sxs-lookup"><span data-stu-id="5f6e3-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="5f6e3-107">雖然在釋放 factory 之後釋放資源是有效的，但這種情況可能表示記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="5f6e3-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="5f6e3-108">預留位置</span><span class="sxs-lookup"><span data-stu-id="5f6e3-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="5f6e3-109"><span id="factory"></span><span id="FACTORY"></span>*廠*</span><span class="sxs-lookup"><span data-stu-id="5f6e3-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="5f6e3-110">已釋放的 factory 位址。</span><span class="sxs-lookup"><span data-stu-id="5f6e3-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="5f6e3-111"><span id="interface"></span><span id="INTERFACE"></span>*介面*</span><span class="sxs-lookup"><span data-stu-id="5f6e3-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="5f6e3-112">在 *factory* 上建立的介面位址。</span><span class="sxs-lookup"><span data-stu-id="5f6e3-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="5f6e3-113">錯誤層級</span><span class="sxs-lookup"><span data-stu-id="5f6e3-113">Error Level</span></span> | <span data-ttu-id="5f6e3-114">資訊</span><span class="sxs-lookup"><span data-stu-id="5f6e3-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="5f6e3-115">可能的原因</span><span class="sxs-lookup"><span data-stu-id="5f6e3-115">Possible Causes</span></span>

<span data-ttu-id="5f6e3-116">Factory 已釋放，但從它建立的介面仍在運作中。</span><span class="sxs-lookup"><span data-stu-id="5f6e3-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




