---
title: StringTable 結構
description: 代表檔案版本資源中的資料組織。 它包含子系成員所指定之字串的語言和字碼頁格式資訊。 字碼頁是一組已排序的字元集。
ms.assetid: e8e9d654-b515-434c-ac38-79d333a8d7cb
keywords:
- StringTable 結構功能表和其他資源
topic_type:
- apiref
api_name:
- StringTable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc790baa6484c5b1a8a7d96a0a7bc8e8ad12b0e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384141"
---
# <a name="stringtable-structure"></a><span data-ttu-id="b5932-106">StringTable 結構</span><span class="sxs-lookup"><span data-stu-id="b5932-106">StringTable structure</span></span>

<span data-ttu-id="b5932-107">代表檔案版本資源中的資料組織。</span><span class="sxs-lookup"><span data-stu-id="b5932-107">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="b5932-108">它包含 **子** 系成員所指定之字串的語言和字碼頁格式資訊。</span><span class="sxs-lookup"><span data-stu-id="b5932-108">It contains language and code page formatting information for the strings specified by the **Children** member.</span></span> <span data-ttu-id="b5932-109">字碼頁是一組已排序的字元集。</span><span class="sxs-lookup"><span data-stu-id="b5932-109">A code page is an ordered character set.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5932-110">語法</span><span class="sxs-lookup"><span data-stu-id="b5932-110">Syntax</span></span>


```C++
typedef struct {
  WORD   wLength;
  WORD   wValueLength;
  WORD   wType;
  WCHAR  szKey;
  WORD   Padding;
  String Children;
} StringTable;
```



## <a name="members"></a><span data-ttu-id="b5932-111">成員</span><span class="sxs-lookup"><span data-stu-id="b5932-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="b5932-112">**wLength**</span><span class="sxs-lookup"><span data-stu-id="b5932-112">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="b5932-113">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="b5932-113">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b5932-114">這個 **StringTable** 結構的長度（以位元組為單位），包括 **子** 成員所指示的所有結構。</span><span class="sxs-lookup"><span data-stu-id="b5932-114">The length, in bytes, of this **StringTable** structure, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="b5932-115">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="b5932-115">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="b5932-116">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="b5932-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b5932-117">這個成員永遠等於零。</span><span class="sxs-lookup"><span data-stu-id="b5932-117">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b5932-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="b5932-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="b5932-119">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="b5932-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b5932-120">版本資源中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="b5932-120">The type of data in the version resource.</span></span> <span data-ttu-id="b5932-121">如果版本資源包含文字資料，則此成員為1，如果版本資源包含二進位資料，則為0。</span><span class="sxs-lookup"><span data-stu-id="b5932-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="b5932-122">**szKey**</span><span class="sxs-lookup"><span data-stu-id="b5932-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="b5932-123">類型： **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="b5932-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="b5932-124">儲存為 Unicode 字串的8位數十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="b5932-124">An 8-digit hexadecimal number stored as a Unicode string.</span></span> <span data-ttu-id="b5932-125">四個最有效的數位代表語言識別項。</span><span class="sxs-lookup"><span data-stu-id="b5932-125">The four most significant digits represent the language identifier.</span></span> <span data-ttu-id="b5932-126">四個最不重要的數位代表要格式化資料的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="b5932-126">The four least significant digits represent the code page for which the data is formatted.</span></span> <span data-ttu-id="b5932-127">每個 Microsoft 標準語言識別項都包含兩個部分：低序位10位會指定主要語言，而高序位6位則會指定語言。</span><span class="sxs-lookup"><span data-stu-id="b5932-127">Each Microsoft Standard Language identifier contains two parts: the low-order 10 bits specify the major language, and the high-order 6 bits specify the sublanguage.</span></span> <span data-ttu-id="b5932-128">如需有效識別碼的表格，請參閱。</span><span class="sxs-lookup"><span data-stu-id="b5932-128">For a table of valid identifiers see .</span></span>

</dd> <dt>

<span data-ttu-id="b5932-129">**填補**</span><span class="sxs-lookup"><span data-stu-id="b5932-129">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="b5932-130">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="b5932-130">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b5932-131">在32位界限上對齊 **子** 成員所需的任意零個單字。</span><span class="sxs-lookup"><span data-stu-id="b5932-131">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="b5932-132">**子系**</span><span class="sxs-lookup"><span data-stu-id="b5932-132">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="b5932-133">類型： **[**字串**](string-str.md)**</span><span class="sxs-lookup"><span data-stu-id="b5932-133">Type: **[**String**](string-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b5932-134">一或多個 [**字串**](string-str.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="b5932-134">An array of one or more [**String**](string-str.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5932-135">備註</span><span class="sxs-lookup"><span data-stu-id="b5932-135">Remarks</span></span>

<span data-ttu-id="b5932-136">此結構不是真正的 C 語言結構，因為它包含可變長度的成員。</span><span class="sxs-lookup"><span data-stu-id="b5932-136">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="b5932-137">此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="b5932-137">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="b5932-138">[**StringFileInfo**](stringfileinfo.md)結構的 **子** 系成員至少包含一個 **StringTable** 結構。</span><span class="sxs-lookup"><span data-stu-id="b5932-138">The **Children** member of the [**StringFileInfo**](stringfileinfo.md) structure contains at least one **StringTable** structure.</span></span>

<span data-ttu-id="b5932-139">將 **szKey** 成員的字碼頁部分設定為十六進位值0x04b0，以指出 Unicode 字碼頁或適用于語言元件之字碼頁的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="b5932-139">Set the code page portion of the **szKey** member to the hexadecimal value 0x04b0 to indicate the Unicode code page, or to the hexadecimal value of the code page that is appropriate for the language component.</span></span> <span data-ttu-id="b5932-140">選擇 [字碼頁] 的值之後，您應該會在稍後的檔案修訂中繼續使用相同的值。</span><span class="sxs-lookup"><span data-stu-id="b5932-140">After you choose the value for the code page you should continue to use the same value in later revisions to the file.</span></span>

<span data-ttu-id="b5932-141">支援多種語言的可執行檔或 DLL 應該具有每個語言的版本資源，而不是包含數種語言之字串的單一版本資源。</span><span class="sxs-lookup"><span data-stu-id="b5932-141">An executable file or DLL that supports multiple languages should have a version resource for each language, rather than a single version resource that contains strings in several languages.</span></span> <span data-ttu-id="b5932-142">但是，如果您使用 [**var**](var-str.md)結構來列出您的應用程式支援的語言，則版本資源中的 **StringTable** 結構數目會與 **Var** 結構的 **Value** 成員中的語言/字碼頁識別碼組數目直接相關。</span><span class="sxs-lookup"><span data-stu-id="b5932-142">However, if you use the [**Var**](var-str.md) structure to list the languages that your application supports, the number of **StringTable** structures in the version resource is directly related to the number of language/code page identifier pairs in the **Value** member of the **Var** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5932-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5932-143">Requirements</span></span>



| <span data-ttu-id="b5932-144">需求</span><span class="sxs-lookup"><span data-stu-id="b5932-144">Requirement</span></span> | <span data-ttu-id="b5932-145">值</span><span class="sxs-lookup"><span data-stu-id="b5932-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b5932-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5932-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b5932-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5932-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b5932-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5932-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b5932-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5932-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b5932-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5932-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="b5932-151">**參考**</span><span class="sxs-lookup"><span data-stu-id="b5932-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b5932-152">**字串**</span><span class="sxs-lookup"><span data-stu-id="b5932-152">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="b5932-153">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="b5932-153">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="b5932-154">**無 功**</span><span class="sxs-lookup"><span data-stu-id="b5932-154">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="b5932-155">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="b5932-155">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="b5932-156">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="b5932-156">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="b5932-157">**概念**</span><span class="sxs-lookup"><span data-stu-id="b5932-157">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b5932-158">版本資訊</span><span class="sxs-lookup"><span data-stu-id="b5932-158">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





