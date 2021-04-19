---
title: 字串結構
description: 代表檔案版本資源中的資料組織。 它包含的字串會描述檔案的特定層面，例如檔案的版本、其著作權聲明或其商標。
ms.assetid: fcc5ac68-4aec-4a3b-aa92-96fc50cc4ca2
keywords:
- 字串結構功能表和其他資源
topic_type:
- apiref
api_name:
- String
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7035223082a9e446caebd6e07d3d55c84536d09f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967526"
---
# <a name="string-structure"></a><span data-ttu-id="38d16-105">字串結構</span><span class="sxs-lookup"><span data-stu-id="38d16-105">String structure</span></span>

<span data-ttu-id="38d16-106">代表檔案版本資源中的資料組織。</span><span class="sxs-lookup"><span data-stu-id="38d16-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="38d16-107">它包含的字串會描述檔案的特定層面，例如檔案的版本、其著作權聲明或其商標。</span><span class="sxs-lookup"><span data-stu-id="38d16-107">It contains a string that describes a specific aspect of a file, for example, a file's version, its copyright notices, or its trademarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d16-108">語法</span><span class="sxs-lookup"><span data-stu-id="38d16-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  WORD  Value;
} String;
```



## <a name="members"></a><span data-ttu-id="38d16-109">成員</span><span class="sxs-lookup"><span data-stu-id="38d16-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="38d16-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="38d16-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="38d16-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="38d16-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="38d16-112">這個 **字串** 結構的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="38d16-112">The length, in bytes, of this **String** structure.</span></span>

</dd> <dt>

<span data-ttu-id="38d16-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="38d16-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="38d16-114">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="38d16-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="38d16-115">**值** 成員的大小，以單字為限。</span><span class="sxs-lookup"><span data-stu-id="38d16-115">The size, in words, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="38d16-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="38d16-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="38d16-117">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="38d16-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="38d16-118">版本資源中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="38d16-118">The type of data in the version resource.</span></span> <span data-ttu-id="38d16-119">如果版本資源包含文字資料，則此成員為1，如果版本資源包含二進位資料，則為0。</span><span class="sxs-lookup"><span data-stu-id="38d16-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="38d16-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="38d16-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="38d16-121">類型： **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="38d16-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="38d16-122">任意的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="38d16-122">An arbitrary Unicode string.</span></span> <span data-ttu-id="38d16-123">**SzKey** 成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="38d16-123">The **szKey** member can be one or more of the following values.</span></span> <span data-ttu-id="38d16-124">這些值只是指導方針。</span><span class="sxs-lookup"><span data-stu-id="38d16-124">These values are guidelines only.</span></span>

<dt>

<span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>

<span data-ttu-id="38d16-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**評論**</span><span class="sxs-lookup"><span data-stu-id="38d16-125"><span id="Comments"></span><span id="comments"></span><span id="COMMENTS"></span>**Comments**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-126">**值** 成員包含應針對診斷目的顯示的任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="38d16-126">The **Value** member contains any additional information that should be displayed for diagnostic purposes.</span></span> <span data-ttu-id="38d16-127">這個字串可以是任意長度。</span><span class="sxs-lookup"><span data-stu-id="38d16-127">This string can be an arbitrary length.</span></span>

</dd> <dt>

<span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>

<span data-ttu-id="38d16-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**名稱**</span><span class="sxs-lookup"><span data-stu-id="38d16-128"><span id="CompanyName"></span><span id="companyname"></span><span id="COMPANYNAME"></span>**CompanyName**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-129">**值** 成員會識別產生檔案的公司。</span><span class="sxs-lookup"><span data-stu-id="38d16-129">The **Value** member identifies the company that produced the file.</span></span> <span data-ttu-id="38d16-130">例如，"Microsoft Corporation" 或 "Standard Microsystems Corporation，Inc."</span><span class="sxs-lookup"><span data-stu-id="38d16-130">For example, "Microsoft Corporation" or "Standard Microsystems Corporation, Inc."</span></span>

</dd> <dt>

<span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>

<span data-ttu-id="38d16-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span><span class="sxs-lookup"><span data-stu-id="38d16-131"><span id="FileDescription"></span><span id="filedescription"></span><span id="FILEDESCRIPTION"></span>**FileDescription**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-132">**值** 成員會以提供給使用者的方式來描述檔案。</span><span class="sxs-lookup"><span data-stu-id="38d16-132">The **Value** member describes the file in such a way that it can be presented to users.</span></span> <span data-ttu-id="38d16-133">當使用者選擇要安裝的檔案時，此字串可能會顯示在清單方塊中。</span><span class="sxs-lookup"><span data-stu-id="38d16-133">This string may be presented in a list box when the user is choosing files to install.</span></span> <span data-ttu-id="38d16-134">例如，「適用于樣式鍵盤的鍵盤驅動程式」或「適用于 Windows 的 Microsoft Word」。</span><span class="sxs-lookup"><span data-stu-id="38d16-134">For example, "Keyboard driver for AT-style keyboards" or "Microsoft Word for Windows".</span></span>

</dd> <dt>

<span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>

<span data-ttu-id="38d16-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span><span class="sxs-lookup"><span data-stu-id="38d16-135"><span id="FileVersion"></span><span id="fileversion"></span><span id="FILEVERSION"></span>**FileVersion**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-136">**值** 成員會識別此檔案的版本。</span><span class="sxs-lookup"><span data-stu-id="38d16-136">The **Value** member identifies the version of this file.</span></span> <span data-ttu-id="38d16-137">例如， **值** 可以是 "3.00 a" 或 "5.00. RC2"。</span><span class="sxs-lookup"><span data-stu-id="38d16-137">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>

<span data-ttu-id="38d16-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span><span class="sxs-lookup"><span data-stu-id="38d16-138"><span id="InternalName"></span><span id="internalname"></span><span id="INTERNALNAME"></span>**InternalName**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-139">**值** 成員會識別檔案的內部名稱（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="38d16-139">The **Value** member identifies the file's internal name, if one exists.</span></span> <span data-ttu-id="38d16-140">例如，此字串可能包含 DLL 的模組名稱、Windows 虛擬裝置的虛擬裝置名稱，或 MS-DOS 設備磁碟機的裝置名稱。</span><span class="sxs-lookup"><span data-stu-id="38d16-140">For example, this string could contain the module name for a DLL, a virtual device name for a Windows virtual device, or a device name for a MS-DOS device driver.</span></span>

</dd> <dt>

<span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>

<span data-ttu-id="38d16-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span><span class="sxs-lookup"><span data-stu-id="38d16-141"><span id="LegalCopyright"></span><span id="legalcopyright"></span><span id="LEGALCOPYRIGHT"></span>**LegalCopyright**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-142">**值** 成員描述適用于檔案的所有著作權聲明、商標和注冊商標。</span><span class="sxs-lookup"><span data-stu-id="38d16-142">The **Value** member describes all copyright notices, trademarks, and registered trademarks that apply to the file.</span></span> <span data-ttu-id="38d16-143">這應包括所有注意事項全文、法律符號、版權日期、商標登錄編號等等。</span><span class="sxs-lookup"><span data-stu-id="38d16-143">This should include the full text of all notices, legal symbols, copyright dates, trademark numbers, and so on.</span></span> <span data-ttu-id="38d16-144">在英文中，此字串的格式應為 "著作權 Microsoft Corp. 1990 1994"。</span><span class="sxs-lookup"><span data-stu-id="38d16-144">In English, this string should be in the format "Copyright Microsoft Corp. 1990  1994".</span></span>

</dd> <dt>

<span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>

<span data-ttu-id="38d16-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span><span class="sxs-lookup"><span data-stu-id="38d16-145"><span id="LegalTrademarks"></span><span id="legaltrademarks"></span><span id="LEGALTRADEMARKS"></span>**LegalTrademarks**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-146">**值** 成員描述適用于檔案的所有商標和注冊商標。</span><span class="sxs-lookup"><span data-stu-id="38d16-146">The **Value** member describes all trademarks and registered trademarks that apply to the file.</span></span> <span data-ttu-id="38d16-147">這應包括所有注意事項全文、法律符號、商標登錄編號等等。</span><span class="sxs-lookup"><span data-stu-id="38d16-147">This should include the full text of all notices, legal symbols, trademark numbers, and so on.</span></span> <span data-ttu-id="38d16-148">此段文字的英文格式應為 "Windows is a trademark of Microsoft Corporation"。</span><span class="sxs-lookup"><span data-stu-id="38d16-148">In English, this string should be in the format "Windows is a trademark of Microsoft Corporation".</span></span>

</dd> <dt>

<span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>

<span data-ttu-id="38d16-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span><span class="sxs-lookup"><span data-stu-id="38d16-149"><span id="OriginalFilename"></span><span id="originalfilename"></span><span id="ORIGINALFILENAME"></span>**OriginalFilename**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-150">**值** 成員會識別檔案的原始名稱，而不包含路徑。</span><span class="sxs-lookup"><span data-stu-id="38d16-150">The **Value** member identifies the original name of the file, not including a path.</span></span> <span data-ttu-id="38d16-151">這可讓應用程式判斷使用者是否已重新命名檔案。</span><span class="sxs-lookup"><span data-stu-id="38d16-151">This enables an application to determine whether a file has been renamed by a user.</span></span> <span data-ttu-id="38d16-152">如果檔案是非 FAT 檔案系統的特定名稱，則此名稱不可以是 MS-DOS 8.3 格式。</span><span class="sxs-lookup"><span data-stu-id="38d16-152">This name may not be MS-DOS 8.3-format if the file is specific to a non-FAT file system.</span></span>

</dd> <dt>

<span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>

<span data-ttu-id="38d16-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span><span class="sxs-lookup"><span data-stu-id="38d16-153"><span id="PrivateBuild"></span><span id="privatebuild"></span><span id="PRIVATEBUILD"></span>**PrivateBuild**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-154">**值** 成員會根據其建立檔案私用版本的位置和原因來描述。</span><span class="sxs-lookup"><span data-stu-id="38d16-154">The **Value** member describes by whom, where, and why this private version of the file was built.</span></span> <span data-ttu-id="38d16-155">只有當 vs **\_ FF \_ PRI加值稅EBUILD** 旗標設定于 [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)結構的 **dwFileFlags** 成員時，才會出現這個字串。</span><span class="sxs-lookup"><span data-stu-id="38d16-155">This string should only be present if the **VS\_FF\_PRIVATEBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="38d16-156">例如， **值** 可能是「OSCAR2 上的 OSCAR 建立」 \\ 。</span><span class="sxs-lookup"><span data-stu-id="38d16-156">For example, **Value** could be "Built by OSCAR on \\OSCAR2".</span></span>

</dd> <dt>

<span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>

<span data-ttu-id="38d16-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**名稱**</span><span class="sxs-lookup"><span data-stu-id="38d16-157"><span id="ProductName"></span><span id="productname"></span><span id="PRODUCTNAME"></span>**ProductName**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-158">**值** 成員會識別這個檔案所散發的產品名稱。</span><span class="sxs-lookup"><span data-stu-id="38d16-158">The **Value** member identifies the name of the product with which this file is distributed.</span></span> <span data-ttu-id="38d16-159">例如，這個字串可能是「Microsoft Windows」。</span><span class="sxs-lookup"><span data-stu-id="38d16-159">For example, this string could be "Microsoft Windows".</span></span>

</dd> <dt>

<span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>

<span data-ttu-id="38d16-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="38d16-160"><span id="ProductVersion"></span><span id="productversion"></span><span id="PRODUCTVERSION"></span>**ProductVersion**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-161">**值** 成員會識別這個檔案所散發的產品版本。</span><span class="sxs-lookup"><span data-stu-id="38d16-161">The **Value** member identifies the version of the product with which this file is distributed.</span></span> <span data-ttu-id="38d16-162">例如， **值** 可以是 "3.00 a" 或 "5.00. RC2"。</span><span class="sxs-lookup"><span data-stu-id="38d16-162">For example, **Value** could be "3.00A" or "5.00.RC2".</span></span>

</dd> <dt>

<span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>

<span data-ttu-id="38d16-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span><span class="sxs-lookup"><span data-stu-id="38d16-163"><span id="SpecialBuild"></span><span id="specialbuild"></span><span id="SPECIALBUILD"></span>**SpecialBuild**</span></span>


</dt> <dd>

<span data-ttu-id="38d16-164">**值** 成員描述此檔案版本與一般版本的差異。</span><span class="sxs-lookup"><span data-stu-id="38d16-164">The **Value** member describes how this version of the file differs from the normal version.</span></span> <span data-ttu-id="38d16-165">只有當 vs **\_ FF \_ SPECIALBUILD** 旗標設定于 [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)結構的 **dwFileFlags** 成員時，此專案才會存在。</span><span class="sxs-lookup"><span data-stu-id="38d16-165">This entry should only be present if the **VS\_FF\_SPECIALBUILD** flag is set in the **dwFileFlags** member of the [**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) structure.</span></span> <span data-ttu-id="38d16-166">例如， **值** 可能是「Olivetti 在 M250 和 M250E 電腦上解決滑鼠問題的私用組建」。</span><span class="sxs-lookup"><span data-stu-id="38d16-166">For example, **Value** could be "Private build for Olivetti solving mouse problems on M250 and M250E computers".</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="38d16-167">**填補**</span><span class="sxs-lookup"><span data-stu-id="38d16-167">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="38d16-168">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="38d16-168">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="38d16-169">在32位界限上對齊 **值** 成員所需的任意零個單字。</span><span class="sxs-lookup"><span data-stu-id="38d16-169">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="38d16-170">**值**</span><span class="sxs-lookup"><span data-stu-id="38d16-170">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="38d16-171">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="38d16-171">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="38d16-172">以零結尾的字串。</span><span class="sxs-lookup"><span data-stu-id="38d16-172">A zero-terminated string.</span></span> <span data-ttu-id="38d16-173">如需詳細資訊，請參閱 **szKey** 成員描述。</span><span class="sxs-lookup"><span data-stu-id="38d16-173">See the **szKey** member description for more information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38d16-174">備註</span><span class="sxs-lookup"><span data-stu-id="38d16-174">Remarks</span></span>

<span data-ttu-id="38d16-175">此結構不是真正的 C 語言結構，因為它包含可變長度的成員。</span><span class="sxs-lookup"><span data-stu-id="38d16-175">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="38d16-176">此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="38d16-176">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="38d16-177">**字串** 結構可能具有 szKey 值，例如 "  " 和 "Microsoft Corporation" 的 **值**。</span><span class="sxs-lookup"><span data-stu-id="38d16-177">A **String** structure may have an **szKey** value of, for example, "CompanyName" and a **Value** of "Microsoft Corporation".</span></span> <span data-ttu-id="38d16-178">另一個具有相同 **szKey** 值的 **字串** 結構可能包含 "Microsoft GmbH" 的 **值**。</span><span class="sxs-lookup"><span data-stu-id="38d16-178">Another **String** structure with the same **szKey** value could contain a **Value** of "Microsoft GmbH".</span></span> <span data-ttu-id="38d16-179">如果第二個 **字串** 結構與 [**StringTable**](stringtable.md) 結構相關聯，而其 **szKey** 值是040704b0，也就是德文/Unicode，則可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="38d16-179">This might occur if the second **String** structure were associated with a [**StringTable**](stringtable.md) structure whose **szKey** value is 040704b0   that is, German/Unicode.</span></span>

## <a name="requirements"></a><span data-ttu-id="38d16-180">規格需求</span><span class="sxs-lookup"><span data-stu-id="38d16-180">Requirements</span></span>



| <span data-ttu-id="38d16-181">需求</span><span class="sxs-lookup"><span data-stu-id="38d16-181">Requirement</span></span> | <span data-ttu-id="38d16-182">值</span><span class="sxs-lookup"><span data-stu-id="38d16-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="38d16-183">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38d16-183">Minimum supported client</span></span><br/> | <span data-ttu-id="38d16-184">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38d16-184">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="38d16-185">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38d16-185">Minimum supported server</span></span><br/> | <span data-ttu-id="38d16-186">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38d16-186">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="38d16-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38d16-187">See also</span></span>

<dl> <dt>

<span data-ttu-id="38d16-188">**參考**</span><span class="sxs-lookup"><span data-stu-id="38d16-188">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38d16-189">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="38d16-189">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="38d16-190">**VS \_ FIXEDFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="38d16-190">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

[<span data-ttu-id="38d16-191">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="38d16-191">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="38d16-192">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="38d16-192">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="38d16-193">**概念**</span><span class="sxs-lookup"><span data-stu-id="38d16-193">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38d16-194">版本資訊</span><span class="sxs-lookup"><span data-stu-id="38d16-194">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





