---
description: 如何建立 DirectShow 篩選 DLL
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: 如何建立 DirectShow 篩選 DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970677"
---
# <a name="how-to-create-a-directshow-filter-dll"></a><span data-ttu-id="62476-103">如何建立 DirectShow 篩選 DLL</span><span class="sxs-lookup"><span data-stu-id="62476-103">How to Create a DirectShow Filter DLL</span></span>

<span data-ttu-id="62476-104">本文說明如何在 Microsoft DirectShow 中將元件實作為動態連結程式庫 (DLL) 。</span><span class="sxs-lookup"><span data-stu-id="62476-104">This article describes how to implement a component as a dynamic-link library (DLL) in Microsoft DirectShow.</span></span> <span data-ttu-id="62476-105">本文是 [如何執行 iunknown](how-to-implement-iunknown.md)的接續，其中描述如何藉由從 [**CUnknown**](cunknown.md)基類衍生您的元件來執行 **iunknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="62476-105">This article is a continuation from [How to Implement IUnknown](how-to-implement-iunknown.md), which describes how to implement the **IUnknown** interface by deriving your component from the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="62476-106">本文包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="62476-106">This article contains the following sections.</span></span>

-   [<span data-ttu-id="62476-107">Class factory 和 Factory 範本</span><span class="sxs-lookup"><span data-stu-id="62476-107">Class Factories and Factory Templates</span></span>](class-factories-and-factory-templates.md)
-   [<span data-ttu-id="62476-108">Factory 範本陣列</span><span class="sxs-lookup"><span data-stu-id="62476-108">Factory Template Array</span></span>](factory-template-array.md)
-   [<span data-ttu-id="62476-109">DLL 函數</span><span class="sxs-lookup"><span data-stu-id="62476-109">DLL Functions</span></span>](dll-functions.md)

<span data-ttu-id="62476-110">註冊 DirectShow 篩選 (而不是泛型 COM 物件) 需要一些額外的步驟，這些步驟未涵蓋在本文中。</span><span class="sxs-lookup"><span data-stu-id="62476-110">Registering a DirectShow filter (as opposed to a generic COM object) requires some additional steps that are not covered in this article.</span></span> <span data-ttu-id="62476-111">如需註冊篩選準則的詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="62476-111">For information on registering filters, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62476-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="62476-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62476-113">DirectShow 和 COM</span><span class="sxs-lookup"><span data-stu-id="62476-113">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



