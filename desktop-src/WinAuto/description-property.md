---
title: '描述屬性 (Windows 協助工具功能) '
description: 物件的 Description 屬性提供有關物件視覺外觀的文字描述。
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464149"
---
# <a name="description-property-windows-accessibility-features"></a><span data-ttu-id="ebbff-103">描述屬性 (Windows 協助工具功能) </span><span class="sxs-lookup"><span data-stu-id="ebbff-103">Description Property (Windows Accessibility features)</span></span>

> [!Note]  
> <span data-ttu-id="ebbff-104">**Description** 屬性通常使用不正確，且不受 Microsoft 消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="ebbff-104">The **Description** property is often used incorrectly and is not supported by Microsoft UI Automation.</span></span> <span data-ttu-id="ebbff-105">Microsoft Active Accessibility 伺服器開發人員不應使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="ebbff-105">Microsoft Active Accessibility server developers should not use this property.</span></span> <span data-ttu-id="ebbff-106">如果存取範圍和自動化案例需要詳細資訊，請使用消費者介面自動化專案和控制項模式所支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="ebbff-106">If more information is needed for accessibility and automation scenarios, use the properties supported by UI Automation elements and control patterns.</span></span>

 

<span data-ttu-id="ebbff-107">物件的 **description** 屬性提供有關物件視覺外觀的文字描述。</span><span class="sxs-lookup"><span data-stu-id="ebbff-107">An object's **Description** property provides a textual description about an object's visual appearance.</span></span> <span data-ttu-id="ebbff-108">描述主要是用來為視力或失明使用者提供更好的內容，但也用於內容搜尋或其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="ebbff-108">The description is primarily used to provide greater context for low-vision or blind users, but is also used for context searching or other applications.</span></span> <span data-ttu-id="ebbff-109">這個屬性可協助使用者瞭解圖示或整體的視覺外觀。</span><span class="sxs-lookup"><span data-stu-id="ebbff-109">This property can help users understand an icon or the overall visual appearance.</span></span>

<span data-ttu-id="ebbff-110">藉由呼叫 [**IAccessible：： get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)，即可抓取 **Description** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ebbff-110">The **Description** property is retrieved by calling [**IAccessible::get\_accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).</span></span>

## <a name="when-to-support-the-description-property"></a><span data-ttu-id="ebbff-111">何時支援 Description 屬性</span><span class="sxs-lookup"><span data-stu-id="ebbff-111">When to Support the Description Property</span></span>

<span data-ttu-id="ebbff-112">如果描述不明顯，或根據物件的 [**名稱**](name-property.md)、[**角色**](role-property.md)、[**狀態**](state-property.md)和 [**值**](value-property.md)屬性而不是多餘的，則伺服器支援 **description** 屬性。</span><span class="sxs-lookup"><span data-stu-id="ebbff-112">Servers support the **Description** property if the description is not obvious, or when it is not redundant based on the object's [**Name**](name-property.md), [**Role**](role-property.md), [**State**](state-property.md), and [**Value**](value-property.md) properties.</span></span> <span data-ttu-id="ebbff-113">例如，標示為「確定」的按鈕不需要額外的資訊，而顯示仙人掌圖片的按鈕則會。</span><span class="sxs-lookup"><span data-stu-id="ebbff-113">For example, a button labeled "OK" would not need additional information, whereas a button that shows a picture of a cactus would.</span></span> <span data-ttu-id="ebbff-114">這類按鈕的 [ **名稱**]、[ **角色** [**] 和 [**](help-property.md) 說明] 屬性會描述其用途，但是 **Description** 屬性會傳達較不明確的資訊;例如，「這個按鈕會顯示仙人掌的圖片」。</span><span class="sxs-lookup"><span data-stu-id="ebbff-114">The **Name**, **Role**, and [**Help**](help-property.md) properties for such a button describe its purpose, but the **Description** property conveys information that is less tangible; for example, "This button shows a picture of a cactus."</span></span>

<span data-ttu-id="ebbff-115">Microsoft Active Accessibility server 可以藉由使用 [直接注釋](direct-annotation.md)、使用 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面，或是同時執行 Microsoft Active Accessibility 和消費者介面自動化並存來處理 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息，來新增消費者介面自動化的支援。</span><span class="sxs-lookup"><span data-stu-id="ebbff-115">A Microsoft Active Accessibility server can add support for UI Automation by using [Direct Annotation](direct-annotation.md), using the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface, or by implementing Microsoft Active Accessibility and UI Automation side-by-side with both implementations handling the [**WM\_GETOBJECT**](wm-getobject.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebbff-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebbff-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebbff-117">使用直接注釋</span><span class="sxs-lookup"><span data-stu-id="ebbff-117">Using Direct Annotation</span></span>](using-direct-annotation.md)
</dt> <dt>

[<span data-ttu-id="ebbff-118">IAccessibleEx 介面</span><span class="sxs-lookup"><span data-stu-id="ebbff-118">The IAccessibleEx Interface</span></span>](iaccessibleex.md)
</dt> </dl>

 

 




