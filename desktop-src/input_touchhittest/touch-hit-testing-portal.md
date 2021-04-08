---
title: 觸控點擊測試
description: 本節中的主題提供 Windows 8 中觸控點擊測試支援的總覽。
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- 使用者互動
- input
- 指標
- 觸控
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 8cf6d28badb47a176a6feccf166344003faf1de8
ms.sourcegitcommit: 9e389b8e39616dcef8f7ff4bc53d945179401478
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/07/2020
ms.locfileid: "103841855"
---
# <a name="touch-hit-testing"></a><span data-ttu-id="074df-107">觸控點擊測試</span><span class="sxs-lookup"><span data-stu-id="074df-107">Touch Hit Testing</span></span>

## <a name="purpose"></a><span data-ttu-id="074df-108">目的</span><span class="sxs-lookup"><span data-stu-id="074df-108">Purpose</span></span>

<span data-ttu-id="074df-109">本節中的主題提供 Windows 中觸控點擊測試支援的總覽。</span><span class="sxs-lookup"><span data-stu-id="074df-109">The topics in this section provide an overview of support for Touch Hit Testing in Windows.</span></span> <span data-ttu-id="074df-110">觸控點擊測試可讓您根據 UI 元素的內容區域是否落在連絡人區域內，或包含連絡人點，來識別輸入目標。</span><span class="sxs-lookup"><span data-stu-id="074df-110">Touch Hit Testing lets you identify an input target based on whether the content area of a UI element falls within the contact area or includes the contact point.</span></span>

<span data-ttu-id="074df-111">觸控點擊測試會針對整個觸控區域使用複雜的連絡人幾何，而不是單一的插補 x y 座標。</span><span class="sxs-lookup"><span data-stu-id="074df-111">Touch hit testing uses complex contact geometry for the entire touch area rather than a single interpolated x-y coordinate.</span></span> <span data-ttu-id="074df-112">當您識別觸控輸入最可能的目標時，使用整個連絡人幾何可大幅提升精確度和精確度。</span><span class="sxs-lookup"><span data-stu-id="074df-112">Using the entire contact geometry greatly improves precision and accuracy when you're identifying the most likely target of touch input.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="074df-113">本節內容</span><span class="sxs-lookup"><span data-stu-id="074df-113">In this section</span></span>

| <span data-ttu-id="074df-114">主題</span><span class="sxs-lookup"><span data-stu-id="074df-114">Topic</span></span> | <span data-ttu-id="074df-115">描述</span><span class="sxs-lookup"><span data-stu-id="074df-115">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="074df-116">觸控點擊測試參考</span><span class="sxs-lookup"><span data-stu-id="074df-116">Touch Hit Testing Reference</span></span>](touchhittest-reference.md)<br/> | <span data-ttu-id="074df-117">本節中的主題提供 [觸控點擊測試](touch-hit-testing-portal.md)的參考規格。</span><span class="sxs-lookup"><span data-stu-id="074df-117">The topics in this section provide the reference specifications for [Touch Hit Testing](touch-hit-testing-portal.md).</span></span><br/> |

## <a name="developer-audience"></a><span data-ttu-id="074df-118">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="074df-118">Developer audience</span></span>

<span data-ttu-id="074df-119">觸控點擊測試 Api 是針對建立 UI 架構的開發人員所設計，可在桌面應用程式之間提供一致的觸控優化使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="074df-119">The Touch Hit Testing APIs are designed for developers who are building UI frameworks that provide a consistent touch-optimized user experience across desktop applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="074df-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="074df-120">Related topics</span></span>

[<span data-ttu-id="074df-121">使用者互動</span><span class="sxs-lookup"><span data-stu-id="074df-121">User Interaction</span></span>](../user-interaction.md)
