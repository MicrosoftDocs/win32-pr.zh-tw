---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672019"
---
# <a name="inconsistentstate-inconsistentproperties"></a><span data-ttu-id="22aa4-103">InconsistentState, InconsistentProperties</span><span class="sxs-lookup"><span data-stu-id="22aa4-103">InconsistentState, InconsistentProperties</span></span>

## <a name="text"></a><span data-ttu-id="22aa4-104">Text</span><span class="sxs-lookup"><span data-stu-id="22aa4-104">Text</span></span>

<span data-ttu-id="22aa4-105">控制項具有不一致的狀態/屬性 {0}{1}</span><span class="sxs-lookup"><span data-stu-id="22aa4-105">A control has states/properties that are inconsistent {0} and {1}</span></span>

## <a name="type"></a><span data-ttu-id="22aa4-106">類型</span><span class="sxs-lookup"><span data-stu-id="22aa4-106">Type</span></span>

<span data-ttu-id="22aa4-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="22aa4-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="22aa4-108">描述</span><span class="sxs-lookup"><span data-stu-id="22aa4-108">Description</span></span>

<span data-ttu-id="22aa4-109">元素報告不一致或衝突的 MSAA 狀態或消費者介面自動化屬性。</span><span class="sxs-lookup"><span data-stu-id="22aa4-109">An element is reporting inconsistent or conflicting MSAA states or UI Automation properties.</span></span> <span data-ttu-id="22aa4-110">例如，當 [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) 方法傳回下列任何組合時。</span><span class="sxs-lookup"><span data-stu-id="22aa4-110">For example, when the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method returns any of the following combinations.</span></span>

-   <span data-ttu-id="22aa4-111">狀態 \_ 系統已 \_ 展開且狀態 \_ 系統 \_ 已折迭</span><span class="sxs-lookup"><span data-stu-id="22aa4-111">STATE\_SYSTEM\_EXPANDED and STATE\_SYSTEM\_COLLAPSED</span></span>
-   <span data-ttu-id="22aa4-112">已 \_ 選取狀態系統 \_ ，但無法選取狀態 \_ 系統 \_</span><span class="sxs-lookup"><span data-stu-id="22aa4-112">STATE\_SYSTEM\_SELECTED and not STATE\_SYSTEM\_SELECTABLE</span></span>
-   <span data-ttu-id="22aa4-113">以狀態 \_ 系統為 \_ 焦點且不是狀態 \_ 系統可 \_ 設定焦點</span><span class="sxs-lookup"><span data-stu-id="22aa4-113">STATE\_SYSTEM\_FOCUSED and not STATE\_SYSTEM\_FOCUSABLE</span></span>

<span data-ttu-id="22aa4-114">這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為可能會向使用者回報不正確的元素狀態。</span><span class="sxs-lookup"><span data-stu-id="22aa4-114">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="22aa4-115">可能的原因</span><span class="sxs-lookup"><span data-stu-id="22aa4-115">Possible causes</span></span>

<span data-ttu-id="22aa4-116">元素或其父系的 MSAA 狀態設定不當。</span><span class="sxs-lookup"><span data-stu-id="22aa4-116">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22aa4-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="22aa4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22aa4-118">**IAccessible：： get \_ accState**</span><span class="sxs-lookup"><span data-stu-id="22aa4-118">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="22aa4-119">**物件狀態常數**</span><span class="sxs-lookup"><span data-stu-id="22aa4-119">**Object State Constants**</span></span>](object-state-constants.md)
</dt> <dt>

[<span data-ttu-id="22aa4-120">狀態和屬性</span><span class="sxs-lookup"><span data-stu-id="22aa4-120">States and Properties</span></span>](uiauto-msaa.md)
</dt> </dl>

 

 




