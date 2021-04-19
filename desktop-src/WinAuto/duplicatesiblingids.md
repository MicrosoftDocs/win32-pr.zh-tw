---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ba2ccca45234bb49fc782c5522b4e446d77a2c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106984509"
---
# <a name="duplicatesiblingids"></a><span data-ttu-id="c551f-103">DuplicateSiblingIDs</span><span class="sxs-lookup"><span data-stu-id="c551f-103">DuplicateSiblingIDs</span></span>

## <a name="text"></a><span data-ttu-id="c551f-104">Text</span><span class="sxs-lookup"><span data-stu-id="c551f-104">Text</span></span>

<span data-ttu-id="c551f-105">重複的自動化識別碼 \\ " {0} \\ " 會在元素之間造成不明確的問題。</span><span class="sxs-lookup"><span data-stu-id="c551f-105">Duplicate Automation ID \\"{0}\\" will cause ambiguity between elements.</span></span>

## <a name="type"></a><span data-ttu-id="c551f-106">類型</span><span class="sxs-lookup"><span data-stu-id="c551f-106">Type</span></span>

<span data-ttu-id="c551f-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="c551f-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="c551f-108">描述</span><span class="sxs-lookup"><span data-stu-id="c551f-108">Description</span></span>

<span data-ttu-id="c551f-109">專案的自動化識別碼與另一個元素相同。</span><span class="sxs-lookup"><span data-stu-id="c551f-109">An element has the same Automation ID as another element.</span></span>

<span data-ttu-id="c551f-110">此問題可能會導致自動化問題，而導致測試程式碼無法參考正確的元素。</span><span class="sxs-lookup"><span data-stu-id="c551f-110">This issue can cause automation problems that prevent test code from referencing the correct element.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="c551f-111">可能的原因</span><span class="sxs-lookup"><span data-stu-id="c551f-111">Possible causes</span></span>

-   <span data-ttu-id="c551f-112">同級元素具有相同的自動化識別碼。</span><span class="sxs-lookup"><span data-stu-id="c551f-112">Sibling elements have the same Automation ID.</span></span>
-   <span data-ttu-id="c551f-113">不正確的 UIA AutomationId 屬性執行。</span><span class="sxs-lookup"><span data-stu-id="c551f-113">Incorrect implementation of the UIA AutomationId property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c551f-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="c551f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c551f-115">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c551f-115">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="c551f-116">**IUIAutomationElement.CurrentAutomationId**</span><span class="sxs-lookup"><span data-stu-id="c551f-116">**IUIAutomationElement.CurrentAutomationId**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 




