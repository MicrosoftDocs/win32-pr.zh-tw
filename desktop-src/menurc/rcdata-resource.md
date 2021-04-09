---
title: RCDATA 資源
description: 定義應用程式的原始資料資源。 原始資料資源允許直接在可執行檔中包含二進位資料。
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- RCDATA 資源功能表與其他資源
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932748"
---
# <a name="rcdata-resource"></a><span data-ttu-id="d30cf-105">RCDATA 資源</span><span class="sxs-lookup"><span data-stu-id="d30cf-105">RCDATA resource</span></span>

<span data-ttu-id="d30cf-106">定義應用程式的原始資料資源。</span><span class="sxs-lookup"><span data-stu-id="d30cf-106">Defines a raw data resource for an application.</span></span> <span data-ttu-id="d30cf-107">原始資料資源允許直接在可執行檔中包含二進位資料。</span><span class="sxs-lookup"><span data-stu-id="d30cf-107">Raw data resources permit the inclusion of binary data directly in the executable file.</span></span>

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a><span data-ttu-id="d30cf-108">參數</span><span class="sxs-lookup"><span data-stu-id="d30cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d30cf-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="d30cf-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="d30cf-110">識別資源的唯一名稱或16位不帶正負號的整數值。</span><span class="sxs-lookup"><span data-stu-id="d30cf-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="d30cf-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*</span><span class="sxs-lookup"><span data-stu-id="d30cf-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="d30cf-112">這個參數可以是零或多個下列語句。</span><span class="sxs-lookup"><span data-stu-id="d30cf-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="d30cf-113">陳述式</span><span class="sxs-lookup"><span data-stu-id="d30cf-113">Statement</span></span>                                                        | <span data-ttu-id="d30cf-114">描述</span><span class="sxs-lookup"><span data-stu-id="d30cf-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d30cf-115">[**特性**](characteristics-statement.md) *dword*</span><span class="sxs-lookup"><span data-stu-id="d30cf-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="d30cf-116">有關可供讀取和寫入資源檔的工具使用之資源的使用者定義資訊。</span><span class="sxs-lookup"><span data-stu-id="d30cf-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="d30cf-117">如需詳細資訊，請參閱 [**特性**](characteristics-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="d30cf-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="d30cf-118">[**語言**](language-statement.md)*語言*、*語言*</span><span class="sxs-lookup"><span data-stu-id="d30cf-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="d30cf-119">資源的語言。</span><span class="sxs-lookup"><span data-stu-id="d30cf-119">Language for the resource.</span></span> <span data-ttu-id="d30cf-120">如需詳細資訊，請參閱 [**語言**](language-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="d30cf-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="d30cf-121">[**版本**](version-statement.md) *dword*</span><span class="sxs-lookup"><span data-stu-id="d30cf-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="d30cf-122">資源的使用者定義版本號碼，可供讀取和寫入資源檔的工具使用。</span><span class="sxs-lookup"><span data-stu-id="d30cf-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="d30cf-123">如需詳細資訊，請參閱 [**版本**](version-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="d30cf-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="d30cf-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*原始資料*</span><span class="sxs-lookup"><span data-stu-id="d30cf-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="d30cf-125">由一或多個整數或字元字串所組成的原始資料。</span><span class="sxs-lookup"><span data-stu-id="d30cf-125">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="d30cf-126">您可以用十進位、八進位或十六進位格式來指定整數。</span><span class="sxs-lookup"><span data-stu-id="d30cf-126">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="d30cf-127">為了與16位 Windows 相容，整數會儲存為 **文字** 值。</span><span class="sxs-lookup"><span data-stu-id="d30cf-127">To be compatible with 16-bit Windows, integers are stored as **WORD** values.</span></span> <span data-ttu-id="d30cf-128">您可以使用 "L" 尾碼來限定整數，以將整數儲存為 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="d30cf-128">You can store an integer as a **DWORD** value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="d30cf-129">字串會以引號括住。</span><span class="sxs-lookup"><span data-stu-id="d30cf-129">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="d30cf-130">RC 不會自動將終止的 null 字元附加至字串。</span><span class="sxs-lookup"><span data-stu-id="d30cf-130">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="d30cf-131">每個字串都是指定之 ANSI 字元的序列，除非您將它限定為具有 L 前置詞的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="d30cf-131">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the L prefix.</span></span>

<span data-ttu-id="d30cf-132">資料區塊開始于 **DWORD** 界限，而 RC 不會在 *原始資料* 區塊內執行資料的填補或對齊。</span><span class="sxs-lookup"><span data-stu-id="d30cf-132">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="d30cf-133">您必須負責確保區塊內適當的資料對齊。</span><span class="sxs-lookup"><span data-stu-id="d30cf-133">It is your responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

<span data-ttu-id="d30cf-134">此外，也支援某些屬性以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="d30cf-134">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="d30cf-135">如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="d30cf-135">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d30cf-136">範例</span><span class="sxs-lookup"><span data-stu-id="d30cf-136">Examples</span></span>

<span data-ttu-id="d30cf-137">下列範例示範如何使用 **RCDATA** 語句：</span><span class="sxs-lookup"><span data-stu-id="d30cf-137">The following example demonstrates the use of the **RCDATA** statement:</span></span>

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a><span data-ttu-id="d30cf-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d30cf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d30cf-139">**加速器**</span><span class="sxs-lookup"><span data-stu-id="d30cf-139">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="d30cf-140">**特徵**</span><span class="sxs-lookup"><span data-stu-id="d30cf-140">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="d30cf-141">**語言**</span><span class="sxs-lookup"><span data-stu-id="d30cf-141">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="d30cf-142">**功能表**</span><span class="sxs-lookup"><span data-stu-id="d30cf-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="d30cf-143">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="d30cf-143">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="d30cf-144">**版本**</span><span class="sxs-lookup"><span data-stu-id="d30cf-144">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 




