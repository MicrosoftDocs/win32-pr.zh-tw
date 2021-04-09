---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675663"
---
# <a name="accnameshouldnotcontainrole"></a><span data-ttu-id="d8c4b-103">AccNameShouldNotContainRole</span><span class="sxs-lookup"><span data-stu-id="d8c4b-103">AccNameShouldNotContainRole</span></span>

## <a name="text"></a><span data-ttu-id="d8c4b-104">Text</span><span class="sxs-lookup"><span data-stu-id="d8c4b-104">Text</span></span>

<span data-ttu-id="d8c4b-105">元素的名稱 ({0}) 不應包含元素的角色 (的文字 {1}) </span><span class="sxs-lookup"><span data-stu-id="d8c4b-105">Element's Name ({0}) should not contain the text of the Element's Role ({1})</span></span>

## <a name="type"></a><span data-ttu-id="d8c4b-106">類型</span><span class="sxs-lookup"><span data-stu-id="d8c4b-106">Type</span></span>

<span data-ttu-id="d8c4b-107">警告</span><span class="sxs-lookup"><span data-stu-id="d8c4b-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="d8c4b-108">描述</span><span class="sxs-lookup"><span data-stu-id="d8c4b-108">Description</span></span>

<span data-ttu-id="d8c4b-109">元素的名稱會併入其 MSAA 角色或 UIA 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="d8c4b-109">The name of an element incorporates its MSAA role or UIA control type.</span></span> <span data-ttu-id="d8c4b-110">例如，如果 [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)方法（用來抓取專案的 MSAA 名稱）傳回「角色 \_ 系統捲軸」，則可能會發生這個警告 \_ \_ \* 。</span><span class="sxs-lookup"><span data-stu-id="d8c4b-110">For example, this warning can occur if the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method—which is used to retrieve the MSAA name of an element—returns "ROLE\_SYSTEM\_SCROLLBAR\_\*".</span></span>

<span data-ttu-id="d8c4b-111">這個問題會讓依賴螢幕讀取器和鍵盤進行流覽的人員遇到問題，因為角色會被讀取兩次，或是使用者可能 unpronounceable 或非直覺。</span><span class="sxs-lookup"><span data-stu-id="d8c4b-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the role will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="d8c4b-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="d8c4b-112">Possible causes</span></span>

-   <span data-ttu-id="d8c4b-113">元素或其父系有不正確指派的名稱或標籤。</span><span class="sxs-lookup"><span data-stu-id="d8c4b-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="d8c4b-114">元素或其父系具有尚未修改為易記名稱的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="d8c4b-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="d8c4b-115">例如，button1。</span><span class="sxs-lookup"><span data-stu-id="d8c4b-115">For example, button1.</span></span>
-   <span data-ttu-id="d8c4b-116">開發人員不知道螢幕讀取器會讀取名稱。</span><span class="sxs-lookup"><span data-stu-id="d8c4b-116">A developer is not aware that screen readers read names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8c4b-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8c4b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8c4b-118">**IAccessible：： get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="d8c4b-118">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="d8c4b-119">Name 屬性</span><span class="sxs-lookup"><span data-stu-id="d8c4b-119">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




