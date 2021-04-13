---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27c66027f7948dfa794c85dace015565d636c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184198"
---
# <a name="elementischildofparentmulipletimes"></a><span data-ttu-id="75206-103">ElementIsChildOfParentMulipleTimes</span><span class="sxs-lookup"><span data-stu-id="75206-103">ElementIsChildOfParentMulipleTimes</span></span>

## <a name="text"></a><span data-ttu-id="75206-104">Text</span><span class="sxs-lookup"><span data-stu-id="75206-104">Text</span></span>

<span data-ttu-id="75206-105">元素的 accParent 是 {0})  (，但原始專案是子 {1} 時間</span><span class="sxs-lookup"><span data-stu-id="75206-105">Element's accParent is ({0}), but original element is a child {1} times</span></span>

## <a name="type"></a><span data-ttu-id="75206-106">類型</span><span class="sxs-lookup"><span data-stu-id="75206-106">Type</span></span>

<span data-ttu-id="75206-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="75206-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="75206-108">描述</span><span class="sxs-lookup"><span data-stu-id="75206-108">Description</span></span>

<span data-ttu-id="75206-109">當在目標元素上呼叫 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 時，它會多次報告相同父系的子系。</span><span class="sxs-lookup"><span data-stu-id="75206-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the target element, it reports being a child of the same parent multiple times.</span></span>

<span data-ttu-id="75206-110">此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。</span><span class="sxs-lookup"><span data-stu-id="75206-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="75206-111">可能的原因</span><span class="sxs-lookup"><span data-stu-id="75206-111">Possible causes</span></span>

<span data-ttu-id="75206-112">不正確或不正確 MSAA 執行。</span><span class="sxs-lookup"><span data-stu-id="75206-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75206-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="75206-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75206-114">**IAccessible：： get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="75206-114">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




