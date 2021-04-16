---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104571300"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a><span data-ttu-id="8ea6b-103">AccNavigate \_ ReturnedElementWithIncorrectParent</span><span class="sxs-lookup"><span data-stu-id="8ea6b-103">AccNavigate\_ReturnedElementWithIncorrectParent</span></span>

## <a name="text"></a><span data-ttu-id="8ea6b-104">Text</span><span class="sxs-lookup"><span data-stu-id="8ea6b-104">Text</span></span>

<span data-ttu-id="8ea6b-105">呼叫 accNavigate ( (Live Search) ，0，NAVDIR \_ FIRSTCHILD) 傳回 (x-小工具：///gadget.html) 傳回不正確的父系 (\[ Null \]) ，而不是 (即時搜尋) </span><span class="sxs-lookup"><span data-stu-id="8ea6b-105">Calling accNavigate((Live Search), 0, NAVDIR\_FIRSTCHILD) which returned (x-gadget:///gadget.html) returned the incorrect parent(\[NULL\]) and not (Live Search)</span></span>

## <a name="type"></a><span data-ttu-id="8ea6b-106">類型</span><span class="sxs-lookup"><span data-stu-id="8ea6b-106">Type</span></span>

<span data-ttu-id="8ea6b-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="8ea6b-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="8ea6b-108">描述</span><span class="sxs-lookup"><span data-stu-id="8ea6b-108">Description</span></span>

<span data-ttu-id="8ea6b-109">在 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (使用 NAVDIR FIRSTCHILD 或 NAVDIR LASTCHILD 導覽常數) 所傳回的子專案上呼叫 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)時 \_ \_ ，傳回的父項目不符合 **accNavigate** 呼叫中指定的父元素。</span><span class="sxs-lookup"><span data-stu-id="8ea6b-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

![傳回不正確父項目的無效 msaa 實作為範例。](images/accchecker-invalid-msaa-parent.png)

<span data-ttu-id="8ea6b-111">此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。</span><span class="sxs-lookup"><span data-stu-id="8ea6b-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="8ea6b-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="8ea6b-112">Possible causes</span></span>

<span data-ttu-id="8ea6b-113">不正確或不正確 MSAA 執行。</span><span class="sxs-lookup"><span data-stu-id="8ea6b-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ea6b-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ea6b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ea6b-115">**IAccessible：： accNavigate**</span><span class="sxs-lookup"><span data-stu-id="8ea6b-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="8ea6b-116">**IAccessible：： get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="8ea6b-116">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




