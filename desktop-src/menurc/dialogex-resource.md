---
title: DIALOGEX 資源
description: 定義對話方塊。 |DIALOGEX 資源
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- DIALOGEX 資源功能表與其他資源
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196054"
---
# <a name="dialogex-resource"></a><span data-ttu-id="425a2-105">DIALOGEX 資源</span><span class="sxs-lookup"><span data-stu-id="425a2-105">DIALOGEX resource</span></span>

<span data-ttu-id="425a2-106">定義對話方塊。</span><span class="sxs-lookup"><span data-stu-id="425a2-106">Defines a dialog box.</span></span> <span data-ttu-id="425a2-107">語句會定義畫面上對話方塊的位置和維度，以及對話方塊的樣式。</span><span class="sxs-lookup"><span data-stu-id="425a2-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span> <span data-ttu-id="425a2-108">它也會定義下列各項：</span><span class="sxs-lookup"><span data-stu-id="425a2-108">It also defines the following:</span></span>

-   <span data-ttu-id="425a2-109">對話方塊本身以及對話方塊內控制項的說明識別碼。</span><span class="sxs-lookup"><span data-stu-id="425a2-109">Help IDs on the dialog itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="425a2-110">針對對話方塊本身以及對話方塊內的控制項，使用 [**EXSTYLE**](exstyle-statement.md) 語句。</span><span class="sxs-lookup"><span data-stu-id="425a2-110">Use of the [**EXSTYLE**](exstyle-statement.md) statement for the dialog box itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="425a2-111">要在對話方塊中使用之字型的字型粗細和斜體設定。</span><span class="sxs-lookup"><span data-stu-id="425a2-111">Font weight and italic settings for the font to be used in the dialog box.</span></span>
-   <span data-ttu-id="425a2-112">對話方塊內控制項的控制項特定資料。</span><span class="sxs-lookup"><span data-stu-id="425a2-112">Control-specific data for controls within the dialog box.</span></span>
-   <span data-ttu-id="425a2-113">使用 **BEDIT**、 **IEDIT** 和 **HEDIT** 預先定義的系統類別名稱。</span><span class="sxs-lookup"><span data-stu-id="425a2-113">Use of the **BEDIT**, **IEDIT**, and **HEDIT** predefined system class names.</span></span>

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a><span data-ttu-id="425a2-114">參數</span><span class="sxs-lookup"><span data-stu-id="425a2-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="425a2-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="425a2-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-116">識別對話方塊的唯一名稱或唯一的16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="425a2-116">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="425a2-117"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="425a2-117"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-118">對話方塊左側畫面上的位置，以對話方塊單位表示。</span><span class="sxs-lookup"><span data-stu-id="425a2-118">Location on the screen of the left side of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="425a2-119"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="425a2-119"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-120">對話方塊頂端畫面上的位置，以對話方塊單位表示。</span><span class="sxs-lookup"><span data-stu-id="425a2-120">Location on the screen of the top of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="425a2-121"><span id="width"></span><span id="WIDTH"></span>*寬度*</span><span class="sxs-lookup"><span data-stu-id="425a2-121"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-122">對話方塊的寬度（以對話方塊單位為單位）。</span><span class="sxs-lookup"><span data-stu-id="425a2-122">Width of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="425a2-123"><span id="height"></span><span id="HEIGHT"></span>*高度*</span><span class="sxs-lookup"><span data-stu-id="425a2-123"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-124">對話方塊的高度，以對話方塊單位為單位。</span><span class="sxs-lookup"><span data-stu-id="425a2-124">Height of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="425a2-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="425a2-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-126">數值運算式，指出在 [**WM \_**](../shell/wm-help.md) 說明處理期間用來識別對話方塊的識別碼。</span><span class="sxs-lookup"><span data-stu-id="425a2-126">Numeric expression indicating the ID used to identify the dialog box during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="425a2-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*</span><span class="sxs-lookup"><span data-stu-id="425a2-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-128">對話方塊的選項。</span><span class="sxs-lookup"><span data-stu-id="425a2-128">Options for the dialog box.</span></span> <span data-ttu-id="425a2-129">這可以是零或多個下列語句。</span><span class="sxs-lookup"><span data-stu-id="425a2-129">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="425a2-130">陳述式</span><span class="sxs-lookup"><span data-stu-id="425a2-130">Statement</span></span>                                                         | <span data-ttu-id="425a2-131">描述</span><span class="sxs-lookup"><span data-stu-id="425a2-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="425a2-132">**標題** "*text*"</span><span class="sxs-lookup"><span data-stu-id="425a2-132">**CAPTION** "*text*"</span></span>                                              | <span data-ttu-id="425a2-133">對話方塊的標題列（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="425a2-133">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="425a2-134">如需詳細資訊，請參閱 [**CAPTION 語句**](caption-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-134">For more information, see [**CAPTION Statement**](caption-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="425a2-135">**特性** *dword*</span><span class="sxs-lookup"><span data-stu-id="425a2-135">**CHARACTERISTICS** *dword*</span></span>                                       | <span data-ttu-id="425a2-136">資源工具所使用的使用者定義 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="425a2-136">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="425a2-137">系統不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="425a2-137">This value is not used by the system.</span></span> <span data-ttu-id="425a2-138">如需詳細資訊，請參閱 [**特性語句**](characteristics-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-138">For more information, see [**CHARACTERISTICS Statement**](characteristics-statement.md).</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="425a2-139">**類別**_類別_</span><span class="sxs-lookup"><span data-stu-id="425a2-139">**CLASS**_class_</span></span>                                                  | <span data-ttu-id="425a2-140">以雙引號括住的16位不帶正負號的整數或字串 ( ") ，以識別對話方塊的類別。</span><span class="sxs-lookup"><span data-stu-id="425a2-140">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="425a2-141">如需詳細資訊，請參閱 [**CLASS 語句**](class-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-141">For more information, see [**CLASS Statement**](class-statement.md).</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="425a2-142">**EXSTYLE** = *擴充樣式*</span><span class="sxs-lookup"><span data-stu-id="425a2-142">**EXSTYLE**= *extended-styles*</span></span>                                    | <span data-ttu-id="425a2-143">對話方塊的擴充視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="425a2-143">Extended window style of the dialog box.</span></span> <span data-ttu-id="425a2-144">如需詳細資訊，請參閱 [**EXSTYLE 語句**](exstyle-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-144">For more information, see [**EXSTYLE Statement**](exstyle-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="425a2-145">**字型** *Dialog\*\*、"* font-family"、*權數*、*斜體*、*字元集*</span><span class="sxs-lookup"><span data-stu-id="425a2-145">**FONT** *pointsize*, "*typeface*", *weight*, *italic*, *charset*</span></span> | <span data-ttu-id="425a2-146">字型的點大小和字型。</span><span class="sxs-lookup"><span data-stu-id="425a2-146">Point size and typeface for the font.</span></span> <span data-ttu-id="425a2-147">針對 *權數*，請使用 WinGDI 中定義的 \**FW \_ \** _ 值。</span><span class="sxs-lookup"><span data-stu-id="425a2-147">For *weight*, use the \**FW\_\** _ values defined in WinGDI.h.</span></span> <span data-ttu-id="425a2-148">若為 _italic \*，請指定 TRUE 以使用斜體字型，否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="425a2-148">For _italic\*, specify TRUE to use an italic font, FALSE otherwise.</span></span> <span data-ttu-id="425a2-149">若為 *字元集*，請使用 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構之 **lfCharSet** 成員中定義的值。</span><span class="sxs-lookup"><span data-stu-id="425a2-149">For *charset*, use the value defined in the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="425a2-150">若要取得對話方塊的最終字型，應用程式應指定 *字元集* 以及其他字型屬性。</span><span class="sxs-lookup"><span data-stu-id="425a2-150">To get the definitive font for a dialog box, an application should specify *charset* along with other font properties.</span></span> <span data-ttu-id="425a2-151">如需詳細資訊，請參閱 [**字型語句**](font-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-151">For more information, see [**FONT Statement**](font-statement.md).</span></span> |
| <span data-ttu-id="425a2-152">\**語言\*\*\*語言*、*語言*</span><span class="sxs-lookup"><span data-stu-id="425a2-152">**LANGUAGE** *language*, *sublanguage*</span></span>                            | <span data-ttu-id="425a2-153">對話方塊的語言。</span><span class="sxs-lookup"><span data-stu-id="425a2-153">Language of the dialog box.</span></span> <span data-ttu-id="425a2-154">如需詳細資訊，請參閱 [**LANGUAGE 語句**](language-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-154">For more information, see [**LANGUAGE Statement**](language-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="425a2-155">**功能表** *menuname*</span><span class="sxs-lookup"><span data-stu-id="425a2-155">**MENU** *menuname*</span></span>                                               | <span data-ttu-id="425a2-156">要使用的功能表。</span><span class="sxs-lookup"><span data-stu-id="425a2-156">Menu to be used.</span></span> <span data-ttu-id="425a2-157">此值為功能表的名稱或其整數識別碼。</span><span class="sxs-lookup"><span data-stu-id="425a2-157">This value is either the name of the menu or its integer identifier.</span></span> <span data-ttu-id="425a2-158">如需詳細資訊，請參閱 [**功能表語句**](menu-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-158">For more information, see [**MENU Statement**](menu-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="425a2-159">\**樣式\*\*\*樣式*</span><span class="sxs-lookup"><span data-stu-id="425a2-159">**STYLE** *styles*</span></span>                                                | <span data-ttu-id="425a2-160">對話方塊的樣式。</span><span class="sxs-lookup"><span data-stu-id="425a2-160">Styles of the dialog box.</span></span> <span data-ttu-id="425a2-161">如需詳細資訊，請參閱 [**STYLE 語句**](style-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-161">For more information, see [**STYLE Statement**](style-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="425a2-162">**版本** *dword*</span><span class="sxs-lookup"><span data-stu-id="425a2-162">**VERSION** *dword*</span></span>                                               | <span data-ttu-id="425a2-163">使用者定義的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="425a2-163">User-defined **DWORD** value.</span></span> <span data-ttu-id="425a2-164">此語句適用于其他資源工具，而且系統不會使用此語句。</span><span class="sxs-lookup"><span data-stu-id="425a2-164">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="425a2-165">如需詳細資訊，請參閱 [**版本聲明**](version-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-165">For more information, see [**VERSION Statement**](version-statement.md).</span></span>                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="425a2-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control 語句*</span><span class="sxs-lookup"><span data-stu-id="425a2-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control-statements*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-167">**DIALOGEX** 資源的主體是由任意數目的控制語句所組成。</span><span class="sxs-lookup"><span data-stu-id="425a2-167">Body of the **DIALOGEX** resource is made up of any number of control statements.</span></span> <span data-ttu-id="425a2-168">控制語句有四個系列： [泛型]、[靜態]、[按鈕] 和 [編輯]。</span><span class="sxs-lookup"><span data-stu-id="425a2-168">There are four families of control statements: generic, static, button, and edit.</span></span> <span data-ttu-id="425a2-169">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="425a2-169">For more information, see Remarks.</span></span>

</dd> </dl>

<span data-ttu-id="425a2-170">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="425a2-170">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="425a2-171">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-171">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="425a2-172">備註</span><span class="sxs-lookup"><span data-stu-id="425a2-172">Remarks</span></span>

<span data-ttu-id="425a2-173">可能包含在 **DIALOGEX** 語句中任何數值運算式中的有效作業如下：</span><span class="sxs-lookup"><span data-stu-id="425a2-173">The valid operations that may be contained in any of the numeric expressions in the statements of **DIALOGEX** are as follows:</span></span>

-   <span data-ttu-id="425a2-174">新增 ( ' + ' ) </span><span class="sxs-lookup"><span data-stu-id="425a2-174">Add ('+')</span></span>
-   <span data-ttu-id="425a2-175">減去 ( '-' ) </span><span class="sxs-lookup"><span data-stu-id="425a2-175">Subtract ('-')</span></span>
-   <span data-ttu-id="425a2-176">一元減號 ( '-' ) </span><span class="sxs-lookup"><span data-stu-id="425a2-176">Unary minus ('-')</span></span>
-   <span data-ttu-id="425a2-177">一元未 ( ' ~ ' ) </span><span class="sxs-lookup"><span data-stu-id="425a2-177">Unary NOT ('~')</span></span>
-   <span data-ttu-id="425a2-178">和 ( ' & ' ) </span><span class="sxs-lookup"><span data-stu-id="425a2-178">AND ('&')</span></span>
-   <span data-ttu-id="425a2-179">或 ( ' \| ' ) </span><span class="sxs-lookup"><span data-stu-id="425a2-179">OR ('\|')</span></span>

<span data-ttu-id="425a2-180">資源的主體是由泛型、靜態、按鈕和編輯控制語句所組成。</span><span class="sxs-lookup"><span data-stu-id="425a2-180">The body of the resource is made up of generic, static, button, and edit control statements.</span></span> <span data-ttu-id="425a2-181">雖然這兩個語句系列都使用不同的語法來定義其控制項的特定功能，但它們全都共用定義位置、大小、擴充樣式、說明識別碼和控制項特定資料的一般語法。</span><span class="sxs-lookup"><span data-stu-id="425a2-181">While each of these families of statements uses a different syntax for defining specific features of its controls, they all share a common syntax for defining the position, size, extended styles, help identification number, and control-specific data.</span></span> <span data-ttu-id="425a2-182">如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-182">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

### <a name="generic-control-statements"></a><span data-ttu-id="425a2-183">泛型控制項語句</span><span class="sxs-lookup"><span data-stu-id="425a2-183">Generic Control Statements</span></span>

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span data-ttu-id="425a2-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="425a2-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-185">控制項的視窗文字。</span><span class="sxs-lookup"><span data-stu-id="425a2-185">Window text for the control.</span></span> <span data-ttu-id="425a2-186">如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-186">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="425a2-187"><span id="id"></span><span id="ID"></span>*Id*</span><span class="sxs-lookup"><span data-stu-id="425a2-187"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-188">控制識別碼。</span><span class="sxs-lookup"><span data-stu-id="425a2-188">Control identifier.</span></span> <span data-ttu-id="425a2-189">如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-189">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="425a2-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span><span class="sxs-lookup"><span data-stu-id="425a2-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-191">類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="425a2-191">Name of the class.</span></span> <span data-ttu-id="425a2-192">這可能是以雙引號括住的字串 ( ") 或下列其中一個預先定義的系統類別： **按鈕**、 **靜態**、 **編輯**、 **LISTBOX**、 **捲軸** 或 **COMBOBOX**。</span><span class="sxs-lookup"><span data-stu-id="425a2-192">This may be either a string enclosed in double quotation marks (") or one of the following predefined system classes: **BUTTON**, **STATIC**, **EDIT**, **LISTBOX**, **SCROLLBAR**, or **COMBOBOX**.</span></span>

</dd> <dt>

<span data-ttu-id="425a2-193"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="425a2-193"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-194">您可以將包含在 .rc 檔中的 include 新增至 .rc 檔，以使用在 Winuser 中定義的視窗樣式 (明確 **\_ \* *的 WS _、_* BS \_ \* *_、_* SS \_ \* *_、_* ES \_ \* *_、_* 磅 \_ \* *_、_* SBS \_ \* *_ 和 _* CBS \_ \*** 樣式值： `#include "winuser.h"`) 。</span><span class="sxs-lookup"><span data-stu-id="425a2-194">Window styles (explicit **WS\_\**_, _\* BS\_\**_, _\* SS\_\*\*_, _\* ES\_\*\*_, _\* LBS\_\*\*_, _\* SBS\_\*\*_, and _\* CBS\_\*\*\* style values defined in Winuser.H can be used by adding an include to the .rc file: `#include "winuser.h"`).</span></span> <span data-ttu-id="425a2-195">如需詳細資訊，請參閱 [視窗樣式](/windows/desktop/winmsg/window-styles)。</span><span class="sxs-lookup"><span data-stu-id="425a2-195">For more information, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span>

</dd> </dl>

### <a name="static-control-statements"></a><span data-ttu-id="425a2-196">靜態控制語句</span><span class="sxs-lookup"><span data-stu-id="425a2-196">Static Control Statements</span></span>

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span data-ttu-id="425a2-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span><span class="sxs-lookup"><span data-stu-id="425a2-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-198">**LTEXT**、 **RTEXT** 或 **CTEXT**。</span><span class="sxs-lookup"><span data-stu-id="425a2-198">**LTEXT**, **RTEXT**, or **CTEXT**.</span></span>

</dd> <dt>

<span data-ttu-id="425a2-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="425a2-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-200">控制項的視窗文字。</span><span class="sxs-lookup"><span data-stu-id="425a2-200">Window text for the control.</span></span> <span data-ttu-id="425a2-201">如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-201">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="425a2-202"><span id="id"></span><span id="ID"></span>*Id*</span><span class="sxs-lookup"><span data-stu-id="425a2-202"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-203">控制識別碼。</span><span class="sxs-lookup"><span data-stu-id="425a2-203">Control identifier.</span></span> <span data-ttu-id="425a2-204">如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-204">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="button-control-statements"></a><span data-ttu-id="425a2-205">Button 控制項語句</span><span class="sxs-lookup"><span data-stu-id="425a2-205">Button Control Statements</span></span>

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span data-ttu-id="425a2-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span><span class="sxs-lookup"><span data-stu-id="425a2-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-207">**AUTO3STATE**、 **AUTOCHECKBOX**、 **AUTORADIOBUTTON**、 **CHECKBOX**、 **PUSHBOX**、 **按鈕**、 **選項按鈕**、 **STATE3** 或 **USERBUTTON**。</span><span class="sxs-lookup"><span data-stu-id="425a2-207">**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CHECKBOX**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3**, or **USERBUTTON**.</span></span>

</dd> <dt>

<span data-ttu-id="425a2-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span><span class="sxs-lookup"><span data-stu-id="425a2-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-209">控制項的視窗文字。</span><span class="sxs-lookup"><span data-stu-id="425a2-209">Window text for the control.</span></span> <span data-ttu-id="425a2-210">如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-210">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="425a2-211"><span id="id"></span><span id="ID"></span>*Id*</span><span class="sxs-lookup"><span data-stu-id="425a2-211"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-212">控制識別碼。</span><span class="sxs-lookup"><span data-stu-id="425a2-212">Control identifier.</span></span> <span data-ttu-id="425a2-213">如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-213">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="edit-control-statements"></a><span data-ttu-id="425a2-214">編輯控制語句</span><span class="sxs-lookup"><span data-stu-id="425a2-214">Edit Control Statements</span></span>

``` syntax
editClass id
```

<dl> <dt>

<span data-ttu-id="425a2-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span><span class="sxs-lookup"><span data-stu-id="425a2-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-216">**EDITTEXT**、 **BEDIT**、 **HEDIT** 或 **IEDIT**。</span><span class="sxs-lookup"><span data-stu-id="425a2-216">**EDITTEXT**, **BEDIT**, **HEDIT**, or **IEDIT**.</span></span>

</dd> <dt>

<span data-ttu-id="425a2-217"><span id="id"></span><span id="ID"></span>*Id*</span><span class="sxs-lookup"><span data-stu-id="425a2-217"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="425a2-218">控制識別碼。</span><span class="sxs-lookup"><span data-stu-id="425a2-218">Control identifier.</span></span> <span data-ttu-id="425a2-219">如需詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="425a2-219">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="425a2-220">另請參閱</span><span class="sxs-lookup"><span data-stu-id="425a2-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425a2-221">使用對話方塊</span><span class="sxs-lookup"><span data-stu-id="425a2-221">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="425a2-222">**加速器**</span><span class="sxs-lookup"><span data-stu-id="425a2-222">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="425a2-223">**特徵**</span><span class="sxs-lookup"><span data-stu-id="425a2-223">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="425a2-224">**控制**</span><span class="sxs-lookup"><span data-stu-id="425a2-224">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="425a2-225">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="425a2-225">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="425a2-226">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="425a2-226">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="425a2-227">**對話方塊**</span><span class="sxs-lookup"><span data-stu-id="425a2-227">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="425a2-228">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="425a2-228">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="425a2-229">**語言**</span><span class="sxs-lookup"><span data-stu-id="425a2-229">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="425a2-230">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="425a2-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="425a2-231">功能表</span><span class="sxs-lookup"><span data-stu-id="425a2-231">MENU</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="425a2-232">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="425a2-232">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="425a2-233">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="425a2-233">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="425a2-234">**版本**</span><span class="sxs-lookup"><span data-stu-id="425a2-234">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
