---
title: POPUP 資源
description: 定義可以包含功能表項目和子功能表的功能表項目。
ms.assetid: afca21c7-605e-4354-b6ec-576b81389b69
keywords:
- 快顯視窗資源功能表與其他資源
topic_type:
- apiref
api_name:
- POPUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c7a1af3bd8ed9aae8908aa7ff926a3f4799ee5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092385"
---
# <a name="popup-resource"></a><span data-ttu-id="9ecb6-104">POPUP 資源</span><span class="sxs-lookup"><span data-stu-id="9ecb6-104">POPUP resource</span></span>

<span data-ttu-id="9ecb6-105">定義可以包含功能表項目和子功能表的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-105">Defines a menu item that can contain menu items and submenus.</span></span>

``` syntax
POPUP text, [optionlist] {item-definitions ...}
```

## <a name="parameters"></a><span data-ttu-id="9ecb6-106">參數</span><span class="sxs-lookup"><span data-stu-id="9ecb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ecb6-107"><span id="text"></span><span id="TEXT"></span>*文本*</span><span class="sxs-lookup"><span data-stu-id="9ecb6-107"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="9ecb6-108">包含功能表名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-108">String that contains the name of the menu.</span></span> <span data-ttu-id="9ecb6-109">此字串必須用雙引號括住 (**"**) 。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-109">This string must be enclosed in double quotation marks (**"**).</span></span>

</dd> <dt>

<span data-ttu-id="9ecb6-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span><span class="sxs-lookup"><span data-stu-id="9ecb6-110"><span id="optionlist"></span><span id="OPTIONLIST"></span>*optionlist*</span></span>
</dt> <dd>

<span data-ttu-id="9ecb6-111">此參數會指定已重新定義的功能表選項，以指定功能表項目的外觀。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-111">This parameter specifies redefined menu options that specify the appearance of the menu item.</span></span> <span data-ttu-id="9ecb6-112">這個選擇性參數可以是下列其中一項或多項。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-112">This optional parameter can be one or more of the following.</span></span>



| <span data-ttu-id="9ecb6-113">選項</span><span class="sxs-lookup"><span data-stu-id="9ecb6-113">Option</span></span>           | <span data-ttu-id="9ecb6-114">Description</span><span class="sxs-lookup"><span data-stu-id="9ecb6-114">Description</span></span>                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ecb6-115">**檢查**</span><span class="sxs-lookup"><span data-stu-id="9ecb6-115">**CHECKED**</span></span>      | <span data-ttu-id="9ecb6-116">功能表項目旁邊有核取記號。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-116">Menu item has a check mark next to it.</span></span> <span data-ttu-id="9ecb6-117">最上層功能表的此選項無效。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-117">This option is not valid for a top-level menu.</span></span>                                                                                 |
| <span data-ttu-id="9ecb6-118">**灰色**</span><span class="sxs-lookup"><span data-stu-id="9ecb6-118">**GRAYED**</span></span>       | <span data-ttu-id="9ecb6-119">功能表項目一開始為非使用中，並顯示在功能表中的灰色或功能表文字色彩的淺色陰影。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-119">Menu item is initially inactive and appears on the menu in gray or a lightened shade of the menu-text color.</span></span> <span data-ttu-id="9ecb6-120">此選項不能與 **非** 使用中的選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-120">This option cannot be used with the **INACTIVE** option.</span></span> |
| <span data-ttu-id="9ecb6-121">**説明**</span><span class="sxs-lookup"><span data-stu-id="9ecb6-121">**HELP**</span></span>         | <span data-ttu-id="9ecb6-122">識別說明專案。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-122">Identifies a help item.</span></span> <span data-ttu-id="9ecb6-123">功能表項目放在功能表列上最右邊的位置。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-123">The menu item is place at the right-most position on the menu bar.</span></span>                                                                            |
| <span data-ttu-id="9ecb6-124">**無效**</span><span class="sxs-lookup"><span data-stu-id="9ecb6-124">**INACTIVE**</span></span>     | <span data-ttu-id="9ecb6-125">功能表項目隨即顯示，但無法選取。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-125">Menu item is displayed but it cannot be selected.</span></span> <span data-ttu-id="9ecb6-126">此選項不能與 **灰色** 選項搭配使用。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-126">This option cannot be used with the **GRAYED** option.</span></span>                                                              |
| <span data-ttu-id="9ecb6-127">**MENUBARBREAK**</span><span class="sxs-lookup"><span data-stu-id="9ecb6-127">**MENUBARBREAK**</span></span> | <span data-ttu-id="9ecb6-128">與 **MENUBREAK** 相同，不同之處在于針對快顯功能表，它會將新的資料行與舊的資料行與垂直線分開。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-128">Same as **MENUBREAK** except that for pop-up menus, it separates the new column from the old column with a vertical line.</span></span>                                             |
| <span data-ttu-id="9ecb6-129">**MENUBREAK**</span><span class="sxs-lookup"><span data-stu-id="9ecb6-129">**MENUBREAK**</span></span>    | <span data-ttu-id="9ecb6-130">將功能表項目放在靜態功能表列專案的新行上。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-130">Places the menu item on a new line for static menu-bar items.</span></span> <span data-ttu-id="9ecb6-131">在功能表中，它會將功能表項目放在新的資料行中，而且資料行之間不會有分隔線。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-131">For menus, it places the menu item in a new column with no dividing line between the columns.</span></span>           |



 

</dd> </dl>

<span data-ttu-id="9ecb6-132">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-132">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="9ecb6-133">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="9ecb6-133">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9ecb6-134">範例</span><span class="sxs-lookup"><span data-stu-id="9ecb6-134">Examples</span></span>

<span data-ttu-id="9ecb6-135">下列範例示範如何使用 **POPUP** 語句：</span><span class="sxs-lookup"><span data-stu-id="9ecb6-135">The following example demonstrates the use of the **POPUP** statement:</span></span>

``` syntax
chem MENU
{
    POPUP "&Elements"
    {
         MENUITEM "&Oxygen", 200
         MENUITEM "&Carbon", 201, CHECKED
         MENUITEM "&Hydrogen", 202
         MENUITEM SEPARATOR
         MENUITEM "&Sulfur", 203
         MENUITEM "Ch&lorine", 204
    } 
    POPUP "&Compounds"
    {
         POPUP "&Sugars"
         {
            MENUITEM "&Glucose", 301
            MENUITEM "&Sucrose", 302, CHECKED
            MENUITEM "&Lactose", 303, MENUBREAK
            MENUITEM "&Fructose", 304
         }
         POPUP "&Acids"
         {
              "&Hydrochloric", 401
              "&Sulfuric", 402
         }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="9ecb6-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ecb6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ecb6-137">**功能表**</span><span class="sxs-lookup"><span data-stu-id="9ecb6-137">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="9ecb6-138">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="9ecb6-138">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> </dl>

 

 




