---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675875"
---
# <a name="duplicatesiblingnames"></a><span data-ttu-id="84df7-103">DuplicateSiblingNames</span><span class="sxs-lookup"><span data-stu-id="84df7-103">DuplicateSiblingNames</span></span>

## <a name="text"></a><span data-ttu-id="84df7-104">Text</span><span class="sxs-lookup"><span data-stu-id="84df7-104">Text</span></span>

<span data-ttu-id="84df7-105">重複的同級名稱 + Role \\ " {0} \\ " 在元素之間會造成不明確的情況。</span><span class="sxs-lookup"><span data-stu-id="84df7-105">Duplicate sibling Name+Role \\"{0}\\" will cause ambiguity between elements.</span></span>

## <a name="type"></a><span data-ttu-id="84df7-106">類型</span><span class="sxs-lookup"><span data-stu-id="84df7-106">Type</span></span>

<span data-ttu-id="84df7-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="84df7-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="84df7-108">描述</span><span class="sxs-lookup"><span data-stu-id="84df7-108">Description</span></span>

<span data-ttu-id="84df7-109">專案的名稱和角色/ControlType 與另一個元素相同。</span><span class="sxs-lookup"><span data-stu-id="84df7-109">An element has the same Name and Role/ControlType as another element.</span></span>

<span data-ttu-id="84df7-110">此問題可能會造成混淆，因為螢幕讀取器將會針對所有具有相同名稱和角色/ControlType 的元素讀取相同的文字。</span><span class="sxs-lookup"><span data-stu-id="84df7-110">This issue can cause confusion because screen readers will read the same text for all the elements with the same Name and Role/ControlType.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="84df7-111">可能的原因</span><span class="sxs-lookup"><span data-stu-id="84df7-111">Possible causes</span></span>

-   <span data-ttu-id="84df7-112">元素的名稱包含角色/ControlType 文字。</span><span class="sxs-lookup"><span data-stu-id="84df7-112">Element’s name contain Role/ControlType text.</span></span>
-   <span data-ttu-id="84df7-113">專案的名稱或其父系的名稱未設定或設定不正確。</span><span class="sxs-lookup"><span data-stu-id="84df7-113">Element’s name or the name of its parent is not set or is set incorrectly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84df7-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="84df7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84df7-115">**IAccessible：： get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="84df7-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="84df7-116">Name 屬性</span><span class="sxs-lookup"><span data-stu-id="84df7-116">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="84df7-117">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84df7-117">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="84df7-118">**IUIAutomationElement.CurrentName**</span><span class="sxs-lookup"><span data-stu-id="84df7-118">**IUIAutomationElement.CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




