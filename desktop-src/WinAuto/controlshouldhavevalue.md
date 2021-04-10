---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183668"
---
# <a name="controlshouldhavevalue"></a><span data-ttu-id="20c94-103">ControlShouldHaveValue</span><span class="sxs-lookup"><span data-stu-id="20c94-103">ControlShouldHaveValue</span></span>

## <a name="text"></a><span data-ttu-id="20c94-104">Text</span><span class="sxs-lookup"><span data-stu-id="20c94-104">Text</span></span>

<span data-ttu-id="20c94-105">角色為的控制項 {0} 應具有值，但未實 \_ accValue</span><span class="sxs-lookup"><span data-stu-id="20c94-105">A control with role of {0} should have a value but get\_accValue is not implemented</span></span>

## <a name="type"></a><span data-ttu-id="20c94-106">類型</span><span class="sxs-lookup"><span data-stu-id="20c94-106">Type</span></span>

<span data-ttu-id="20c94-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="20c94-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="20c94-108">描述</span><span class="sxs-lookup"><span data-stu-id="20c94-108">Description</span></span>

<span data-ttu-id="20c94-109">根據指派的 MSAA 角色，元素不會如預期般提供值，這表示該元素未實作用 [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) 方法。</span><span class="sxs-lookup"><span data-stu-id="20c94-109">An element does not supply a value as expected based on the assigned MSAA role, implying that the element does not have the [**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) method implemented.</span></span> <span data-ttu-id="20c94-110">例如，下列 MSAA 角色應該都提供一個值。</span><span class="sxs-lookup"><span data-stu-id="20c94-110">For example, the following MSAA roles should all supply a value.</span></span>

-   <span data-ttu-id="20c94-111">角色 \_ 系統 \_ COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="20c94-111">ROLE\_SYSTEM\_COMBOBOX</span></span>
-   <span data-ttu-id="20c94-112">角色 \_ 系統 \_ IPADDRESS</span><span class="sxs-lookup"><span data-stu-id="20c94-112">ROLE\_SYSTEM\_IPADDRESS</span></span>
-   <span data-ttu-id="20c94-113">角色 \_ 系統 \_ 連結</span><span class="sxs-lookup"><span data-stu-id="20c94-113">ROLE\_SYSTEM\_LINK</span></span>
-   <span data-ttu-id="20c94-114">角色 \_ 系統 \_ OUTLINEITEM</span><span class="sxs-lookup"><span data-stu-id="20c94-114">ROLE\_SYSTEM\_OUTLINEITEM</span></span>
-   <span data-ttu-id="20c94-115">角色 \_ 系統 \_ PROGRESSBAR</span><span class="sxs-lookup"><span data-stu-id="20c94-115">ROLE\_SYSTEM\_PROGRESSBAR</span></span>
-   <span data-ttu-id="20c94-116">角色 \_ 系統 \_ 滑杆</span><span class="sxs-lookup"><span data-stu-id="20c94-116">ROLE\_SYSTEM\_SLIDER</span></span>
-   <span data-ttu-id="20c94-117">角色系統已進行數值 \_ \_ 調節</span><span class="sxs-lookup"><span data-stu-id="20c94-117">ROLE\_SYSTEM\_SPINBUTTON</span></span>
-   <span data-ttu-id="20c94-118">角色 \_ 系統 \_ 捲軸</span><span class="sxs-lookup"><span data-stu-id="20c94-118">ROLE\_SYSTEM\_SCROLLBAR</span></span>
-   <span data-ttu-id="20c94-119">角色 \_ 系統 \_ 文字</span><span class="sxs-lookup"><span data-stu-id="20c94-119">ROLE\_SYSTEM\_TEXT</span></span>

<span data-ttu-id="20c94-120">這個問題是因為有內建值的元素必須能夠將該值回報給使用者，所以依賴螢幕讀取器和鍵盤進行導覽的人會遇到問題。</span><span class="sxs-lookup"><span data-stu-id="20c94-120">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because an element that has an intrinsic value must be able to report that value to a user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="20c94-121">可能的原因</span><span class="sxs-lookup"><span data-stu-id="20c94-121">Possible causes</span></span>

<span data-ttu-id="20c94-122">元素或其父系的 MSAA 角色設定不當。</span><span class="sxs-lookup"><span data-stu-id="20c94-122">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20c94-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="20c94-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20c94-124">**IAccessible：： get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="20c94-124">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="20c94-125">**物件角色**</span><span class="sxs-lookup"><span data-stu-id="20c94-125">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




