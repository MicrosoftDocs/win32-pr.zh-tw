---
title: StringFileInfo 結構
description: 代表檔案版本資源中的資料組織。 它包含可以針對特定語言和字碼頁顯示的版本資訊。
ms.assetid: dda38fee-e8ea-4e58-b5ee-72e4cdb08f42
keywords:
- StringFileInfo 結構功能表和其他資源
topic_type:
- apiref
api_name:
- StringFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f252077a5536194e635281d4b4178a457f7a82cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934049"
---
# <a name="stringfileinfo-structure"></a><span data-ttu-id="24900-105">StringFileInfo 結構</span><span class="sxs-lookup"><span data-stu-id="24900-105">StringFileInfo structure</span></span>

<span data-ttu-id="24900-106">代表檔案版本資源中的資料組織。</span><span class="sxs-lookup"><span data-stu-id="24900-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="24900-107">它包含可以針對特定語言和字碼頁顯示的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="24900-107">It contains version information that can be displayed for a particular language and code page.</span></span>

## <a name="syntax"></a><span data-ttu-id="24900-108">語法</span><span class="sxs-lookup"><span data-stu-id="24900-108">Syntax</span></span>


```C++
typedef struct {
  WORD        wLength;
  WORD        wValueLength;
  WORD        wType;
  WCHAR       szKey;
  WORD        Padding;
  StringTable Children;
} StringFileInfo;
```



## <a name="members"></a><span data-ttu-id="24900-109">成員</span><span class="sxs-lookup"><span data-stu-id="24900-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="24900-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="24900-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="24900-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="24900-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="24900-112">整個 **StringFileInfo** 區塊的長度（以位元組為單位），包括 **子** 成員所指示的所有結構。</span><span class="sxs-lookup"><span data-stu-id="24900-112">The length, in bytes, of the entire **StringFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="24900-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="24900-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="24900-114">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="24900-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="24900-115">這個成員永遠等於零。</span><span class="sxs-lookup"><span data-stu-id="24900-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="24900-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="24900-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="24900-117">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="24900-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="24900-118">版本資源中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="24900-118">The type of data in the version resource.</span></span> <span data-ttu-id="24900-119">如果版本資源包含文字資料，則此成員為1，如果版本資源包含二進位資料，則為0。</span><span class="sxs-lookup"><span data-stu-id="24900-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="24900-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="24900-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="24900-121">類型： **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="24900-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="24900-122">Unicode 字串 L "StringFileInfo"。</span><span class="sxs-lookup"><span data-stu-id="24900-122">The Unicode string L"StringFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="24900-123">**填補**</span><span class="sxs-lookup"><span data-stu-id="24900-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="24900-124">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="24900-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="24900-125">在32位界限上對齊 **子** 成員所需的任意零個單字。</span><span class="sxs-lookup"><span data-stu-id="24900-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="24900-126">**子系**</span><span class="sxs-lookup"><span data-stu-id="24900-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="24900-127">類型： **[ **StringTable**](stringtable.md)**</span><span class="sxs-lookup"><span data-stu-id="24900-127">Type: **[**StringTable**](stringtable.md)**</span></span>

</dd> <dd>

<span data-ttu-id="24900-128">一或多個 [**StringTable**](stringtable.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="24900-128">An array of one or more [**StringTable**](stringtable.md) structures.</span></span> <span data-ttu-id="24900-129">每個 **StringTable** 結構的 **szKey** 成員都會指出適當的語言和字碼頁，以顯示該 **StringTable** 結構中的文字。</span><span class="sxs-lookup"><span data-stu-id="24900-129">Each **StringTable** structure's **szKey** member indicates the appropriate language and code page for displaying the text in that **StringTable** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24900-130">備註</span><span class="sxs-lookup"><span data-stu-id="24900-130">Remarks</span></span>

<span data-ttu-id="24900-131">此結構不是真正的 C 語言結構，因為它包含可變長度的成員。</span><span class="sxs-lookup"><span data-stu-id="24900-131">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="24900-132">此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="24900-132">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="24900-133">[**VS \_ VERSIONINFO**](vs-versioninfo.md)結構的 **子** 成員可以包含零或多個 **StringFileInfo** 結構。</span><span class="sxs-lookup"><span data-stu-id="24900-133">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or more **StringFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="24900-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="24900-134">Requirements</span></span>



| <span data-ttu-id="24900-135">需求</span><span class="sxs-lookup"><span data-stu-id="24900-135">Requirement</span></span> | <span data-ttu-id="24900-136">值</span><span class="sxs-lookup"><span data-stu-id="24900-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="24900-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24900-137">Minimum supported client</span></span><br/> | <span data-ttu-id="24900-138">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24900-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="24900-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24900-139">Minimum supported server</span></span><br/> | <span data-ttu-id="24900-140">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24900-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="24900-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24900-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="24900-142">**參考**</span><span class="sxs-lookup"><span data-stu-id="24900-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24900-143">**StringTable**</span><span class="sxs-lookup"><span data-stu-id="24900-143">**StringTable**</span></span>](stringtable.md)
</dt> <dt>

[<span data-ttu-id="24900-144">**字串**</span><span class="sxs-lookup"><span data-stu-id="24900-144">**String**</span></span>](string-str.md)
</dt> <dt>

[<span data-ttu-id="24900-145">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="24900-145">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="24900-146">**概念**</span><span class="sxs-lookup"><span data-stu-id="24900-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="24900-147">版本資訊</span><span class="sxs-lookup"><span data-stu-id="24900-147">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





