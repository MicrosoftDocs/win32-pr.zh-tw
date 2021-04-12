---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372375"
---
# <a name="firstchildlastchildmismatch"></a><span data-ttu-id="9c2d6-103">FirstChildLastChildMismatch</span><span class="sxs-lookup"><span data-stu-id="9c2d6-103">FirstChildLastChildMismatch</span></span>

## <a name="text"></a><span data-ttu-id="9c2d6-104">Text</span><span class="sxs-lookup"><span data-stu-id="9c2d6-104">Text</span></span>

<span data-ttu-id="9c2d6-105">當您 {0} 從已測試的節點進行呼叫，然後重複呼叫時 {1} ，我們已完成下列子系： {2} 。</span><span class="sxs-lookup"><span data-stu-id="9c2d6-105">When navigating by calling {0} from the tested node, and then repeatedly calling {1}, we finished at the following child: {2}.</span></span> <span data-ttu-id="9c2d6-106">這不符合在測試的節點上呼叫的結果 {3} ，這會產生： {4} 。</span><span class="sxs-lookup"><span data-stu-id="9c2d6-106">This did not match the result of calling {3} on the tested node, which yielded: {4}.</span></span> <span data-ttu-id="9c2d6-107">相反地，子系應該報告為測試節點的父代。</span><span class="sxs-lookup"><span data-stu-id="9c2d6-107">Instead, the child should report as its parent the testing node.</span></span>

## <a name="type"></a><span data-ttu-id="9c2d6-108">類型</span><span class="sxs-lookup"><span data-stu-id="9c2d6-108">Type</span></span>

<span data-ttu-id="9c2d6-109">錯誤</span><span class="sxs-lookup"><span data-stu-id="9c2d6-109">Error</span></span>

## <a name="description"></a><span data-ttu-id="9c2d6-110">描述</span><span class="sxs-lookup"><span data-stu-id="9c2d6-110">Description</span></span>

<span data-ttu-id="9c2d6-111">在元素的子系之間流覽時發生問題。</span><span class="sxs-lookup"><span data-stu-id="9c2d6-111">There is a problem when navigating between element’s children.</span></span> <span data-ttu-id="9c2d6-112">1.</span><span class="sxs-lookup"><span data-stu-id="9c2d6-112">1.</span></span> <span data-ttu-id="9c2d6-113">消費者介面自動化的執行不正確或無效。</span><span class="sxs-lookup"><span data-stu-id="9c2d6-113">An incorrect or invalid UI Automation implementation.</span></span>

<span data-ttu-id="9c2d6-114">此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。</span><span class="sxs-lookup"><span data-stu-id="9c2d6-114">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="9c2d6-115">可能的原因</span><span class="sxs-lookup"><span data-stu-id="9c2d6-115">Possible causes</span></span>

<span data-ttu-id="9c2d6-116">消費者介面自動化的執行不正確或無效。</span><span class="sxs-lookup"><span data-stu-id="9c2d6-116">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c2d6-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c2d6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c2d6-118">**IUIAutomationElement::GetCachedParent**</span><span class="sxs-lookup"><span data-stu-id="9c2d6-118">**IUIAutomationElement::GetCachedParent**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[<span data-ttu-id="9c2d6-119">**IUIAutomationTreeWalker**</span><span class="sxs-lookup"><span data-stu-id="9c2d6-119">**IUIAutomationTreeWalker**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




