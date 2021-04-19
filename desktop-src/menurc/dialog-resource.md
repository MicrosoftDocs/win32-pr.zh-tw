---
title: 對話方塊資源
description: 定義對話方塊。 |對話方塊資源
ms.assetid: d166fb7d-0fe5-4e48-a545-19acc0ff80f1
keywords:
- 對話方塊資源功能表與其他資源
topic_type:
- apiref
api_name:
- DIALOG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7a1aef314406340c42c6a4aca40b76f91ac353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997335"
---
# <a name="dialog-resource"></a><span data-ttu-id="7b8ce-105">對話方塊資源</span><span class="sxs-lookup"><span data-stu-id="7b8ce-105">DIALOG resource</span></span>

<span data-ttu-id="7b8ce-106">定義對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-106">Defines a dialog box.</span></span> <span data-ttu-id="7b8ce-107">語句會定義畫面上對話方塊的位置和維度，以及對話方塊的樣式。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span>

> [!Note]  
> <span data-ttu-id="7b8ce-108">**對話方塊** 是過時的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-108">**DIALOG** is an obsolete resource ID.</span></span> <span data-ttu-id="7b8ce-109">新的應用程式應該使用 [**DIALOGEX**](dialogex-resource.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-109">New applications should use [**DIALOGEX**](dialogex-resource.md).</span></span>

 

``` syntax
nameID DIALOG x, y, width, height  [optional-statements] {control-statement  . . . }
```

## <a name="parameters"></a><span data-ttu-id="7b8ce-110">參數</span><span class="sxs-lookup"><span data-stu-id="7b8ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b8ce-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="7b8ce-111"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="7b8ce-112">識別對話方塊的唯一名稱或唯一的16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-112">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="7b8ce-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*</span><span class="sxs-lookup"><span data-stu-id="7b8ce-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="7b8ce-114">對話方塊的選項。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-114">Options for the dialog box.</span></span> <span data-ttu-id="7b8ce-115">這可以是零或多個下列語句。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-115">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="7b8ce-116">陳述式</span><span class="sxs-lookup"><span data-stu-id="7b8ce-116">Statement</span></span>                                                        | <span data-ttu-id="7b8ce-117">描述</span><span class="sxs-lookup"><span data-stu-id="7b8ce-117">Description</span></span>                                                                                                                                                                                  |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b8ce-118">[**標題**](caption-statement.md) "*text*"</span><span class="sxs-lookup"><span data-stu-id="7b8ce-118">[**CAPTION**](caption-statement.md) "*text*"</span></span>                    | <span data-ttu-id="7b8ce-119">對話方塊的標題列（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-119">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="7b8ce-120">如需詳細資訊，請參閱 [**標題**](caption-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-120">For more information, see [**CAPTION**](caption-statement.md).</span></span>                                                                             |
| <span data-ttu-id="7b8ce-121">[**特性**](characteristics-statement.md) *dword*</span><span class="sxs-lookup"><span data-stu-id="7b8ce-121">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="7b8ce-122">資源工具所使用的使用者定義 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-122">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="7b8ce-123">系統不會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-123">This value is not used by the system.</span></span> <span data-ttu-id="7b8ce-124">如需詳細資訊，請參閱 [**特性**](characteristics-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-124">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span>                |
| <span data-ttu-id="7b8ce-125">[**類別**](class-statement.md)*類別*</span><span class="sxs-lookup"><span data-stu-id="7b8ce-125">[**CLASS**](class-statement.md) *class*</span></span>                         | <span data-ttu-id="7b8ce-126">以雙引號括住的16位不帶正負號的整數或字串 ( ") ，以識別對話方塊的類別。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-126">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="7b8ce-127">如需詳細資訊，請參閱 [**類別**](class-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-127">For more information, see [**CLASS**](class-statement.md).</span></span>      |
| <span data-ttu-id="7b8ce-128">**EXSTYLE =** *擴充樣式*</span><span class="sxs-lookup"><span data-stu-id="7b8ce-128">**EXSTYLE=** *extended-styles*</span></span>                                   | <span data-ttu-id="7b8ce-129">對話方塊的擴充視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-129">Extended window style of the dialog box.</span></span> <span data-ttu-id="7b8ce-130">如需詳細資訊，請參閱 [**EXSTYLE**](exstyle-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-130">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>                                                                                     |
| <span data-ttu-id="7b8ce-131">**字型** *dialog*、 *字型*</span><span class="sxs-lookup"><span data-stu-id="7b8ce-131">**FONT** *pointsize*, *typeface*</span></span>                                 | <span data-ttu-id="7b8ce-132">字型的點大小和字型。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-132">Point size and typeface for the font.</span></span> <span data-ttu-id="7b8ce-133">如需詳細資訊，請參閱 [**字型**](font-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-133">For more information, see [**FONT**](font-statement.md).</span></span>                                                                                              |
| <span data-ttu-id="7b8ce-134">[**語言**](language-statement.md)*語言*、*語言*</span><span class="sxs-lookup"><span data-stu-id="7b8ce-134">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="7b8ce-135">對話方塊的語言。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-135">Language of the dialog box.</span></span> <span data-ttu-id="7b8ce-136">如需詳細資訊，請參閱 [**語言**](language-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-136">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                                |
| <span data-ttu-id="7b8ce-137">**功能表** *menuname*</span><span class="sxs-lookup"><span data-stu-id="7b8ce-137">**MENU** *menuname*</span></span>                                              | <span data-ttu-id="7b8ce-138">要使用的功能表。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-138">Menu to be used.</span></span> <span data-ttu-id="7b8ce-139">此值為功能表的名稱或其整數識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-139">This value is either the name of the menu or its integer identifier.</span></span>                                                                                                        |
| <span data-ttu-id="7b8ce-140">[**樣式**](style-statement.md)*樣式*</span><span class="sxs-lookup"><span data-stu-id="7b8ce-140">[**STYLE**](style-statement.md) *styles*</span></span>                        | <span data-ttu-id="7b8ce-141">對話方塊的樣式。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-141">Styles of the dialog box.</span></span> <span data-ttu-id="7b8ce-142">如需詳細資訊，請參閱 [**樣式**](style-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-142">For more information, see [**STYLE**](style-statement.md).</span></span>                                                                                                        |
| <span data-ttu-id="7b8ce-143">[**版本**](version-statement.md) *dword*</span><span class="sxs-lookup"><span data-stu-id="7b8ce-143">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="7b8ce-144">使用者定義的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-144">User-defined **DWORD** value.</span></span> <span data-ttu-id="7b8ce-145">此語句適用于其他資源工具，而且系統不會使用此語句。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-145">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="7b8ce-146">如需詳細資訊，請參閱 [**版本**](version-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-146">For more information, see [**VERSION**](version-statement.md).</span></span> |



 

</dd> </dl>

<span data-ttu-id="7b8ce-147">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-147">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="7b8ce-148">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-148">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b8ce-149">備註</span><span class="sxs-lookup"><span data-stu-id="7b8ce-149">Remarks</span></span>

<span data-ttu-id="7b8ce-150">[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)函式會傳回對話方塊基礎單位（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-150">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="7b8ce-151">座標的確切意義取決於 [**style**](style-statement.md) option 語句所定義的樣式。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-151">The exact meaning of the coordinates depends on the style defined by the [**STYLE**](style-statement.md) option statement.</span></span> <span data-ttu-id="7b8ce-152">針對子樣式對話方塊，除非對話方塊的樣式為 **DS \_ ABSALIGN**，否則座標會相對於父視窗的原點，而在此情況下，座標是相對於顯示畫面的原點。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-152">For child-style dialog boxes, the coordinates are relative to the origin of the parent window, unless the dialog box has the style **DS\_ABSALIGN**; in that case, the coordinates are relative to the origin of the display screen.</span></span>

<span data-ttu-id="7b8ce-153">請勿使用 **WS \_ 子** 樣式搭配強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-153">Do not use the **WS\_CHILD** style with a modal dialog box.</span></span> <span data-ttu-id="7b8ce-154">[**對話方塊**](/windows/win32/api/winuser/nf-winuser-dialogboxa)函式一律會停用新建立之對話方塊的父/擁有者。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-154">The [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function always disables the parent/owner of the newly created dialog box.</span></span> <span data-ttu-id="7b8ce-155">停用父視窗時，會隱含停用其子視窗。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-155">When a parent window is disabled, its child windows are implicitly disabled.</span></span> <span data-ttu-id="7b8ce-156">由於子樣式對話方塊的父視窗已停用，因此子樣式對話方塊也是如此。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-156">Since the parent window of the child-style dialog box is disabled, the child-style dialog box is too.</span></span>

<span data-ttu-id="7b8ce-157">如果對話方塊具有 **DS \_ ABSALIGN** 樣式，則其左上角的對話座標是相對於螢幕原點，而不是父視窗的左上角。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-157">If a dialog box has the **DS\_ABSALIGN** style, the dialog coordinates for its upper-left corner are relative to the screen origin instead of to the upper-left corner of the parent window.</span></span> <span data-ttu-id="7b8ce-158">當您希望對話方塊在顯示的特定部分中啟動時，您通常會使用這種樣式，不論父視窗在螢幕上的哪個位置。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-158">You would typically use this style when you wanted the dialog box to start in a specific part of the display no matter where the parent window may be on the screen.</span></span>

<span data-ttu-id="7b8ce-159">[名稱 **] 對話方塊** 也可以當做 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 函式的類別名稱參數，用來建立具有對話方塊屬性的視窗。</span><span class="sxs-lookup"><span data-stu-id="7b8ce-159">The name **DIALOG** can also be used as the class-name parameter to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function to create a window with dialog-box attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="7b8ce-160">範例</span><span class="sxs-lookup"><span data-stu-id="7b8ce-160">Examples</span></span>

<span data-ttu-id="7b8ce-161">以下示範 **DIALOG** 語句的用法：</span><span class="sxs-lookup"><span data-stu-id="7b8ce-161">The following demonstrates the usage of the **DIALOG** statement:</span></span>

``` syntax
#include <windows.h>

ErrorDialog DIALOG  10, 10, 300, 110
STYLE WS_POPUP | WS_BORDER
CAPTION "Error!" 
{
    CTEXT "Select One:", 1, 10, 10, 280, 12
    PUSHBUTTON "&Retry", 2, 75, 30, 60, 12
    PUSHBUTTON "&Abort", 3, 75, 50, 60, 12
    PUSHBUTTON "&Ignore", 4, 75, 80, 60, 12
}
```

## <a name="see-also"></a><span data-ttu-id="7b8ce-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b8ce-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b8ce-163">使用對話方塊</span><span class="sxs-lookup"><span data-stu-id="7b8ce-163">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="7b8ce-164">**加速器**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-164">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="7b8ce-165">**特徵**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-165">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="7b8ce-166">**控制**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-166">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="7b8ce-167">**CreateDialog**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-167">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="7b8ce-168">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-168">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="7b8ce-169">**對話方塊**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-169">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="7b8ce-170">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-170">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="7b8ce-171">**語言**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-171">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="7b8ce-172">**功能表**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-172">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="7b8ce-173">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-173">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="7b8ce-174">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-174">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="7b8ce-175">**版本**</span><span class="sxs-lookup"><span data-stu-id="7b8ce-175">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
