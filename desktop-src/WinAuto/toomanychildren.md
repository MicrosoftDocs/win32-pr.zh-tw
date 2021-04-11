---
title: TooManyChildren
description: TooManyChildren
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e0eee0c29d0d5ee4cdfe66ee5b61aef4b31b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183579"
---
# <a name="toomanychildren"></a><span data-ttu-id="64714-103">TooManyChildren</span><span class="sxs-lookup"><span data-stu-id="64714-103">TooManyChildren</span></span>

## <a name="text"></a><span data-ttu-id="64714-104">Text</span><span class="sxs-lookup"><span data-stu-id="64714-104">Text</span></span>

<span data-ttu-id="64714-105">在尋找同級之後，已停止尋找其他的同級 {0} 。</span><span class="sxs-lookup"><span data-stu-id="64714-105">Stopped looking for additional siblings after finding {0} siblings.</span></span> <span data-ttu-id="64714-106">可能不正確的樹狀結構</span><span class="sxs-lookup"><span data-stu-id="64714-106">Possible incorrect tree</span></span>

## <a name="type"></a><span data-ttu-id="64714-107">類型</span><span class="sxs-lookup"><span data-stu-id="64714-107">Type</span></span>

<span data-ttu-id="64714-108">警告</span><span class="sxs-lookup"><span data-stu-id="64714-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="64714-109">描述</span><span class="sxs-lookup"><span data-stu-id="64714-109">Description</span></span>

<span data-ttu-id="64714-110">專案樹狀結構可能是迴圈，而樹狀結構深度是無限的。</span><span class="sxs-lookup"><span data-stu-id="64714-110">The element tree might be cyclic and the tree depth infinite.</span></span>

<span data-ttu-id="64714-111">此問題可能會導致自動化工具的導覽問題，因為它們會進入看似迴圈參考或無限迴圈的內容。</span><span class="sxs-lookup"><span data-stu-id="64714-111">This issue can cause navigation problems for automated tools because they will enter what appears to be a circular reference or infinite loop.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="64714-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="64714-112">Possible causes</span></span>

-   <span data-ttu-id="64714-113">應用程式或控制項設計可能太複雜。</span><span class="sxs-lookup"><span data-stu-id="64714-113">Application or control design may be too complex.</span></span> <span data-ttu-id="64714-114">有大量專案的清單視圖控制項可能會報告此警告。</span><span class="sxs-lookup"><span data-stu-id="64714-114">This warning might be reported for list-view controls that have a large number of items.</span></span> <span data-ttu-id="64714-115">在這些情況下，您通常可以忽略此警告。</span><span class="sxs-lookup"><span data-stu-id="64714-115">In these cases, you can typically ignore this warning.</span></span>
-   <span data-ttu-id="64714-116">不正確或不正確 MSAA 執行。</span><span class="sxs-lookup"><span data-stu-id="64714-116">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64714-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="64714-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64714-118">**IAccessible：： accNavigate**</span><span class="sxs-lookup"><span data-stu-id="64714-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




