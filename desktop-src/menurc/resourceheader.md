---
title: RESOURCEHEADER 結構
description: 包含資源標頭本身的相關資訊，以及此資源特定的資料。
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- RESOURCEHEADER 結構功能表和其他資源
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965887"
---
# <a name="resourceheader-structure"></a><span data-ttu-id="f850c-104">RESOURCEHEADER 結構</span><span class="sxs-lookup"><span data-stu-id="f850c-104">RESOURCEHEADER structure</span></span>

<span data-ttu-id="f850c-105">包含資源標頭本身的相關資訊，以及此資源特定的資料。</span><span class="sxs-lookup"><span data-stu-id="f850c-105">Contains information about the resource header itself and the data specific to this resource.</span></span> <span data-ttu-id="f850c-106">此結構不是真正的 C 語言結構，因為它包含可變長度的成員。</span><span class="sxs-lookup"><span data-stu-id="f850c-106">This structure is not a true C-language structure, because it contains variable-length members.</span></span> <span data-ttu-id="f850c-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="f850c-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f850c-108">語法</span><span class="sxs-lookup"><span data-stu-id="f850c-108">Syntax</span></span>


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a><span data-ttu-id="f850c-109">成員</span><span class="sxs-lookup"><span data-stu-id="f850c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="f850c-110">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="f850c-110">**DataSize**</span></span>
</dt> <dd>

<span data-ttu-id="f850c-111">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f850c-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f850c-112">在此特定資源的資源標頭之後，資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f850c-112">The size, in bytes, of the data that follows the resource header for this particular resource.</span></span> <span data-ttu-id="f850c-113">它不會在資源檔中包含此資源和其後任何資源之間的任何檔案填補。</span><span class="sxs-lookup"><span data-stu-id="f850c-113">It does not include any file padding between this resource and any resource that follows it in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="f850c-114">**HeaderSize**</span><span class="sxs-lookup"><span data-stu-id="f850c-114">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="f850c-115">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f850c-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f850c-116">接下來資源標頭資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f850c-116">The size, in bytes, of the resource header data that follows.</span></span>

</dd> <dt>

<span data-ttu-id="f850c-117">**TYPE**</span><span class="sxs-lookup"><span data-stu-id="f850c-117">**TYPE**</span></span>
</dt> <dd>

<span data-ttu-id="f850c-118">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f850c-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f850c-119">資源類型。</span><span class="sxs-lookup"><span data-stu-id="f850c-119">The resource type.</span></span> <span data-ttu-id="f850c-120">**型** 別成員可以是數值，也可以是以 null 結束的 Unicode 字串來指定類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="f850c-120">The **TYPE** member can either be a numeric value or a null-terminated Unicode string that specifies the name of the type.</span></span> <span data-ttu-id="f850c-121">如需 **名稱** 或 **序數** 類型成員的描述，請參閱下列備註一節。</span><span class="sxs-lookup"><span data-stu-id="f850c-121">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="f850c-122">如果 **類型** 成員是數值，則可以指定標準或使用者定義的資源類型。</span><span class="sxs-lookup"><span data-stu-id="f850c-122">If the **TYPE** member is a numeric value, it can specify either a standard or a user-defined resource type.</span></span> <span data-ttu-id="f850c-123">如果成員是字串，則它是使用者定義的資源類型。</span><span class="sxs-lookup"><span data-stu-id="f850c-123">If the member is a string, then it is a user-defined resource type.</span></span> <span data-ttu-id="f850c-124">如需預先定義的資源類型清單，請參閱 [資源類型](/windows/desktop/menurc/resource-types)。</span><span class="sxs-lookup"><span data-stu-id="f850c-124">For a list of the predefined resource types, see [Resource Types](/windows/desktop/menurc/resource-types).</span></span>

<span data-ttu-id="f850c-125">小於256的值會保留供系統使用。</span><span class="sxs-lookup"><span data-stu-id="f850c-125">Values less than 256 are reserved for system use.</span></span>

</dd> <dt>

<span data-ttu-id="f850c-126">**名稱**</span><span class="sxs-lookup"><span data-stu-id="f850c-126">**NAME**</span></span>
</dt> <dd>

<span data-ttu-id="f850c-127">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f850c-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f850c-128">識別特定資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f850c-128">A name that identifies the particular resource.</span></span> <span data-ttu-id="f850c-129">**名稱** 成員就像 **類型** 成員一樣，可以是數值或以 null 終止的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="f850c-129">The **NAME** member, like the **TYPE** member, can either be a numeric value or a null-terminated Unicode string.</span></span> <span data-ttu-id="f850c-130">如需 **名稱** 或 **序數** 類型成員的描述，請參閱下列備註一節。</span><span class="sxs-lookup"><span data-stu-id="f850c-130">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="f850c-131">您不需要在 **類型** 和 **名稱** 成員之間新增 **DWORD** 對齊的填補，因為它們包含 **文字** 資料。</span><span class="sxs-lookup"><span data-stu-id="f850c-131">You do not need to add padding for **DWORD** alignment between the **TYPE** and **NAME** members because they contain **WORD** data.</span></span> <span data-ttu-id="f850c-132">不過，您可能需要在 **名稱** 成員後面加上邊框間距，以對齊 **DWORD** 界限上的其餘標頭。</span><span class="sxs-lookup"><span data-stu-id="f850c-132">However, you may need to add a **WORD** of padding after the **NAME** member to align the rest of the header on **DWORD** boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="f850c-133">**DataVersion**</span><span class="sxs-lookup"><span data-stu-id="f850c-133">**DataVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f850c-134">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f850c-134">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f850c-135">預先定義的資源資料版本。</span><span class="sxs-lookup"><span data-stu-id="f850c-135">A predefined resource data version.</span></span> <span data-ttu-id="f850c-136">這會決定應用程式應使用哪個版本的資源資料。</span><span class="sxs-lookup"><span data-stu-id="f850c-136">This will determine which version of the resource data the application should use.</span></span>

</dd> <dt>

<span data-ttu-id="f850c-137">**MemoryFlags**</span><span class="sxs-lookup"><span data-stu-id="f850c-137">**MemoryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f850c-138">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="f850c-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f850c-139">一組可描述資源狀態的屬性旗標。</span><span class="sxs-lookup"><span data-stu-id="f850c-139">A set of attribute flags that can describe the state of the resource.</span></span> <span data-ttu-id="f850c-140">中的修飾詞。RC 腳本檔會將這些屬性指派給資源。</span><span class="sxs-lookup"><span data-stu-id="f850c-140">Modifiers in the .RC script file assign these attributes to the resource.</span></span> <span data-ttu-id="f850c-141">腳本識別碼可以指派下列旗標值。</span><span class="sxs-lookup"><span data-stu-id="f850c-141">The script identifiers can assign the following flag values.</span></span>

<span data-ttu-id="f850c-142">應用程式不會使用這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f850c-142">Applications do not use any of these attributes.</span></span> <span data-ttu-id="f850c-143">腳本中允許使用屬性來與現有腳本回溯相容，但是會忽略這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f850c-143">The attributes are permitted in the script for backward compatibility with existing scripts, but they are ignored.</span></span> <span data-ttu-id="f850c-144">載入對應模組時，會載入資源，並在卸載模組時釋放資源。</span><span class="sxs-lookup"><span data-stu-id="f850c-144">Resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

<span data-ttu-id="f850c-145">**可移動** 的 (0x0010) </span><span class="sxs-lookup"><span data-stu-id="f850c-145">**MOVEABLE** (0x0010)</span></span>


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

<span data-ttu-id="f850c-146">已 **修正** (~ 可移動) </span><span class="sxs-lookup"><span data-stu-id="f850c-146">**FIXED** (~MOVEABLE)</span></span>


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

<span data-ttu-id="f850c-147">**純** (0x0020) </span><span class="sxs-lookup"><span data-stu-id="f850c-147">**PURE** (0x0020)</span></span>


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

<span data-ttu-id="f850c-148">**IMPURE** (~ 純) </span><span class="sxs-lookup"><span data-stu-id="f850c-148">**IMPURE** (~PURE)</span></span>


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

<span data-ttu-id="f850c-149">**預先載入** (0x0040) </span><span class="sxs-lookup"><span data-stu-id="f850c-149">**PRELOAD** (0x0040)</span></span>


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

<span data-ttu-id="f850c-150">**LOADONCALL** (~ 預先載入) </span><span class="sxs-lookup"><span data-stu-id="f850c-150">**LOADONCALL** (~PRELOAD)</span></span>


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

<span data-ttu-id="f850c-151">**DISCARDABLE** (0x1000) </span><span class="sxs-lookup"><span data-stu-id="f850c-151">**DISCARDABLE** (0x1000)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="f850c-152">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="f850c-152">**LanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="f850c-153">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="f850c-153">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f850c-154">資源或資源集的語言。</span><span class="sxs-lookup"><span data-stu-id="f850c-154">The language for the resource or set of resources.</span></span> <span data-ttu-id="f850c-155">使用選擇性 [語言](./language-statement.md) 資源定義語句來設定這個成員的值。</span><span class="sxs-lookup"><span data-stu-id="f850c-155">Set the value for this member with the optional [LANGUAGE](./language-statement.md) resource definition statement.</span></span> <span data-ttu-id="f850c-156">這些參數是來自 Winnt .h 檔案的常數。</span><span class="sxs-lookup"><span data-stu-id="f850c-156">The parameters are constants from the Winnt.h file.</span></span>

<span data-ttu-id="f850c-157">每個資源都包含一個語言識別項，讓系統或應用程式可以選取適用于系統目前地區設定的語言。</span><span class="sxs-lookup"><span data-stu-id="f850c-157">Each resource includes a language identifier so the system or application can select a language appropriate for the current locale of the system.</span></span> <span data-ttu-id="f850c-158">如果有多個相同類型和名稱的資源與資源內的字串語言不同，您就必須為每個資源指定 **LanguageId** 。</span><span class="sxs-lookup"><span data-stu-id="f850c-158">If there are multiple resources of the same type and name that differ only in the language of the strings within the resources, you will need to specify a **LanguageId** for each one.</span></span>

</dd> <dt>

<span data-ttu-id="f850c-159">**版本**</span><span class="sxs-lookup"><span data-stu-id="f850c-159">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="f850c-160">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f850c-160">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f850c-161">工具可用來讀取和寫入資源檔的資源資料的使用者定義版本號碼。</span><span class="sxs-lookup"><span data-stu-id="f850c-161">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span> <span data-ttu-id="f850c-162">使用選擇性的 [版本](./version-statement.md) 資源定義語句來設定此值。</span><span class="sxs-lookup"><span data-stu-id="f850c-162">Set this value with the optional [VERSION](./version-statement.md) resource definition statement.</span></span>

</dd> <dt>

<span data-ttu-id="f850c-163">**特性**</span><span class="sxs-lookup"><span data-stu-id="f850c-163">**Characteristics**</span></span>
</dt> <dd>

<span data-ttu-id="f850c-164">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f850c-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f850c-165">指定有關工具可用來讀取和寫入資源檔之資源的使用者定義資訊。</span><span class="sxs-lookup"><span data-stu-id="f850c-165">Specifies user-defined information about the resource that tools can use to read and write resource files.</span></span> <span data-ttu-id="f850c-166">使用選擇性的 [ [特性](./characteristics-statement.md) ] 資源定義語句來設定此值。</span><span class="sxs-lookup"><span data-stu-id="f850c-166">Set this value with the optional [CHARACTERISTICS](./characteristics-statement.md) resource definition statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f850c-167">備註</span><span class="sxs-lookup"><span data-stu-id="f850c-167">Remarks</span></span>

<span data-ttu-id="f850c-168">變數型別成員稱為「 **名稱** 」或「 **序數** 」成員，它會在資源檔中出現識別碼的大部分位置使用。</span><span class="sxs-lookup"><span data-stu-id="f850c-168">A variable type member is called a **Name** or **Ordinal** member, and it is used in most places in the resource file where an identifier appears.</span></span> <span data-ttu-id="f850c-169">**Name** 或 **序數** 類型成員的第一個 **單字** 指出成員是數值或字串。</span><span class="sxs-lookup"><span data-stu-id="f850c-169">The first **WORD** of a **Name** or **Ordinal** type member indicates whether the member is a numeric value or a string.</span></span> <span data-ttu-id="f850c-170">如果成員中的第一個 **單字** 等於值0xffff （這是不正確 Unicode 字元），則下列 **單字** 是類型號碼。</span><span class="sxs-lookup"><span data-stu-id="f850c-170">If the first **WORD** in the member is equal to the value 0xffff, which is an invalid Unicode character, then the following **WORD** is a type number.</span></span> <span data-ttu-id="f850c-171">否則，成員會包含 Unicode 字串，而成員中的第一個 **單字** 是名稱字串中的第一個字元。</span><span class="sxs-lookup"><span data-stu-id="f850c-171">Otherwise, the member contains a Unicode string and the first **WORD** in the member is the first character in the name string.</span></span> <span data-ttu-id="f850c-172">如需資源定義語句的詳細資訊，請參閱 [資源定義語句](./resource-definition-statements.md)。</span><span class="sxs-lookup"><span data-stu-id="f850c-172">For additional information about resource definition statements, see [Resource-Definition Statements](./resource-definition-statements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f850c-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="f850c-173">Requirements</span></span>



| <span data-ttu-id="f850c-174">需求</span><span class="sxs-lookup"><span data-stu-id="f850c-174">Requirement</span></span> | <span data-ttu-id="f850c-175">值</span><span class="sxs-lookup"><span data-stu-id="f850c-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f850c-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f850c-176">Minimum supported client</span></span><br/> | <span data-ttu-id="f850c-177">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f850c-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f850c-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f850c-178">Minimum supported server</span></span><br/> | <span data-ttu-id="f850c-179">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f850c-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f850c-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f850c-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="f850c-181">**概念**</span><span class="sxs-lookup"><span data-stu-id="f850c-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f850c-182">資源</span><span class="sxs-lookup"><span data-stu-id="f850c-182">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="f850c-183">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="f850c-183">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f850c-184">特性語句</span><span class="sxs-lookup"><span data-stu-id="f850c-184">CHARACTERISTICS Statement</span></span>](./characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="f850c-185">LANGUAGE 語句</span><span class="sxs-lookup"><span data-stu-id="f850c-185">LANGUAGE Statement</span></span>](./language-statement.md)
</dt> <dt>

[<span data-ttu-id="f850c-186">VERSION 語句</span><span class="sxs-lookup"><span data-stu-id="f850c-186">VERSION Statement</span></span>](./version-statement.md)
</dt> </dl>

 

