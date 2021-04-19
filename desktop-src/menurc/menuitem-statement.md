---
title: MENUITEM 語句
description: 定義功能表項目。
ms.assetid: b154211a-5267-4dcf-9e70-ac36671d10d3
keywords:
- MENUITEM 語句功能表和其他資源
topic_type:
- apiref
api_name:
- MENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2051b326b2f2f37c9e24e03bcb5e5116cf290a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106967653"
---
# <a name="menuitem-statement"></a><span data-ttu-id="35880-104">MENUITEM 語句</span><span class="sxs-lookup"><span data-stu-id="35880-104">MENUITEM statement</span></span>

<span data-ttu-id="35880-105">定義功能表項目。</span><span class="sxs-lookup"><span data-stu-id="35880-105">Defines a menu item.</span></span>

``` syntax
MENUITEM text, result, [optionlist]  
MENUITEM SEPARATOR
```

<dl> <dt>

<span data-ttu-id="35880-106"><span id="text"></span><span id="TEXT"></span>*文本*</span><span class="sxs-lookup"><span data-stu-id="35880-106"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="35880-107">功能表項目的名稱。</span><span class="sxs-lookup"><span data-stu-id="35880-107">The name of the menu item.</span></span>

<span data-ttu-id="35880-108">字串可以包含 escape 字元 **\\ t** **\\ 和。**</span><span class="sxs-lookup"><span data-stu-id="35880-108">The string can contain the escape characters **\\t** and **\\a**.</span></span> <span data-ttu-id="35880-109">**\\ T** 字元會在字串中插入索引標籤，用來對齊資料行中的文字。</span><span class="sxs-lookup"><span data-stu-id="35880-109">The **\\t** character inserts a tab in the string and is used to align text in columns.</span></span> <span data-ttu-id="35880-110">只有在功能表中（而不是在功能表列中）使用 Tab 字元。</span><span class="sxs-lookup"><span data-stu-id="35880-110">Tab characters should be used only in menus, not in menu bars.</span></span> <span data-ttu-id="35880-111"> (如需功能表的詳細資訊，請參閱快顯 [**資源**](popup-resource.md)。 ) **\\ 一個** 字元，將緊接在上方的所有文字排在功能表列或快顯功能表上。</span><span class="sxs-lookup"><span data-stu-id="35880-111">(For information on menus, see [**POPUP Resource**](popup-resource.md).) The **\\a** character aligns all text that follows it flush right to the menu bar or pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="35880-112"><span id="result"></span><span id="RESULT"></span>*結果*</span><span class="sxs-lookup"><span data-stu-id="35880-112"><span id="result"></span><span id="RESULT"></span>*result*</span></span>
</dt> <dd>

<span data-ttu-id="35880-113">數位，指定當使用者選取功能表項目時所產生的結果。</span><span class="sxs-lookup"><span data-stu-id="35880-113">A number that specifies the result generated when the user selects the menu item.</span></span> <span data-ttu-id="35880-114">此參數會使用整數值。</span><span class="sxs-lookup"><span data-stu-id="35880-114">This parameter takes an integer value.</span></span> <span data-ttu-id="35880-115">功能表項目結果一律為整數;當使用者按一下功能表項目名稱時，結果會傳送到擁有功能表的視窗。</span><span class="sxs-lookup"><span data-stu-id="35880-115">Menu-item results are always integers; when the user clicks the menu-item name, the result is sent to the window that owns the menu.</span></span>

</dd> <dt>

<span data-ttu-id="35880-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span><span class="sxs-lookup"><span data-stu-id="35880-116"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="35880-117">功能表項目的外觀。</span><span class="sxs-lookup"><span data-stu-id="35880-117">The appearance of the menu item.</span></span> <span data-ttu-id="35880-118">這個選擇性參數會採用下列一或多個重新定義的功能表選項，並以逗號或空格分隔。</span><span class="sxs-lookup"><span data-stu-id="35880-118">This optional parameter takes one or more of the following redefined menu options, separated by commas or spaces.</span></span>



| <span data-ttu-id="35880-119">選項</span><span class="sxs-lookup"><span data-stu-id="35880-119">Option</span></span>           | <span data-ttu-id="35880-120">Description</span><span class="sxs-lookup"><span data-stu-id="35880-120">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35880-121">**檢查**</span><span class="sxs-lookup"><span data-stu-id="35880-121">**CHECKED**</span></span>      | <span data-ttu-id="35880-122">功能表項目旁邊有核取記號。</span><span class="sxs-lookup"><span data-stu-id="35880-122">Menu item has a check mark next to it.</span></span>                                                                                                                                |
| <span data-ttu-id="35880-123">**灰色**</span><span class="sxs-lookup"><span data-stu-id="35880-123">**GRAYED**</span></span>       | <span data-ttu-id="35880-124">功能表項目一開始為非使用中，並顯示在功能表中的灰色或功能表文字色彩的淺色陰影。</span><span class="sxs-lookup"><span data-stu-id="35880-124">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="35880-125">此選項不能與 **非** 使用中的選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="35880-125">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="35880-126">**説明**</span><span class="sxs-lookup"><span data-stu-id="35880-126">**HELP**</span></span>         | <span data-ttu-id="35880-127">識別說明專案。</span><span class="sxs-lookup"><span data-stu-id="35880-127">Identifies a help item.</span></span> <span data-ttu-id="35880-128">此選項不會影響功能表項目的外觀。</span><span class="sxs-lookup"><span data-stu-id="35880-128">This option has no effect on the appearance of the menu item.</span></span>                                                                                 |
| <span data-ttu-id="35880-129">**無效**</span><span class="sxs-lookup"><span data-stu-id="35880-129">**INACTIVE**</span></span>     | <span data-ttu-id="35880-130">功能表項目隨即顯示，但無法選取。</span><span class="sxs-lookup"><span data-stu-id="35880-130">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="35880-131">此選項不能與 **灰色** 選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="35880-131">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="35880-132">**MENUBARBREAK**</span><span class="sxs-lookup"><span data-stu-id="35880-132">**MENUBARBREAK**</span></span> | <span data-ttu-id="35880-133">與 **MENUBREAK** 相同，不同之處在于針對快顯功能表，它會將新的資料行與舊的資料行與垂直線分開。</span><span class="sxs-lookup"><span data-stu-id="35880-133">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="35880-134">**MENUBREAK**</span><span class="sxs-lookup"><span data-stu-id="35880-134">**MENUBREAK**</span></span>    | <span data-ttu-id="35880-135">將功能表項目放在靜態功能表列專案的新行上。</span><span class="sxs-lookup"><span data-stu-id="35880-135">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="35880-136">在功能表中，它會將功能表項目放在新的資料行中，而且資料行之間不會有分隔線。</span><span class="sxs-lookup"><span data-stu-id="35880-136">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="35880-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM 分隔符號**</span><span class="sxs-lookup"><span data-stu-id="35880-137"><span id="MENUITEM_SEPARATOR"></span><span id="menuitem_separator"></span>**MENUITEM SEPARATOR**</span></span>
</dt> <dd>

<span data-ttu-id="35880-138">**Menuitem** 語句的 **menuitem 分隔符號** 形式會建立非作用中的功能表項目，做為功能表上兩個現用功能表項目之間的分隔線。</span><span class="sxs-lookup"><span data-stu-id="35880-138">The **MENUITEM SEPARATOR** form of the **MENUITEM** statement creates an inactive menu item that serves as a dividing bar between two active menu items on a menu.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="35880-139">範例</span><span class="sxs-lookup"><span data-stu-id="35880-139">Examples</span></span>

<span data-ttu-id="35880-140">下列範例將示範 **menuitem** 和 **menuitem 分隔符號** 語句的用法：</span><span class="sxs-lookup"><span data-stu-id="35880-140">The following example demonstrates the use of the **MENUITEM** and **MENUITEM SEPARATOR** statements:</span></span>

``` syntax
MENUITEM "&Roman", 206, CHECKED, GRAYED
MENUITEM SEPARATOR
MENUITEM "&Blackletter", 301
```

## <a name="see-also"></a><span data-ttu-id="35880-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35880-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35880-142">**功能表**</span><span class="sxs-lookup"><span data-stu-id="35880-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="35880-143">**彈出**</span><span class="sxs-lookup"><span data-stu-id="35880-143">**POPUP**</span></span>](popup-resource.md)
</dt> </dl>

 

 




