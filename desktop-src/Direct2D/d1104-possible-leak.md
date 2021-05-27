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
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548673"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="cf5aa-105">D1104：可能的洩漏</span><span class="sxs-lookup"><span data-stu-id="cf5aa-105">D1104: Possible Leak</span></span>

<span data-ttu-id="cf5aa-106">已釋放 factory 處理站， \[  \] 但 \[  \] 從它建立的介面介面仍在運作中。</span><span class="sxs-lookup"><span data-stu-id="cf5aa-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="cf5aa-107">雖然在釋放 factory 之後釋放資源是有效的，但這種情況可能表示記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="cf5aa-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="cf5aa-108">預留位置</span><span class="sxs-lookup"><span data-stu-id="cf5aa-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="cf5aa-109"><span id="factory"></span><span id="FACTORY"></span>*廠*</span><span class="sxs-lookup"><span data-stu-id="cf5aa-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="cf5aa-110">已釋放的 factory 位址。</span><span class="sxs-lookup"><span data-stu-id="cf5aa-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="cf5aa-111"><span id="interface"></span><span id="INTERFACE"></span>*介面*</span><span class="sxs-lookup"><span data-stu-id="cf5aa-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="cf5aa-112">在 *factory* 上建立的介面位址。</span><span class="sxs-lookup"><span data-stu-id="cf5aa-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| <span data-ttu-id="cf5aa-113">錯誤層級</span><span class="sxs-lookup"><span data-stu-id="cf5aa-113">Error Level</span></span> | <span data-ttu-id="cf5aa-114">資訊</span><span class="sxs-lookup"><span data-stu-id="cf5aa-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="cf5aa-115">可能的原因</span><span class="sxs-lookup"><span data-stu-id="cf5aa-115">Possible Causes</span></span>

<span data-ttu-id="cf5aa-116">Factory 已釋放，但從它建立的介面仍在運作中。</span><span class="sxs-lookup"><span data-stu-id="cf5aa-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




