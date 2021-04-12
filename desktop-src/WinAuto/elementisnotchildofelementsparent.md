---
title: ElementIsNotChildOfElementsParent
description: ElementIsNotChildOfElementsParent
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a3d62a6ae656bffffca442ed3cbb9b85be8dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372676"
---
# <a name="elementisnotchildofelementsparent"></a><span data-ttu-id="0ce1b-103">ElementIsNotChildOfElementsParent</span><span class="sxs-lookup"><span data-stu-id="0ce1b-103">ElementIsNotChildOfElementsParent</span></span>

## <a name="text"></a><span data-ttu-id="0ce1b-104">Text</span><span class="sxs-lookup"><span data-stu-id="0ce1b-104">Text</span></span>

<span data-ttu-id="0ce1b-105">元素不是其父系的子系</span><span class="sxs-lookup"><span data-stu-id="0ce1b-105">Element is not a child of it's parent</span></span>

## <a name="type"></a><span data-ttu-id="0ce1b-106">類型</span><span class="sxs-lookup"><span data-stu-id="0ce1b-106">Type</span></span>

<span data-ttu-id="0ce1b-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="0ce1b-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="0ce1b-108">描述</span><span class="sxs-lookup"><span data-stu-id="0ce1b-108">Description</span></span>

<span data-ttu-id="0ce1b-109">在 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (使用 NAVDIR FIRSTCHILD 或 NAVDIR LASTCHILD 導覽常數) 所傳回的子專案上呼叫 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)時 \_ \_ ，傳回的父項目不符合 **accNavigate** 呼叫中指定的父元素。</span><span class="sxs-lookup"><span data-stu-id="0ce1b-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

<span data-ttu-id="0ce1b-110">此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。</span><span class="sxs-lookup"><span data-stu-id="0ce1b-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="0ce1b-111">可能的原因</span><span class="sxs-lookup"><span data-stu-id="0ce1b-111">Possible causes</span></span>

<span data-ttu-id="0ce1b-112">不正確或不正確 MSAA 執行。</span><span class="sxs-lookup"><span data-stu-id="0ce1b-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ce1b-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ce1b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ce1b-114">**IAccessible：： accNavigate**</span><span class="sxs-lookup"><span data-stu-id="0ce1b-114">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="0ce1b-115">**IAccessible：： get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="0ce1b-115">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




