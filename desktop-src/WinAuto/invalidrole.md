---
title: InvalidRole
description: InvalidRole
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969033"
---
# <a name="invalidrole"></a><span data-ttu-id="6b544-103">InvalidRole</span><span class="sxs-lookup"><span data-stu-id="6b544-103">InvalidRole</span></span>

## <a name="text"></a><span data-ttu-id="6b544-104">Text</span><span class="sxs-lookup"><span data-stu-id="6b544-104">Text</span></span>

<span data-ttu-id="6b544-105">從 get accRole 傳回的 int \_ 不是有效的角色常數，也就是 IE 角色 \_ 系統\_\*</span><span class="sxs-lookup"><span data-stu-id="6b544-105">The int returned from get\_accRole is not a valid role constant, ie ROLE\_SYSTEM\_\*</span></span>

## <a name="type"></a><span data-ttu-id="6b544-106">類型</span><span class="sxs-lookup"><span data-stu-id="6b544-106">Type</span></span>

<span data-ttu-id="6b544-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="6b544-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="6b544-108">描述</span><span class="sxs-lookup"><span data-stu-id="6b544-108">Description</span></span>

<span data-ttu-id="6b544-109">元素報告了不正確 MSAA 角色。</span><span class="sxs-lookup"><span data-stu-id="6b544-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="6b544-110">例如， [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) 方法會傳回一個整數值，這個值不會對應到有效的物件角色常數 (例如角色 \_ 系統表示 \_) 。</span><span class="sxs-lookup"><span data-stu-id="6b544-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method returns an integer value that does not map to a valid object role constant (such as ROLE\_SYSTEM\_LISTITEM).</span></span>

<span data-ttu-id="6b544-111">這個問題會讓依賴螢幕讀取器和鍵盤進行流覽的人員遇到問題，因為專案可能會不正確地識別給使用者。</span><span class="sxs-lookup"><span data-stu-id="6b544-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="6b544-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="6b544-112">Possible causes</span></span>

<span data-ttu-id="6b544-113">元素或其父系的 MSAA 角色設定不當。</span><span class="sxs-lookup"><span data-stu-id="6b544-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b544-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b544-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b544-115">**IAccessible：： get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="6b544-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="6b544-116">**物件角色**</span><span class="sxs-lookup"><span data-stu-id="6b544-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




