---
title: VS_VERSIONINFO 結構
description: 代表檔案版本資源中的資料組織。 它是包含所有其他檔案版本資訊結構的根結構。
ms.assetid: 7864510f-1894-4f17-bf7b-fd5bc1ba4aae
keywords:
- VS_VERSIONINFO 結構功能表和其他資源
topic_type:
- apiref
api_name:
- VS_VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2758d5553e192357296868e2dbb62f7a6733ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106163"
---
# <a name="vs_versioninfo-structure"></a><span data-ttu-id="e4cc0-105">VS \_ VERSIONINFO 結構</span><span class="sxs-lookup"><span data-stu-id="e4cc0-105">VS\_VERSIONINFO structure</span></span>

<span data-ttu-id="e4cc0-106">代表檔案版本資源中的資料組織。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="e4cc0-107">它是包含所有其他檔案版本資訊結構的根結構。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-107">It is the root structure that contains all other file-version information structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4cc0-108">語法</span><span class="sxs-lookup"><span data-stu-id="e4cc0-108">Syntax</span></span>


```C++
typedef struct {
  WORD             wLength;
  WORD             wValueLength;
  WORD             wType;
  WCHAR            szKey;
  WORD             Padding1;
  VS_FIXEDFILEINFO Value;
  WORD             Padding2;
  WORD             Children;
} VS_VERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="e4cc0-109">成員</span><span class="sxs-lookup"><span data-stu-id="e4cc0-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e4cc0-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="e4cc0-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e4cc0-112">**VS \_ VERSIONINFO** 結構的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-112">The length, in bytes, of the **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="e4cc0-113">此長度不包含在32位界限上對齊任何後續版本資源資料的任何填補。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-113">This length does not include any padding that aligns any subsequent version resource data on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="e4cc0-114">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-114">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="e4cc0-115">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e4cc0-116">**值** 成員的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-116">The length, in bytes, of the **Value** member.</span></span> <span data-ttu-id="e4cc0-117">如果沒有任何與目前版本結構相關聯的 **值** 成員，則此值為零。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-117">This value is zero if there is no **Value** member associated with the current version structure.</span></span>

</dd> <dt>

<span data-ttu-id="e4cc0-118">**wType**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-118">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="e4cc0-119">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-119">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e4cc0-120">版本資源中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-120">The type of data in the version resource.</span></span> <span data-ttu-id="e4cc0-121">如果版本資源包含文字資料，則此成員為1，如果版本資源包含二進位資料，則為0。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-121">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="e4cc0-122">**szKey**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-122">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="e4cc0-123">類型： **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-123">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="e4cc0-124">Unicode 字串 L 「VS \_ VERSION \_ INFO」。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-124">The Unicode string L"VS\_VERSION\_INFO".</span></span>

</dd> <dt>

<span data-ttu-id="e4cc0-125">**Padding1**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-125">**Padding1**</span></span>
</dt> <dd>

<span data-ttu-id="e4cc0-126">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e4cc0-127">包含所需的零個單字，以對齊32位界限上的 **值** 成員。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-127">Contains as many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="e4cc0-128">**值**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-128">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="e4cc0-129">類型： **[ **VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-129">Type: **[**VS\_FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)**</span></span>

</dd> <dd>

<span data-ttu-id="e4cc0-130">與這個 **VS \_ VERSIONINFO** 結構相關聯的任意資料。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-130">Arbitrary data associated with this **VS\_VERSIONINFO** structure.</span></span> <span data-ttu-id="e4cc0-131">**WValueLength** 成員會指定這個成員的長度;如果 **wValueLength** 為零，則此成員不存在。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-131">The **wValueLength** member specifies the length of this member; if **wValueLength** is zero, this member does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="e4cc0-132">**Padding2**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-132">**Padding2**</span></span>
</dt> <dd>

<span data-ttu-id="e4cc0-133">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-133">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e4cc0-134">在32位界限上對齊 **子** 成員所需的任意零個單字。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-134">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span> <span data-ttu-id="e4cc0-135">這些位元組不包含在 **wValueLength** 中。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-135">These bytes are not included in **wValueLength**.</span></span> <span data-ttu-id="e4cc0-136">這個成員是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-136">This member is optional.</span></span>

</dd> <dt>

<span data-ttu-id="e4cc0-137">**子系**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-137">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="e4cc0-138">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e4cc0-139">零或一個 [**StringFileInfo**](stringfileinfo.md)結構的陣列，以及屬於目前 **VS \_ VERSIONINFO** 結構子系的零個或一個 [**VarFileInfo**](varfileinfo.md)結構。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-139">An array of zero or one [**StringFileInfo**](stringfileinfo.md) structures, and zero or one [**VarFileInfo**](varfileinfo.md) structures that are children of the current **VS\_VERSIONINFO** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4cc0-140">備註</span><span class="sxs-lookup"><span data-stu-id="e4cc0-140">Remarks</span></span>

<span data-ttu-id="e4cc0-141">此結構不是真正的 C 語言結構，因為它包含可變長度的成員。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-141">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="e4cc0-142">此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="e4cc0-142">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4cc0-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4cc0-143">Requirements</span></span>



| <span data-ttu-id="e4cc0-144">需求</span><span class="sxs-lookup"><span data-stu-id="e4cc0-144">Requirement</span></span> | <span data-ttu-id="e4cc0-145">值</span><span class="sxs-lookup"><span data-stu-id="e4cc0-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e4cc0-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e4cc0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e4cc0-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4cc0-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e4cc0-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e4cc0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e4cc0-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e4cc0-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e4cc0-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4cc0-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="e4cc0-151">**參考**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e4cc0-152">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-152">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="e4cc0-153">**VerQueryValue**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-153">**VerQueryValue**</span></span>](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
</dt> <dt>

[<span data-ttu-id="e4cc0-154">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-154">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="e4cc0-155">**VS \_ FIXEDFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-155">**VS\_FIXEDFILEINFO**</span></span>](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo)
</dt> <dt>

<span data-ttu-id="e4cc0-156">**概念**</span><span class="sxs-lookup"><span data-stu-id="e4cc0-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e4cc0-157">版本資訊</span><span class="sxs-lookup"><span data-stu-id="e4cc0-157">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





