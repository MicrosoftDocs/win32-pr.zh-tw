---
title: NullParent
description: NullParent
ms.assetid: F9563D73-66EF-4C66-8783-B034AA7A212E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765217f8d2d46645358d590c5a93310b04da01b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300707"
---
# <a name="nullparent"></a><span data-ttu-id="9ed7d-103">NullParent</span><span class="sxs-lookup"><span data-stu-id="9ed7d-103">NullParent</span></span>

## <a name="text"></a><span data-ttu-id="9ed7d-104">Text</span><span class="sxs-lookup"><span data-stu-id="9ed7d-104">Text</span></span>

<span data-ttu-id="9ed7d-105">元素父系為 Null</span><span class="sxs-lookup"><span data-stu-id="9ed7d-105">Elements parent is NULL</span></span>

## <a name="type"></a><span data-ttu-id="9ed7d-106">類型</span><span class="sxs-lookup"><span data-stu-id="9ed7d-106">Type</span></span>

<span data-ttu-id="9ed7d-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="9ed7d-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="9ed7d-108">描述</span><span class="sxs-lookup"><span data-stu-id="9ed7d-108">Description</span></span>

<span data-ttu-id="9ed7d-109">在元素上呼叫 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 時，會傳回 Null。</span><span class="sxs-lookup"><span data-stu-id="9ed7d-109">NULL is returned when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the element.</span></span> <span data-ttu-id="9ed7d-110">**Get \_ accParent** 方法只有在驗證目標的根項目上呼叫時，才應該傳回 Null。</span><span class="sxs-lookup"><span data-stu-id="9ed7d-110">The **get\_accParent** method should return NULL only when called on the root element of the verification target.</span></span>

<span data-ttu-id="9ed7d-111">此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。</span><span class="sxs-lookup"><span data-stu-id="9ed7d-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="9ed7d-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="9ed7d-112">Possible causes</span></span>

<span data-ttu-id="9ed7d-113">不正確或不正確 MSAA 執行。</span><span class="sxs-lookup"><span data-stu-id="9ed7d-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ed7d-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ed7d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ed7d-115">**IAccessible：： accNavigate**</span><span class="sxs-lookup"><span data-stu-id="9ed7d-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="9ed7d-116">**IAccessible：： get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="9ed7d-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




