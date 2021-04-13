---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311523"
---
# <a name="elementhasnoname"></a><span data-ttu-id="f1d61-103">ElementHasNoName</span><span class="sxs-lookup"><span data-stu-id="f1d61-103">ElementHasNoName</span></span>

## <a name="text"></a><span data-ttu-id="f1d61-104">Text</span><span class="sxs-lookup"><span data-stu-id="f1d61-104">Text</span></span>

<span data-ttu-id="f1d61-105">元素沒有名稱</span><span class="sxs-lookup"><span data-stu-id="f1d61-105">Element has no name</span></span>

## <a name="type"></a><span data-ttu-id="f1d61-106">類型</span><span class="sxs-lookup"><span data-stu-id="f1d61-106">Type</span></span>

<span data-ttu-id="f1d61-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="f1d61-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="f1d61-108">描述</span><span class="sxs-lookup"><span data-stu-id="f1d61-108">Description</span></span>

<span data-ttu-id="f1d61-109">元素沒有名稱。</span><span class="sxs-lookup"><span data-stu-id="f1d61-109">An element does not have a name.</span></span> <span data-ttu-id="f1d61-110">例如，元素未實 accName，而且當 [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) 方法用來取得專案的 MSAA 名稱時，會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="f1d61-110">For example, the element does not have accName implemented and an empty string is returned when the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method is used to retrieve the MSAA name of the element.</span></span>

<span data-ttu-id="f1d61-111">這個問題會讓依賴螢幕讀取器和鍵盤進行流覽的人員遇到問題，因為專案可能會不正確地識別給使用者。</span><span class="sxs-lookup"><span data-stu-id="f1d61-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f1d61-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="f1d61-112">Possible causes</span></span>

-   <span data-ttu-id="f1d61-113">元素或其父系沒有名稱或標籤。</span><span class="sxs-lookup"><span data-stu-id="f1d61-113">The element or its parent has no name or label.</span></span>
-   <span data-ttu-id="f1d61-114">系統會為元素指派 [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) ，以建議專案有名稱。</span><span class="sxs-lookup"><span data-stu-id="f1d61-114">The element is assigned an [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) that suggests the element have a name.</span></span>
-   <span data-ttu-id="f1d61-115">具有焦點的元素不應獲得焦點。</span><span class="sxs-lookup"><span data-stu-id="f1d61-115">The element that has focus should not receive focus.</span></span> <span data-ttu-id="f1d61-116">例如，標籤或停用的控制項。</span><span class="sxs-lookup"><span data-stu-id="f1d61-116">For example, a label or a disabled control.</span></span>
-   <span data-ttu-id="f1d61-117">不可見的控制項已獲得焦點。</span><span class="sxs-lookup"><span data-stu-id="f1d61-117">An invisible control has received focus.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1d61-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="f1d61-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1d61-119">**IAccessible：： get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="f1d61-119">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="f1d61-120">Name 屬性</span><span class="sxs-lookup"><span data-stu-id="f1d61-120">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




