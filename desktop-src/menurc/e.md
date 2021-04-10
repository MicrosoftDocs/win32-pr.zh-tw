---
title: 'E (功能表和其他資源) '
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093700"
---
# <a name="e-menus-and-other-resources"></a><span data-ttu-id="c94b4-103">E (功能表和其他資源) </span><span class="sxs-lookup"><span data-stu-id="c94b4-103">E (Menus and Other Resources)</span></span>

<span data-ttu-id="c94b4-104">[](a.md) [B](b.md) [C](c.md) D [](u.md) [](v.md) E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="c94b4-104">[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c94b4-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**不允許空白功能表**</span><span class="sxs-lookup"><span data-stu-id="c94b4-105"><span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Empty menus not allowed**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-106">在 [**功能表**](menu-resource.md)語句中定義任何功能表項目之前，會出現 **END** 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="c94b4-106">An **END** keyword appears before any menu items are defined in the [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="c94b4-107">Microsoft Windows 32 資源編譯器 (RC) 不允許空的功能表。</span><span class="sxs-lookup"><span data-stu-id="c94b4-107">Empty menus are not permitted by Microsoft Windows 32 Resource Compiler (RC).</span></span> <span data-ttu-id="c94b4-108">請確定 **功能表** 語句內沒有任何左引號。</span><span class="sxs-lookup"><span data-stu-id="c94b4-108">Make sure that you do not have any opening quotation marks within the **MENU** statement.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**對話方塊中預期的結尾**</span><span class="sxs-lookup"><span data-stu-id="c94b4-109"><span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**END expected in Dialog**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-110">**End** 關鍵字必須出現在 [**DIALOG**](dialog-resource.md)語句的結尾。</span><span class="sxs-lookup"><span data-stu-id="c94b4-110">The **END** keyword must appear at the end of a [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="c94b4-111">請確定前面的語句沒有任何左引號。</span><span class="sxs-lookup"><span data-stu-id="c94b4-111">Make sure that there are no opening quotation marks left from the preceding statement.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**功能表中的預期結尾**</span><span class="sxs-lookup"><span data-stu-id="c94b4-112"><span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**END expected in menu**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-113">**End** 關鍵字必須出現在 [**功能表**](menu-resource.md)語句的結尾。</span><span class="sxs-lookup"><span data-stu-id="c94b4-113">The **END** keyword must appear at the end of a [**MENU**](menu-resource.md) statement.</span></span> <span data-ttu-id="c94b4-114">請確定沒有不相符的 **BEGIN** 和 **END** 語句。</span><span class="sxs-lookup"><span data-stu-id="c94b4-114">Make sure that there are no mismatched **BEGIN** and **END** statements.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**錯誤 Creatingresource-名稱**</span><span class="sxs-lookup"><span data-stu-id="c94b4-115"><span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Error Creatingresource-name**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-116">Microsoft Windows 32 資源編譯器 (RC) 無法建立指定的二進位資源 (。RES) 檔。</span><span class="sxs-lookup"><span data-stu-id="c94b4-116">Microsoft Windows 32 Resource Compiler (RC) could not create the specified binary resource (.RES) file.</span></span> <span data-ttu-id="c94b4-117">請確定它不是在唯讀磁片磁碟機上建立的。</span><span class="sxs-lookup"><span data-stu-id="c94b4-117">Make sure that it is not being created on a read-only drive.</span></span> <span data-ttu-id="c94b4-118">您可以使用 **/v** 選項來找出檔案是否正在建立。</span><span class="sxs-lookup"><span data-stu-id="c94b4-118">Use the **/v** option to find out whether the file is being created.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**快速鍵對應表中應有逗號**</span><span class="sxs-lookup"><span data-stu-id="c94b4-119"><span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Expected Comma in Accelerator Table**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-120">Microsoft Windows 32 資源編譯器 (RC) 需要 [**快速鍵**](accelerators-resource.md)語句中的 *事件* 和 *idvalue* 參數之間必須有逗號。</span><span class="sxs-lookup"><span data-stu-id="c94b4-120">Microsoft Windows 32 Resource Compiler (RC) requires a comma between the *event* and *idvalue* parameters in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**預期的控制項類別名稱**</span><span class="sxs-lookup"><span data-stu-id="c94b4-121"><span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Expected control class name**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-122">[**對話方塊**](dialog-resource.md)語句中 [**control**](control-control.md)語句的 *class* 參數必須是下列其中一個控制項類型：**按鈕**、 [**COMBOBOX**](combobox-control.md)、**編輯**、 [**LISTBOX**](listbox-control.md)、[**捲軸**](scrollbar-control.md)、**靜態** 或使用者定義。</span><span class="sxs-lookup"><span data-stu-id="c94b4-122">The *class* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement must be one of the following control types: **BUTTON**, [**COMBOBOX**](combobox-control.md), **EDIT**, [**LISTBOX**](listbox-control.md), [**SCROLLBAR**](scrollbar-control.md), **STATIC**, or user-defined.</span></span> <span data-ttu-id="c94b4-123">請確定類別拼寫正確。</span><span class="sxs-lookup"><span data-stu-id="c94b4-123">Make sure that the class is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**預期的字型名稱**</span><span class="sxs-lookup"><span data-stu-id="c94b4-124"><span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Expected font face name**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-125">[**對話方塊**](dialog-resource.md)語句中 FONT 語句的 **font-size** *參數必須* 是以雙引號括住的字元字串 ( ") 。</span><span class="sxs-lookup"><span data-stu-id="c94b4-125">The *typeface* parameter of the **FONT** statement in the [**DIALOG**](dialog-resource.md) statement must be a character string enclosed in double quotation marks (").</span></span> <span data-ttu-id="c94b4-126">此參數會指定字型的名稱。</span><span class="sxs-lookup"><span data-stu-id="c94b4-126">This parameter specifies the name of a font.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Menuitem 的預期識別碼值**</span><span class="sxs-lookup"><span data-stu-id="c94b4-127"><span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Expected ID value for Menuitem**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-128">[**MENU**](menu-resource.md)語句必須包含 [**MENUITEM**](menuitem-statement.md)語句，此語句在 *MenuID* 參數中有整數或符號常數。</span><span class="sxs-lookup"><span data-stu-id="c94b4-128">The [**MENU**](menu-resource.md) statement must contain a [**MENUITEM**](menuitem-statement.md) statement, which has either an integer or a symbolic constant in the *MenuID* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**預期的功能表字串**</span><span class="sxs-lookup"><span data-stu-id="c94b4-129"><span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Expected Menu String**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-130">每個 [**MENUITEM**](menuitem-statement.md) 和 [**POPUP**](popup-resource.md) 語句都必須包含 *文字* 參數。</span><span class="sxs-lookup"><span data-stu-id="c94b4-130">Each [**MENUITEM**](menuitem-statement.md) and [**POPUP**](popup-resource.md) statement must contain a *text* parameter.</span></span> <span data-ttu-id="c94b4-131">這個參數是以雙引號括住的字串 ( ") ，可指定功能表項目或快顯功能表的名稱。</span><span class="sxs-lookup"><span data-stu-id="c94b4-131">This parameter is a string enclosed in double quotation marks (") that specifies the name of the menu item or pop-up menu.</span></span> <span data-ttu-id="c94b4-132">**MENUITEM 分隔符號** 語句不需要加上引號的字串。</span><span class="sxs-lookup"><span data-stu-id="c94b4-132">A **MENUITEM SEPARATOR** statement requires no quoted string.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**預期的數值命令值**</span><span class="sxs-lookup"><span data-stu-id="c94b4-133"><span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Expected numeric command value**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-134">Microsoft Windows 資源編譯器 (RC) 在 [**快速鍵**](accelerators-resource.md)語句中必須要有數值 *idvalue* 參數。</span><span class="sxs-lookup"><span data-stu-id="c94b4-134">Microsoft Windows Resource Compiler (RC) was expecting a numeric *idvalue* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement.</span></span> <span data-ttu-id="c94b4-135">請確定您已使用 [**\# define**](-define.md)語句來指定值，而且使用的常數拼寫正確。</span><span class="sxs-lookup"><span data-stu-id="c94b4-135">Make sure that you have used a [**\#define**](-define.md) statement to specify the value and that the constant used is spelled correctly.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**字串資料表中應有數值常數**</span><span class="sxs-lookup"><span data-stu-id="c94b4-136"><span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Expected numeric constant in string table**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-137">定義在 [**\# 定義**](-define.md)語句中的數值常數，必須緊接在 [**STRINGTABLE**](stringtable-resource.md)語句中的 **BEGIN** 關鍵字後面。</span><span class="sxs-lookup"><span data-stu-id="c94b4-137">A numeric constant, defined in a [**\#define**](-define.md) statement, must immediately follow the **BEGIN** keyword in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**預期的數值點大小**</span><span class="sxs-lookup"><span data-stu-id="c94b4-138"><span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Expected numeric point size**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-139">[**對話方塊**](dialog-resource.md)語句中 [**FONT**](font-statement.md)語句的 *dialog* 參數必須是整數點大小值。</span><span class="sxs-lookup"><span data-stu-id="c94b4-139">The *pointsize* parameter of the [**FONT**](font-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer point-size value.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**預期的數值對話常數**</span><span class="sxs-lookup"><span data-stu-id="c94b4-140"><span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Expected Numerical Dialog constant**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-141">[**對話方塊**](dialog-resource.md)語句需要 *x*、 *y*、*寬度* 和 *高度* 參數的整數值。</span><span class="sxs-lookup"><span data-stu-id="c94b4-141">A [**DIALOG**](dialog-resource.md) statement requires integer values for the *x*, *y*, *width*, and *height* parameters.</span></span> <span data-ttu-id="c94b4-142">請確定這些值（這些值包含在 **對話方塊** 關鍵字之後）不是負數。</span><span class="sxs-lookup"><span data-stu-id="c94b4-142">Make sure that these values, which are included after the **DIALOG** keyword, are not negative.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**STRINGTABLE 中的預期字串**</span><span class="sxs-lookup"><span data-stu-id="c94b4-143"><span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Expected String in STRINGTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-144">在 [**STRINGTABLE**](stringtable-resource.md)語句中的每個數值 *stringid 指定* 參數之後，預期會有一個字串。</span><span class="sxs-lookup"><span data-stu-id="c94b4-144">A string is expected after each numeric *stringid* parameter in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**預期的字串或常數快速鍵命令**</span><span class="sxs-lookup"><span data-stu-id="c94b4-145"><span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Expected String or Constant Accelerator command**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-146">Microsoft Windows 資源編譯器 (RC) 無法判斷為加速器設定的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c94b4-146">Microsoft Windows Resource Compiler (RC) was not able to determine which key was being set up for the accelerator.</span></span> <span data-ttu-id="c94b4-147">[**快速鍵**](accelerators-resource.md)語句中的 *事件* 參數可能無效。</span><span class="sxs-lookup"><span data-stu-id="c94b4-147">The *event* parameter in the [**ACCELERATORS**](accelerators-resource.md) statement might be invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**預期的 VALUE、BLOCK 或 END 關鍵字。**</span><span class="sxs-lookup"><span data-stu-id="c94b4-148"><span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Expected VALUE, BLOCK, or END keyword.**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-149">[**VERSIONINFO**](versioninfo-resource.md)結構需要 **VALUE**、 **BLOCK** 或 **END** 關鍵字。</span><span class="sxs-lookup"><span data-stu-id="c94b4-149">The [**VERSIONINFO**](versioninfo-resource.md) structure requires a **VALUE**, **BLOCK**, or **END** keyword.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**預期的識別碼數目**</span><span class="sxs-lookup"><span data-stu-id="c94b4-150"><span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Expecting number for ID**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-151">在 [**DIALOG**](dialog-resource.md)語句中， [**CONTROL**](control-control.md)語句的 *id* 參數必須是數位。</span><span class="sxs-lookup"><span data-stu-id="c94b4-151">A number is expected for the *id* parameter of a [**CONTROL**](control-control.md) statement in the [**DIALOG**](dialog-resource.md) statement.</span></span> <span data-ttu-id="c94b4-152">請確定您有控制項識別碼的數位或 [**\# 定義**](-define.md)語句。</span><span class="sxs-lookup"><span data-stu-id="c94b4-152">Make sure that you have a number or a [**\#define**](-define.md) statement for the control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**需要以引號括住的索引鍵字串**</span><span class="sxs-lookup"><span data-stu-id="c94b4-153"><span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Expecting quoted string for key**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-154">在 **區塊** 或 **值** 關鍵字之後的索引鍵字串應以雙引號括住。</span><span class="sxs-lookup"><span data-stu-id="c94b4-154">The key string following the **BLOCK** or **VALUE** keyword should be enclosed in double quotation marks.</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**在對話方塊類別中需要引號字串**</span><span class="sxs-lookup"><span data-stu-id="c94b4-155"><span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Expecting quoted string in dialog class**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-156">在 [**對話方塊**](dialog-resource.md)語句中， [**class**](class-statement.md)語句的 *class* 參數必須是以雙引號括住的整數或字串 ( ") 。</span><span class="sxs-lookup"><span data-stu-id="c94b4-156">The *class* parameter of the [**CLASS**](class-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be an integer or a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="c94b4-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**需要在對話方塊標題中加上引號的字串**</span><span class="sxs-lookup"><span data-stu-id="c94b4-157"><span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Expecting quoted string in dialog title**</span></span>
</dt> <dd>

<span data-ttu-id="c94b4-158">在 [**對話方塊**](dialog-resource.md)語句中， [**CAPTION**](caption-statement.md)語句的 *captioNtext* 參數必須是字元字串，以雙引號括住 ( ") 。</span><span class="sxs-lookup"><span data-stu-id="c94b4-158">The *captiontext* parameter of the [**CAPTION**](caption-statement.md) statement in the [**DIALOG**](dialog-resource.md) statement must be a character string, enclosed in double quotation marks (").</span></span>

</dd> </dl>

 

 




