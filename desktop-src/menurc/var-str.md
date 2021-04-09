---
title: Var 結構
description: 代表檔案版本資源中的資料組織。 它通常會包含應用程式或 DLL 版本所支援的語言和字碼頁識別碼組清單。
ms.assetid: edd2f2e5-100c-49c2-841f-f75e2909460a
keywords:
- Var 結構功能表和其他資源
topic_type:
- apiref
api_name:
- Var
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 151103366e85537368cacb7063f199f1f91bf023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844299"
---
# <a name="var-structure"></a><span data-ttu-id="6c62a-105">Var 結構</span><span class="sxs-lookup"><span data-stu-id="6c62a-105">Var structure</span></span>

<span data-ttu-id="6c62a-106">代表檔案版本資源中的資料組織。</span><span class="sxs-lookup"><span data-stu-id="6c62a-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="6c62a-107">它通常會包含應用程式或 DLL 版本所支援的語言和字碼頁識別碼組清單。</span><span class="sxs-lookup"><span data-stu-id="6c62a-107">It typically contains a list of language and code page identifier pairs that the version of the application or DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c62a-108">語法</span><span class="sxs-lookup"><span data-stu-id="6c62a-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  DWORD Value;
} Var;
```



## <a name="members"></a><span data-ttu-id="6c62a-109">成員</span><span class="sxs-lookup"><span data-stu-id="6c62a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="6c62a-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="6c62a-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="6c62a-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="6c62a-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6c62a-112">**Var** 結構的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6c62a-112">The length, in bytes, of the **Var** structure.</span></span>

</dd> <dt>

<span data-ttu-id="6c62a-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="6c62a-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="6c62a-114">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="6c62a-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6c62a-115">**值** 成員的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6c62a-115">The length, in bytes, of the **Value** member.</span></span>

</dd> <dt>

<span data-ttu-id="6c62a-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="6c62a-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="6c62a-117">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="6c62a-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6c62a-118">版本資源中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="6c62a-118">The type of data in the version resource.</span></span> <span data-ttu-id="6c62a-119">如果版本資源包含文字資料，則此成員為1，如果版本資源包含二進位資料，則為0。</span><span class="sxs-lookup"><span data-stu-id="6c62a-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="6c62a-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="6c62a-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="6c62a-121">類型： **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="6c62a-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="6c62a-122">Unicode 字串 L 「轉譯」。</span><span class="sxs-lookup"><span data-stu-id="6c62a-122">The Unicode string L"Translation".</span></span>

</dd> <dt>

<span data-ttu-id="6c62a-123">**填補**</span><span class="sxs-lookup"><span data-stu-id="6c62a-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="6c62a-124">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="6c62a-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="6c62a-125">在32位界限上對齊 **值** 成員所需的任意零個單字。</span><span class="sxs-lookup"><span data-stu-id="6c62a-125">As many zero words as necessary to align the **Value** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="6c62a-126">**值**</span><span class="sxs-lookup"><span data-stu-id="6c62a-126">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="6c62a-127">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="6c62a-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="6c62a-128">一或多個值為語言和字碼頁識別碼組的陣列。</span><span class="sxs-lookup"><span data-stu-id="6c62a-128">An array of one or more values that are language and code page identifier pairs.</span></span> <span data-ttu-id="6c62a-129">如需詳細資訊，請參閱下列備註一節。</span><span class="sxs-lookup"><span data-stu-id="6c62a-129">For additional information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c62a-130">備註</span><span class="sxs-lookup"><span data-stu-id="6c62a-130">Remarks</span></span>

<span data-ttu-id="6c62a-131">此結構不是真正的 C 語言結構，因為它包含可變長度的成員。</span><span class="sxs-lookup"><span data-stu-id="6c62a-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="6c62a-132">此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="6c62a-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="6c62a-133">如果您使用 **Var** 結構來列出您的應用程式或 DLL 所支援的語言，而不是使用多個版本的資源，請使用 **Value** 成員來包含 **DWORD** 值陣列，指出此檔案所支援的語言和字碼頁組合。</span><span class="sxs-lookup"><span data-stu-id="6c62a-133">If you use the **Var** structure to list the languages your application or DLL supports instead of using multiple version resources, use the **Value** member to contain an array of **DWORD** values indicating the language and code page combinations supported by this file.</span></span> <span data-ttu-id="6c62a-134">每個 **DWORD** 的低序位字必須包含 Microsoft 語言識別項，而高序位單字必須包含 IBM 字碼頁編號。</span><span class="sxs-lookup"><span data-stu-id="6c62a-134">The low-order word of each **DWORD** must contain a Microsoft language identifier, and the high-order word must contain the IBM code page number.</span></span> <span data-ttu-id="6c62a-135">高序位或低序位的單字可以是零，表示檔案與語言或字碼頁無關。</span><span class="sxs-lookup"><span data-stu-id="6c62a-135">Either high-order or low-order word can be zero, indicating that the file is language or code page independent.</span></span> <span data-ttu-id="6c62a-136">如果省略了 **Var** 結構，檔案將會被視為與語言和字碼頁無關。</span><span class="sxs-lookup"><span data-stu-id="6c62a-136">If the **Var** structure is omitted, the file will be interpreted as both language and code page independent.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c62a-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c62a-137">Requirements</span></span>



| <span data-ttu-id="6c62a-138">需求</span><span class="sxs-lookup"><span data-stu-id="6c62a-138">Requirement</span></span> | <span data-ttu-id="6c62a-139">值</span><span class="sxs-lookup"><span data-stu-id="6c62a-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6c62a-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c62a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6c62a-141">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c62a-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6c62a-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c62a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6c62a-143">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c62a-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6c62a-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c62a-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="6c62a-145">**參考**</span><span class="sxs-lookup"><span data-stu-id="6c62a-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6c62a-146">**VarFileInfo**</span><span class="sxs-lookup"><span data-stu-id="6c62a-146">**VarFileInfo**</span></span>](varfileinfo.md)
</dt> <dt>

[<span data-ttu-id="6c62a-147">**StringFileInfo**</span><span class="sxs-lookup"><span data-stu-id="6c62a-147">**StringFileInfo**</span></span>](stringfileinfo.md)
</dt> <dt>

[<span data-ttu-id="6c62a-148">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="6c62a-148">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="6c62a-149">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="6c62a-149">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="6c62a-150">**概念**</span><span class="sxs-lookup"><span data-stu-id="6c62a-150">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6c62a-151">版本資訊</span><span class="sxs-lookup"><span data-stu-id="6c62a-151">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





