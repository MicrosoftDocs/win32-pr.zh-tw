---
title: 加速器資源
description: 定義應用程式的一個或多個加速器。 加速器是應用程式所定義的按鍵，可讓使用者快速地執行工作。
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- 加速器資源功能表與其他資源
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507891"
---
# <a name="accelerators-resource"></a><span data-ttu-id="3d647-105">加速器資源</span><span class="sxs-lookup"><span data-stu-id="3d647-105">ACCELERATORS resource</span></span>

<span data-ttu-id="3d647-106">定義應用程式的一個或多個加速器。</span><span class="sxs-lookup"><span data-stu-id="3d647-106">Defines one or more accelerators for an application.</span></span> <span data-ttu-id="3d647-107">加速器是應用程式所定義的按鍵，可讓使用者快速地執行工作。</span><span class="sxs-lookup"><span data-stu-id="3d647-107">An accelerator is a keystroke defined by the application to give the user a quick way to perform a task.</span></span>

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a><span data-ttu-id="3d647-108">參數</span><span class="sxs-lookup"><span data-stu-id="3d647-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d647-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span><span class="sxs-lookup"><span data-stu-id="3d647-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span></span>
</dt> <dd>

<span data-ttu-id="3d647-110">識別資源的唯一名稱或16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="3d647-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="3d647-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*</span><span class="sxs-lookup"><span data-stu-id="3d647-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="3d647-112">下列零或多個語句。</span><span class="sxs-lookup"><span data-stu-id="3d647-112">Zero or more of the following statements.</span></span>



| <span data-ttu-id="3d647-113">陳述式</span><span class="sxs-lookup"><span data-stu-id="3d647-113">Statement</span></span>                                                        | <span data-ttu-id="3d647-114">描述</span><span class="sxs-lookup"><span data-stu-id="3d647-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d647-115">[**特性**](characteristics-statement.md) *dword*</span><span class="sxs-lookup"><span data-stu-id="3d647-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="3d647-116">有關可供讀取和寫入資源檔的工具使用之資源的使用者定義資訊。</span><span class="sxs-lookup"><span data-stu-id="3d647-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="3d647-117">如需詳細資訊，請參閱 [**特性**](characteristics-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d647-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="3d647-118">[**語言**](language-statement.md)*語言*、*語言*</span><span class="sxs-lookup"><span data-stu-id="3d647-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="3d647-119">指定資源的語言。</span><span class="sxs-lookup"><span data-stu-id="3d647-119">Specifies the language for the resource.</span></span> <span data-ttu-id="3d647-120">如需詳細資訊，請參閱 [**語言**](language-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d647-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="3d647-121">[**版本**](version-statement.md) *dword*</span><span class="sxs-lookup"><span data-stu-id="3d647-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="3d647-122">資源的使用者定義版本號碼，可供讀取和寫入資源檔的工具使用。</span><span class="sxs-lookup"><span data-stu-id="3d647-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="3d647-123">如需詳細資訊，請參閱 [**版本**](version-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="3d647-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="3d647-124"><span id="event"></span><span id="EVENT"></span>*事件*</span><span class="sxs-lookup"><span data-stu-id="3d647-124"><span id="event"></span><span id="EVENT"></span>*event*</span></span>
</dt> <dd>

<span data-ttu-id="3d647-125">要作為加速器使用的按鍵。</span><span class="sxs-lookup"><span data-stu-id="3d647-125">Keystroke to be used as an accelerator.</span></span> <span data-ttu-id="3d647-126">它可以是下列任何一個字元類型。</span><span class="sxs-lookup"><span data-stu-id="3d647-126">It can be any one of the following character types.</span></span>



| <span data-ttu-id="3d647-127">類型</span><span class="sxs-lookup"><span data-stu-id="3d647-127">Type</span></span>                    | <span data-ttu-id="3d647-128">Description</span><span class="sxs-lookup"><span data-stu-id="3d647-128">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d647-129">"*char*"</span><span class="sxs-lookup"><span data-stu-id="3d647-129">"*char*"</span></span>                | <span data-ttu-id="3d647-130">用雙引號括住的單一字元 ( ") 。</span><span class="sxs-lookup"><span data-stu-id="3d647-130">A single character enclosed in double quotation marks (").</span></span> <span data-ttu-id="3d647-131">字元前面可以加上插入號 (^) ，表示字元是控制字元。</span><span class="sxs-lookup"><span data-stu-id="3d647-131">The character can be preceded by a caret (^), meaning that the character is a control character.</span></span>                                                                                  |
| <span data-ttu-id="3d647-132">*字元*</span><span class="sxs-lookup"><span data-stu-id="3d647-132">*Character*</span></span>             | <span data-ttu-id="3d647-133">代表字元的整數值。</span><span class="sxs-lookup"><span data-stu-id="3d647-133">An integer value representing a character.</span></span> <span data-ttu-id="3d647-134">*型* 別參數必須是 **ASCII**。</span><span class="sxs-lookup"><span data-stu-id="3d647-134">The *type* parameter must be **ASCII**.</span></span>                                                                                                                                                           |
| <span data-ttu-id="3d647-135">*虛擬機器碼字元*</span><span class="sxs-lookup"><span data-stu-id="3d647-135">*virtual-key character*</span></span> | <span data-ttu-id="3d647-136">代表虛擬機器碼的整數值。</span><span class="sxs-lookup"><span data-stu-id="3d647-136">An integer value representing a virtual key.</span></span> <span data-ttu-id="3d647-137">您可以藉由在雙引號中放置大寫字母或數位來指定英數位元的虛擬機器碼 (例如 "9" 或 "C" ) 。</span><span class="sxs-lookup"><span data-stu-id="3d647-137">The virtual key for alphanumeric keys can be specified by placing the uppercase letter or number in double quotation marks (for example, "9" or "C").</span></span> <span data-ttu-id="3d647-138">*型* 別參數必須是 **VIRTKEY**。</span><span class="sxs-lookup"><span data-stu-id="3d647-138">The *type* parameter must be **VIRTKEY**.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3d647-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span><span class="sxs-lookup"><span data-stu-id="3d647-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span></span>
</dt> <dd>

<span data-ttu-id="3d647-140">識別快速鍵的16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="3d647-140">a 16-bit unsigned integer value that identifies the accelerator.</span></span>

</dd> <dt>

<span data-ttu-id="3d647-141"><span id="type"></span><span id="TYPE"></span>*類型*</span><span class="sxs-lookup"><span data-stu-id="3d647-141"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="3d647-142">只有當 *事件* 參數是 *字元* 或 *虛擬金鑰字元* 時才需要。</span><span class="sxs-lookup"><span data-stu-id="3d647-142">Required only when the *event* parameter is a *character* or a *virtual-key character*.</span></span> <span data-ttu-id="3d647-143">*類型* 參數會指定 **ASCII** 或 **VIRTKEY**;*事件* 的整數值會據以解讀。</span><span class="sxs-lookup"><span data-stu-id="3d647-143">The *type* parameter specifies either **ASCII** or **VIRTKEY**; the integer value of *event* is interpreted accordingly.</span></span> <span data-ttu-id="3d647-144">當指定 **VIRTKEY** 且 *事件* 包含字串時， *事件* 必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="3d647-144">When **VIRTKEY** is specified and *event* contains a string, *event* must be uppercase.</span></span>

</dd> <dt>

<span data-ttu-id="3d647-145"><span id="options"></span><span id="OPTIONS"></span>*選項*</span><span class="sxs-lookup"><span data-stu-id="3d647-145"><span id="options"></span><span id="OPTIONS"></span>*options*</span></span>
</dt> <dd>

<span data-ttu-id="3d647-146">定義加速器的選項。</span><span class="sxs-lookup"><span data-stu-id="3d647-146">options that define the accelerator.</span></span> <span data-ttu-id="3d647-147">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="3d647-147">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3d647-148">選項</span><span class="sxs-lookup"><span data-stu-id="3d647-148">Option</span></span>                             | <span data-ttu-id="3d647-149">Description</span><span class="sxs-lookup"><span data-stu-id="3d647-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d647-150">**NOINVERT**</span><span class="sxs-lookup"><span data-stu-id="3d647-150">**NOINVERT**</span></span>                       | <span data-ttu-id="3d647-151">指定使用快速鍵時，不會反白顯示最上層功能表項目。</span><span class="sxs-lookup"><span data-stu-id="3d647-151">Specifies that no top-level menu item is highlighted when the accelerator is used.</span></span> <span data-ttu-id="3d647-152">當您針對未對應至功能表項目的動作定義快速鍵時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="3d647-152">This is useful when defining accelerators for actions such as scrolling that do not correspond to a menu item.</span></span> <span data-ttu-id="3d647-153">如果省略 **NOINVERT** ，當使用快速鍵時，最上層的功能表項目會反白顯示 (可能的) 。</span><span class="sxs-lookup"><span data-stu-id="3d647-153">If **NOINVERT** is omitted, a top-level menu item will be highlighted (if possible) when the accelerator is used.</span></span> <span data-ttu-id="3d647-154">這個屬性已過時，而且只是為了與針對16位 Windows 設計的資源檔回溯相容。</span><span class="sxs-lookup"><span data-stu-id="3d647-154">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span> |
| <span data-ttu-id="3d647-155">**ALT**</span><span class="sxs-lookup"><span data-stu-id="3d647-155">**ALT**</span></span>                            | <span data-ttu-id="3d647-156">只有在 ALT 鍵關閉時，才會啟用快速鍵。</span><span class="sxs-lookup"><span data-stu-id="3d647-156">Causes the accelerator to be activated only if the ALT key is down.</span></span> <span data-ttu-id="3d647-157">只適用于虛擬機器碼。</span><span class="sxs-lookup"><span data-stu-id="3d647-157">Applies only to virtual keys.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="3d647-158">**轉變**</span><span class="sxs-lookup"><span data-stu-id="3d647-158">**SHIFT**</span></span>                          | <span data-ttu-id="3d647-159">只有在 SHIFT 鍵已關閉時，才會啟用快速鍵。</span><span class="sxs-lookup"><span data-stu-id="3d647-159">Causes the accelerator to be activated only if the SHIFT key is down.</span></span> <span data-ttu-id="3d647-160">僅適用于虛擬機器碼</span><span class="sxs-lookup"><span data-stu-id="3d647-160">Applies only to virtual keys</span></span>                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="3d647-161">**控制**</span><span class="sxs-lookup"><span data-stu-id="3d647-161">**CONTROL**</span></span>](control-control.md) | <span data-ttu-id="3d647-162">將字元定義為控制字元 (只有在控制項索引鍵) 關閉時，才會啟用快速鍵。</span><span class="sxs-lookup"><span data-stu-id="3d647-162">Defines the character as a control character (the accelerator is only activated if the CONTROL key is down).</span></span> <span data-ttu-id="3d647-163">這與使用插入號 (^) 在 *事件* 參數中的快速鍵之前，會有相同的效果。</span><span class="sxs-lookup"><span data-stu-id="3d647-163">This has the same effect as using a caret (^) before the accelerator character in the *event* parameter.</span></span> <span data-ttu-id="3d647-164">僅適用于虛擬機器碼</span><span class="sxs-lookup"><span data-stu-id="3d647-164">Applies only to virtual keys</span></span>                                                                                                                                                                                           |



 

</dd> </dl>

<span data-ttu-id="3d647-165">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="3d647-165">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="3d647-166">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="3d647-166">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d647-167">備註</span><span class="sxs-lookup"><span data-stu-id="3d647-167">Remarks</span></span>

<span data-ttu-id="3d647-168">[**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)函式可用來將應用程式佇列中的加速器訊息轉譯為 [**Wm \_ 命令**](./wm-command.md)或 [**wm \_ SYSCOMMAND**](./wm-syscommand.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="3d647-168">The [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function is used to translate accelerator messages from the application queue into [**WM\_COMMAND**](./wm-command.md) or [**WM\_SYSCOMMAND**](./wm-syscommand.md) messages.</span></span>

## <a name="examples"></a><span data-ttu-id="3d647-169">範例</span><span class="sxs-lookup"><span data-stu-id="3d647-169">Examples</span></span>

<span data-ttu-id="3d647-170">下列範例示範快速鍵的使用。</span><span class="sxs-lookup"><span data-stu-id="3d647-170">The following example demonstrates the use of accelerator keys.</span></span>

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a><span data-ttu-id="3d647-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d647-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d647-172">使用鍵盤加速器</span><span class="sxs-lookup"><span data-stu-id="3d647-172">Using Keyboard Accelerators</span></span>](./using-keyboard-accelerators.md)
</dt> <dt>

[<span data-ttu-id="3d647-173">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="3d647-173">**TranslateAccelerator**</span></span>](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="3d647-174">**特徵**</span><span class="sxs-lookup"><span data-stu-id="3d647-174">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="3d647-175">**對話 框**</span><span class="sxs-lookup"><span data-stu-id="3d647-175">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="3d647-176">**語言**</span><span class="sxs-lookup"><span data-stu-id="3d647-176">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="3d647-177">**功能表**</span><span class="sxs-lookup"><span data-stu-id="3d647-177">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="3d647-178">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="3d647-178">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="3d647-179">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="3d647-179">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="3d647-180">**版本**</span><span class="sxs-lookup"><span data-stu-id="3d647-180">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 