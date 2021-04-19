---
title: MENUEX 資源
description: 定義功能表資源的內容。 |MENUEX 資源
ms.assetid: a83e1e78-2af4-4257-906e-7eb6d98bcbc8
keywords:
- MENUEX 資源功能表與其他資源
topic_type:
- apiref
api_name:
- MENUEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ed379fb97d2795a166571fb48cde2c233021a33
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106979866"
---
# <a name="menuex-resource"></a><span data-ttu-id="03857-105">MENUEX 資源</span><span class="sxs-lookup"><span data-stu-id="03857-105">MENUEX resource</span></span>

<span data-ttu-id="03857-106">定義功能表資源的內容。</span><span class="sxs-lookup"><span data-stu-id="03857-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="03857-107">功能表資源是一組資訊，可定義應用程式功能表的外觀和功能。</span><span class="sxs-lookup"><span data-stu-id="03857-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="03857-108">功能表是一種特殊的輸入工具，可讓使用者選取命令，並從功能表項目清單中開啟子功能表。</span><span class="sxs-lookup"><span data-stu-id="03857-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span> <span data-ttu-id="03857-109">它也會定義下列各項：</span><span class="sxs-lookup"><span data-stu-id="03857-109">It also defines the following:</span></span>

-   <span data-ttu-id="03857-110">功能表上的說明識別碼。</span><span class="sxs-lookup"><span data-stu-id="03857-110">Help identifiers on menus.</span></span>
-   <span data-ttu-id="03857-111">功能表上的識別碼。</span><span class="sxs-lookup"><span data-stu-id="03857-111">Identifiers on menus.</span></span>
-   <span data-ttu-id="03857-112">使用 **MFT \_ \** _ 類型旗標和 _*MFS \_ \*\*_ 狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="03857-112">Use of the **MFT\_\** _ type flags and _*MFS\_\*\*_ state flags.</span></span> <span data-ttu-id="03857-113">如需這些旗標的詳細資訊，請參閱 [_ *MENUITEMINFO* \*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)結構。</span><span class="sxs-lookup"><span data-stu-id="03857-113">For more information on these flags, see the [_ *MENUITEMINFO*\*](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span>

``` syntax
menuID MENUEX{ [{[MENUITEM itemText [,[id][, [type][, state]]]] | 
    POPUP itemText [,[id][, [type][, [state][, helpID]]]] { popupBody } } . . .]}
```

## <a name="parameters"></a><span data-ttu-id="03857-114">參數</span><span class="sxs-lookup"><span data-stu-id="03857-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03857-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span><span class="sxs-lookup"><span data-stu-id="03857-115"><span id="MENUITEM"></span><span id="menuitem"></span>[**MENUITEM**](menuitem-statement.md)</span></span>
</dt> <dd>

<span data-ttu-id="03857-116">定義功能表項目。</span><span class="sxs-lookup"><span data-stu-id="03857-116">Defines a menu item.</span></span>

<dl> <dt>

<span data-ttu-id="03857-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span><span class="sxs-lookup"><span data-stu-id="03857-117"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="03857-118">字串，包含功能表項目的文字。</span><span class="sxs-lookup"><span data-stu-id="03857-118">String containing the text for the menu item.</span></span> <span data-ttu-id="03857-119">如需詳細資訊，請參閱 [**MENUITEM**](menuitem-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="03857-119">For more information, see [**MENUITEM**](menuitem-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="03857-120"><span id="id"></span><span id="ID"></span>*Id*</span><span class="sxs-lookup"><span data-stu-id="03857-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="03857-121">指出功能表項目識別碼的數值運算式。</span><span class="sxs-lookup"><span data-stu-id="03857-121">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="03857-122"><span id="type"></span><span id="TYPE"></span>*類型*</span><span class="sxs-lookup"><span data-stu-id="03857-122"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="03857-123">數值運算式，指出要使用預先定義的 MFT 類型值之功能表項目的類型 \_ \* ，在 .rc 檔中加入下列語句：`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="03857-123">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="03857-124"><span id="state"></span><span id="STATE"></span>*狀態*</span><span class="sxs-lookup"><span data-stu-id="03857-124"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="03857-125">數值運算式，指出要使用預先定義的 MFS 狀態值之功能表項目的狀態 \_ \* ，在您的中加入下列語句。RC 檔案：`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="03857-125">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="03857-126"><span id="POPUP"></span><span id="popup"></span>[**彈出**](popup-resource.md)</span><span class="sxs-lookup"><span data-stu-id="03857-126"><span id="POPUP"></span><span id="popup"></span>[**POPUP**](popup-resource.md)</span></span>
</dt> <dd>

<span data-ttu-id="03857-127">定義具有與其相關聯之子功能表的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="03857-127">Defines a menu item that has a submenu associated with it.</span></span>

<dl> <dt>

<span data-ttu-id="03857-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span><span class="sxs-lookup"><span data-stu-id="03857-128"><span id="itemText"></span><span id="itemtext"></span><span id="ITEMTEXT"></span>*itemText*</span></span>
</dt> <dd>

<span data-ttu-id="03857-129">字串，包含功能表項目的文字。</span><span class="sxs-lookup"><span data-stu-id="03857-129">String containing the text for the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="03857-130"><span id="id"></span><span id="ID"></span>*Id*</span><span class="sxs-lookup"><span data-stu-id="03857-130"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="03857-131">指出功能表項目識別碼的數值運算式。</span><span class="sxs-lookup"><span data-stu-id="03857-131">Numeric expression indicating the identifier of the menu item.</span></span>

</dd> <dt>

<span data-ttu-id="03857-132"><span id="type"></span><span id="TYPE"></span>*類型*</span><span class="sxs-lookup"><span data-stu-id="03857-132"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="03857-133">數值運算式，指出要使用預先定義的 MFT 類型值之功能表項目的類型 \_ \* ，請在您的中包含下列語句。RC 檔案：`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="03857-133">Numeric expression indicating the type of the menu item To use the predefined MFT\_\* type values, include the following statement in your .RC file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="03857-134"><span id="state"></span><span id="STATE"></span>*狀態*</span><span class="sxs-lookup"><span data-stu-id="03857-134"><span id="state"></span><span id="STATE"></span>*state*</span></span>
</dt> <dd>

<span data-ttu-id="03857-135">數值運算式，指出要使用預先定義的 MFS 狀態值之功能表項目的狀態 \_ \* ，在 .rc 檔中加入下列語句：`#include "winuser.h"`</span><span class="sxs-lookup"><span data-stu-id="03857-135">Numeric expression indicating the state of the menu item To use the predefined MFS\_\* state values, include the following statement in your .rc file: `#include "winuser.h"`</span></span>

</dd> <dt>

<span data-ttu-id="03857-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="03857-136"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="03857-137">數值運算式，指出在 [**WM \_**](../shell/wm-help.md) 說明處理期間用來識別功能表的識別碼。</span><span class="sxs-lookup"><span data-stu-id="03857-137">Numeric expression indicating the identifier used to identify the menu during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="03857-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span><span class="sxs-lookup"><span data-stu-id="03857-138"><span id="popupBody"></span><span id="popupbody"></span><span id="POPUPBODY"></span>*popupBody*</span></span>
</dt> <dd>

<span data-ttu-id="03857-139">包含 [**MENUITEM**](menuitem-statement.md) 和 [**POPUP**](popup-resource.md) 語句的任何組合。</span><span class="sxs-lookup"><span data-stu-id="03857-139">Contains any combination of the [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statements.</span></span>

</dd> </dl>

<span data-ttu-id="03857-140">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="03857-140">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="03857-141">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="03857-141">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03857-142">備註</span><span class="sxs-lookup"><span data-stu-id="03857-142">Remarks</span></span>

<span data-ttu-id="03857-143">可包含在 **MENUEX** 語句中任何數值運算式內的有效算術和布耳運算如下所示：</span><span class="sxs-lookup"><span data-stu-id="03857-143">The valid arithmetic and Boolean operations that can be contained in any of the numeric expressions in the statements of **MENUEX** are as follows:</span></span>

-   <span data-ttu-id="03857-144">新增 ( ' + ' ) </span><span class="sxs-lookup"><span data-stu-id="03857-144">Add ('+')</span></span>
-   <span data-ttu-id="03857-145">減去 ( '-' ) </span><span class="sxs-lookup"><span data-stu-id="03857-145">Subtract ('-')</span></span>
-   <span data-ttu-id="03857-146">一元減號 ( '-' ) </span><span class="sxs-lookup"><span data-stu-id="03857-146">Unary minus ('-')</span></span>
-   <span data-ttu-id="03857-147">一元未 ( ' ~ ' ) </span><span class="sxs-lookup"><span data-stu-id="03857-147">Unary NOT ('~')</span></span>
-   <span data-ttu-id="03857-148">和 ( ' & ' ) </span><span class="sxs-lookup"><span data-stu-id="03857-148">AND ('&')</span></span>
-   <span data-ttu-id="03857-149">或 ( ' \| ' ) </span><span class="sxs-lookup"><span data-stu-id="03857-149">OR ('\|')</span></span>

## <a name="see-also"></a><span data-ttu-id="03857-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03857-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03857-151">使用功能表</span><span class="sxs-lookup"><span data-stu-id="03857-151">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="03857-152">**加速器**</span><span class="sxs-lookup"><span data-stu-id="03857-152">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="03857-153">**特徵**</span><span class="sxs-lookup"><span data-stu-id="03857-153">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="03857-154">**對話 框**</span><span class="sxs-lookup"><span data-stu-id="03857-154">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="03857-155">**語言**</span><span class="sxs-lookup"><span data-stu-id="03857-155">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="03857-156">**功能表**</span><span class="sxs-lookup"><span data-stu-id="03857-156">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="03857-157">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="03857-157">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="03857-158">**彈出**</span><span class="sxs-lookup"><span data-stu-id="03857-158">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="03857-159">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="03857-159">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="03857-160">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="03857-160">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="03857-161">**版本**</span><span class="sxs-lookup"><span data-stu-id="03857-161">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
