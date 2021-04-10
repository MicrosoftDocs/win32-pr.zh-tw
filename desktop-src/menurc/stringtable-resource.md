---
title: STRINGTABLE 資源
description: 定義應用程式的一或多個字串資源。 字串資源就是以 null 結束的 Unicode 或 ASCII 字串，可在需要時從可執行檔載入，使用 Loadstring 時函數。
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- STRINGTABLE 資源功能表與其他資源
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092725"
---
# <a name="stringtable-resource"></a><span data-ttu-id="f480d-105">STRINGTABLE 資源</span><span class="sxs-lookup"><span data-stu-id="f480d-105">STRINGTABLE resource</span></span>

<span data-ttu-id="f480d-106">定義應用程式的一或多個字串資源。</span><span class="sxs-lookup"><span data-stu-id="f480d-106">Defines one or more string resources for an application.</span></span> <span data-ttu-id="f480d-107">字串資源就是以 null 結束的 Unicode 或 ASCII 字串，可在需要時從可執行檔載入，使用 [**loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa) 函數。</span><span class="sxs-lookup"><span data-stu-id="f480d-107">String resources are simply null-terminated Unicode or ASCII strings that can be loaded when needed from the executable file, using the [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) function.</span></span>

<span data-ttu-id="f480d-108">有兩種方式可將 **STRINGTABLE** 語句格式化：</span><span class="sxs-lookup"><span data-stu-id="f480d-108">There are two ways to format a **STRINGTABLE** statement:</span></span>

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

<span data-ttu-id="f480d-109">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="f480d-109">\- or -</span></span>

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="f480d-110">參數</span><span class="sxs-lookup"><span data-stu-id="f480d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f480d-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*</span><span class="sxs-lookup"><span data-stu-id="f480d-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="f480d-112">這個參數可以是零或多個下列語句。</span><span class="sxs-lookup"><span data-stu-id="f480d-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="f480d-113">陳述式</span><span class="sxs-lookup"><span data-stu-id="f480d-113">Statement</span></span>                                                        | <span data-ttu-id="f480d-114">描述</span><span class="sxs-lookup"><span data-stu-id="f480d-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f480d-115">[**特性**](characteristics-statement.md) *dword*</span><span class="sxs-lookup"><span data-stu-id="f480d-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="f480d-116">有關可供讀取和寫入資源檔的工具使用之資源的使用者定義資訊。</span><span class="sxs-lookup"><span data-stu-id="f480d-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="f480d-117">如需詳細資訊，請參閱 [**特性**](characteristics-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="f480d-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="f480d-118">[**語言**](language-statement.md)*語言*、*語言*</span><span class="sxs-lookup"><span data-stu-id="f480d-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="f480d-119">指定資源的語言。</span><span class="sxs-lookup"><span data-stu-id="f480d-119">Specifies the language for the resource.</span></span> <span data-ttu-id="f480d-120">如需詳細資訊，請參閱 [**語言**](language-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="f480d-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="f480d-121">[**版本**](version-statement.md) *dword*</span><span class="sxs-lookup"><span data-stu-id="f480d-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="f480d-122">資源的使用者定義版本號碼，可供讀取和寫入資源檔的工具使用。</span><span class="sxs-lookup"><span data-stu-id="f480d-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="f480d-123">如需詳細資訊，請參閱 [**版本**](version-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="f480d-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="f480d-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*Stringid 指定*</span><span class="sxs-lookup"><span data-stu-id="f480d-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span></span>
</dt> <dd>

<span data-ttu-id="f480d-125">識別資源的不帶正負號16位整數。</span><span class="sxs-lookup"><span data-stu-id="f480d-125">Unsigned 16-bit integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f480d-126"><span id="string"></span><span id="STRING"></span>*字串*</span><span class="sxs-lookup"><span data-stu-id="f480d-126"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="f480d-127">以引號括住的一或多個字串。</span><span class="sxs-lookup"><span data-stu-id="f480d-127">One or more strings, enclosed in quotation marks.</span></span> <span data-ttu-id="f480d-128">字串不能超過4097個字元，而且必須在原始程式檔中佔用一行。</span><span class="sxs-lookup"><span data-stu-id="f480d-128">The string must be no longer than 4097 characters and must occupy a single line in the source file.</span></span> <span data-ttu-id="f480d-129">若要將換行字元加入字串，請使用此字元序列： \\ 012。</span><span class="sxs-lookup"><span data-stu-id="f480d-129">To add a carriage return to the string, use this character sequence: \\012.</span></span> <span data-ttu-id="f480d-130">例如，"Line one \\ 012Line 二" 會定義如下所示的字串：</span><span class="sxs-lookup"><span data-stu-id="f480d-130">For example, "Line one\\012Line two" defines a string that is displayed as follows:</span></span>

``` syntax
Line one
Line two
```

<span data-ttu-id="f480d-131">若要在字串中內嵌引號，請使用下列順序： ""。</span><span class="sxs-lookup"><span data-stu-id="f480d-131">To embed quotes in the string, use the following sequence: "".</span></span> <span data-ttu-id="f480d-132">例如，"" "第三行" "" 會定義如下所示的字串：</span><span class="sxs-lookup"><span data-stu-id="f480d-132">For example, """Line three""" defines a string that is displayed as follows:</span></span>

``` syntax
"Line three"
```

<span data-ttu-id="f480d-133">若要將 Unicode 字元編碼，請使用 "L"，後面接著以引號括住的 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="f480d-133">To encode Unicode characters, use an "L" followed by the Unicode characters enclosed by quotes.</span></span> <span data-ttu-id="f480d-134">如需範例，請參閱範例一節。</span><span class="sxs-lookup"><span data-stu-id="f480d-134">See the Examples section for an example.</span></span>

<span data-ttu-id="f480d-135">資源編譯器也支援 *字串* 中的行接續。</span><span class="sxs-lookup"><span data-stu-id="f480d-135">The resource compiler also supports line continuations in *string*.</span></span> <span data-ttu-id="f480d-136">如需範例，請參閱範例一節。</span><span class="sxs-lookup"><span data-stu-id="f480d-136">See the Examples section for an example.</span></span>

</dd> </dl>

<span data-ttu-id="f480d-137">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="f480d-137">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="f480d-138">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="f480d-138">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f480d-139">備註</span><span class="sxs-lookup"><span data-stu-id="f480d-139">Remarks</span></span>

<span data-ttu-id="f480d-140">RC 會為每個區段配置16個字串，並使用識別碼值來判斷要包含字串的區段。</span><span class="sxs-lookup"><span data-stu-id="f480d-140">RC allocates 16 strings per section and uses the identifier value to determine which section is to contain the string.</span></span> <span data-ttu-id="f480d-141">識別碼不同于底部4位的字串會放置在相同的區段中。</span><span class="sxs-lookup"><span data-stu-id="f480d-141">Strings whose identifiers differ only in the bottom 4 bits are placed in the same section.</span></span> <span data-ttu-id="f480d-142">如需詳細資訊，請參閱 [Q196774](https://support.microsoft.com/kb/196774)。</span><span class="sxs-lookup"><span data-stu-id="f480d-142">For more information, see [Q196774](https://support.microsoft.com/kb/196774).</span></span>

## <a name="examples"></a><span data-ttu-id="f480d-143">範例</span><span class="sxs-lookup"><span data-stu-id="f480d-143">Examples</span></span>

<span data-ttu-id="f480d-144">下列範例示範如何使用 **STRINGTABLE** 語句來顯示 ASCII 字串：</span><span class="sxs-lookup"><span data-stu-id="f480d-144">The following example demonstrates the use of the **STRINGTABLE** statement to display ASCII strings:</span></span>

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

<span data-ttu-id="f480d-145">下列範例顯示如何編碼 Unicode 字元：</span><span class="sxs-lookup"><span data-stu-id="f480d-145">The following example shows how to encode Unicode characters:</span></span>

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

<span data-ttu-id="f480d-146">下列範例會顯示具有 ASCII 和 Unicode 的字串。</span><span class="sxs-lookup"><span data-stu-id="f480d-146">The following example shows strings with both ASCII and Unicode.</span></span> <span data-ttu-id="f480d-147">請注意，沒有初始 "L" 的字串會使用2位數的 escape 格式：</span><span class="sxs-lookup"><span data-stu-id="f480d-147">Note that strings without the initial "L" use the 2-digit escape format:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

<span data-ttu-id="f480d-148">下列範例會顯示如何使用行接續：</span><span class="sxs-lookup"><span data-stu-id="f480d-148">The following example shows how line continuations can be used:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a><span data-ttu-id="f480d-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f480d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f480d-150">**Loadstring 時**</span><span class="sxs-lookup"><span data-stu-id="f480d-150">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[<span data-ttu-id="f480d-151">**加速器**</span><span class="sxs-lookup"><span data-stu-id="f480d-151">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="f480d-152">**特徵**</span><span class="sxs-lookup"><span data-stu-id="f480d-152">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="f480d-153">**語言**</span><span class="sxs-lookup"><span data-stu-id="f480d-153">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="f480d-154">**功能表**</span><span class="sxs-lookup"><span data-stu-id="f480d-154">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="f480d-155">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="f480d-155">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="f480d-156">**版本**</span><span class="sxs-lookup"><span data-stu-id="f480d-156">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 