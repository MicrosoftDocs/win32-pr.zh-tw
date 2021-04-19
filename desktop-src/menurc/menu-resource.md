---
title: 功能表資源
description: 定義功能表資源的內容。 |功能表資源
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- 功能表資源功能表與其他資源
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993839"
---
# <a name="menu-resource"></a><span data-ttu-id="96232-105">功能表資源</span><span class="sxs-lookup"><span data-stu-id="96232-105">MENU resource</span></span>

<span data-ttu-id="96232-106">定義功能表資源的內容。</span><span class="sxs-lookup"><span data-stu-id="96232-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="96232-107">功能表資源是一組資訊，可定義應用程式功能表的外觀和功能。</span><span class="sxs-lookup"><span data-stu-id="96232-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="96232-108">功能表是一種特殊的輸入工具，可讓使用者選取命令，並從功能表項目清單中開啟子功能表。</span><span class="sxs-lookup"><span data-stu-id="96232-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span>

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a><span data-ttu-id="96232-109">參數</span><span class="sxs-lookup"><span data-stu-id="96232-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96232-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span><span class="sxs-lookup"><span data-stu-id="96232-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span></span>
</dt> <dd>

<span data-ttu-id="96232-111">識別功能表的編號。</span><span class="sxs-lookup"><span data-stu-id="96232-111">Number that identifies the menu.</span></span> <span data-ttu-id="96232-112">此值為1到65535範圍內的唯一字串或唯一的16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="96232-112">This value is either a unique string or a unique 16-bit unsigned integer value in the range of 1 to 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="96232-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*</span><span class="sxs-lookup"><span data-stu-id="96232-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="96232-114">這個參數可以是下列其中零個語句。</span><span class="sxs-lookup"><span data-stu-id="96232-114">This parameter can be zero of more of the following statements.</span></span>



| <span data-ttu-id="96232-115">陳述式</span><span class="sxs-lookup"><span data-stu-id="96232-115">Statement</span></span>                                                        | <span data-ttu-id="96232-116">描述</span><span class="sxs-lookup"><span data-stu-id="96232-116">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96232-117">[**特性**](characteristics-statement.md) *dword*</span><span class="sxs-lookup"><span data-stu-id="96232-117">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="96232-118">有關可供讀取和寫入資源檔的工具使用之資源的使用者定義資訊。</span><span class="sxs-lookup"><span data-stu-id="96232-118">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="96232-119">如需詳細資訊，請參閱 [**特性**](characteristics-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="96232-119">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="96232-120">[**語言**](language-statement.md)*語言*、*語言*</span><span class="sxs-lookup"><span data-stu-id="96232-120">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="96232-121">資源的語言。</span><span class="sxs-lookup"><span data-stu-id="96232-121">Language for the resource.</span></span> <span data-ttu-id="96232-122">如需詳細資訊，請參閱 [**語言**](language-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="96232-122">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="96232-123">[**版本**](version-statement.md) *dword*</span><span class="sxs-lookup"><span data-stu-id="96232-123">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="96232-124">資源的使用者定義版本號碼，可供讀取和寫入資源檔的工具使用。</span><span class="sxs-lookup"><span data-stu-id="96232-124">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="96232-125">如需詳細資訊，請參閱 [**版本**](version-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="96232-125">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> </dl>

<span data-ttu-id="96232-126">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="96232-126">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="96232-127">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="96232-127">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="96232-128">範例</span><span class="sxs-lookup"><span data-stu-id="96232-128">Examples</span></span>

<span data-ttu-id="96232-129">以下是完整 **功能表** 語句的範例：</span><span class="sxs-lookup"><span data-stu-id="96232-129">The following is an example of a complete **MENU** statement:</span></span>

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a><span data-ttu-id="96232-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96232-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96232-131">使用功能表</span><span class="sxs-lookup"><span data-stu-id="96232-131">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="96232-132">**加速器**</span><span class="sxs-lookup"><span data-stu-id="96232-132">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="96232-133">**特徵**</span><span class="sxs-lookup"><span data-stu-id="96232-133">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="96232-134">**語言**</span><span class="sxs-lookup"><span data-stu-id="96232-134">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="96232-135">**MENUEX**</span><span class="sxs-lookup"><span data-stu-id="96232-135">**MENUEX**</span></span>](menuex-resource.md)
</dt> <dt>

[<span data-ttu-id="96232-136">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="96232-136">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="96232-137">**彈出**</span><span class="sxs-lookup"><span data-stu-id="96232-137">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="96232-138">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="96232-138">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="96232-139">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="96232-139">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="96232-140">**版本**</span><span class="sxs-lookup"><span data-stu-id="96232-140">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
