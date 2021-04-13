---
title: 'VariantNotInt (CheckRole) '
description: 'VariantNotInt (CheckRole) '
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300988"
---
# <a name="variantnotint-checkrole"></a><span data-ttu-id="456ef-103">VariantNotInt (CheckRole) </span><span class="sxs-lookup"><span data-stu-id="456ef-103">VariantNotInt (CheckRole)</span></span>

## <a name="text"></a><span data-ttu-id="456ef-104">Text</span><span class="sxs-lookup"><span data-stu-id="456ef-104">Text</span></span>

<span data-ttu-id="456ef-105">從傳回的變異數 {0} 應為， {1} 但為 {2} 。</span><span class="sxs-lookup"><span data-stu-id="456ef-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="456ef-106">類型</span><span class="sxs-lookup"><span data-stu-id="456ef-106">Type</span></span>

<span data-ttu-id="456ef-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="456ef-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="456ef-108">描述</span><span class="sxs-lookup"><span data-stu-id="456ef-108">Description</span></span>

<span data-ttu-id="456ef-109">元素報告了不正確 MSAA 角色。</span><span class="sxs-lookup"><span data-stu-id="456ef-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="456ef-110">例如，用來取出專案之 MSAA 角色的 [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) 方法，應該傳回代表其中一個 msaa 角色常數的整數值，但改為傳回另一個 variant。</span><span class="sxs-lookup"><span data-stu-id="456ef-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method used to retrieve the MSAA role of an element should return an integer value that represents one of the MSAA role constants, but is returning another variant instead.</span></span>

<span data-ttu-id="456ef-111">這個問題會讓依賴螢幕讀取器和鍵盤進行流覽的人員遇到問題，因為專案可能會不正確地識別給使用者。</span><span class="sxs-lookup"><span data-stu-id="456ef-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="456ef-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="456ef-112">Possible causes</span></span>

<span data-ttu-id="456ef-113">元素或其父系的 MSAA 角色設定不當。</span><span class="sxs-lookup"><span data-stu-id="456ef-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="456ef-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="456ef-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="456ef-115">**IAccessible：： get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="456ef-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="456ef-116">**物件角色**</span><span class="sxs-lookup"><span data-stu-id="456ef-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




