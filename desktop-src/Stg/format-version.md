---
title: 格式版本
description: 格式版本值是用來指出此資料流程格式版本的文字資料類型。
ms.assetid: 38362a45-4f49-4a85-aabe-452ff32c2812
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503019a3bfe3224e4137ac3bfd43fadbe1e15a3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507984"
---
# <a name="format-version"></a><span data-ttu-id="f5bf4-103">格式版本</span><span class="sxs-lookup"><span data-stu-id="f5bf4-103">Format Version</span></span>

<span data-ttu-id="f5bf4-104">格式版本值是用來指出此資料流程格式版本的 **文字** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-104">The Format Version value is a **WORD** data type that is used to indicate the format version of this stream.</span></span> <span data-ttu-id="f5bf4-105">它可能是零或一。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-105">It may be zero or one.</span></span> <span data-ttu-id="f5bf4-106">讀取屬性集時，應該檢查格式版本指標。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-106">The format-version indicator should be checked when reading the property set.</span></span> <span data-ttu-id="f5bf4-107">如果不是零或1，則資料流程會寫入至不同的規格，而且無法由根據此規格開發的程式碼讀取。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-107">If it is not zero or one, then the stream was written to a different specification and cannot be read by code developed according to this specification.</span></span>

<span data-ttu-id="f5bf4-108">格式為第1版的屬性集會相當於版本0，具有下列新增專案：</span><span class="sxs-lookup"><span data-stu-id="f5bf4-108">Property sets with Format Version 1 are equivalent to Version 0, with the following additions:</span></span>

-   <span data-ttu-id="f5bf4-109">區分 **大小寫的屬性名稱**。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-109">**Case sensitive property names**.</span></span> <span data-ttu-id="f5bf4-110">屬性名稱會儲存在保留的字典屬性（ [PROPERTY ID 0](/windows/desktop/Stg/reserved-property-identifiers)）中。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-110">Property names are stored in the reserved dictionary property, [Property ID 0](/windows/desktop/Stg/reserved-property-identifiers).</span></span> <span data-ttu-id="f5bf4-111">在第1版的屬性集中，這些名稱可能會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-111">In version 1 property sets, these names can be case sensitive.</span></span> <span data-ttu-id="f5bf4-112">區分大小寫是由保留行為屬性（ [PROPERTY ID 0x80000003](/windows/desktop/Stg/reserved-property-identifiers)）所決定。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-112">Case sensitivity is determined by the reserved Behavior property, [Property ID 0x80000003](/windows/desktop/Stg/reserved-property-identifiers).</span></span>
-   <span data-ttu-id="f5bf4-113">**長屬性名稱**。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-113">**Long property names**.</span></span> <span data-ttu-id="f5bf4-114">與版本0屬性集不同的第1版屬性集不受限於屬性名稱的長度。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-114">Version 1 property sets, unlike version 0 property sets, are not limited in the length of property names.</span></span> <span data-ttu-id="f5bf4-115">如需屬性名稱的詳細資訊，請參閱 [屬性識別碼 0](/windows/desktop/Stg/reserved-property-identifiers) 。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-115">See [Property ID 0](/windows/desktop/Stg/reserved-property-identifiers) for more information on property names.</span></span>
-   <span data-ttu-id="f5bf4-116">**屬性類型**。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-116">**Property types**.</span></span> <span data-ttu-id="f5bf4-117">第1版屬性集可以保留所有可保存在版本0屬性集中的屬性類型，再加上一些其他類型。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-117">Version 1 property sets can hold all the property types that can be held in a version 0 property set plus some additional types.</span></span> <span data-ttu-id="f5bf4-118">如需這些類型的詳細資訊，請參閱 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構。</span><span class="sxs-lookup"><span data-stu-id="f5bf4-118">See the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure for more information on these types.</span></span>

 

 