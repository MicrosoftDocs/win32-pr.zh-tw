---
title: VarFileInfo 結構
description: 代表檔案版本資源中的資料組織。 它包含不相依于特定語言和字碼頁組合的版本資訊。
ms.assetid: 3b667778-fb08-4195-a88e-ac04baf45fee
keywords:
- VarFileInfo 結構功能表和其他資源
topic_type:
- apiref
api_name:
- VarFileInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26326403abef41d131bf25acf5d5d8be7728cd0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965744"
---
# <a name="varfileinfo-structure"></a><span data-ttu-id="dbed9-105">VarFileInfo 結構</span><span class="sxs-lookup"><span data-stu-id="dbed9-105">VarFileInfo structure</span></span>

<span data-ttu-id="dbed9-106">代表檔案版本資源中的資料組織。</span><span class="sxs-lookup"><span data-stu-id="dbed9-106">Represents the organization of data in a file-version resource.</span></span> <span data-ttu-id="dbed9-107">它包含不相依于特定語言和字碼頁組合的版本資訊。</span><span class="sxs-lookup"><span data-stu-id="dbed9-107">It contains version information not dependent on a particular language and code page combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbed9-108">語法</span><span class="sxs-lookup"><span data-stu-id="dbed9-108">Syntax</span></span>


```C++
typedef struct {
  WORD  wLength;
  WORD  wValueLength;
  WORD  wType;
  WCHAR szKey;
  WORD  Padding;
  Var   Children;
} VarFileInfo;
```



## <a name="members"></a><span data-ttu-id="dbed9-109">成員</span><span class="sxs-lookup"><span data-stu-id="dbed9-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="dbed9-110">**wLength**</span><span class="sxs-lookup"><span data-stu-id="dbed9-110">**wLength**</span></span>
</dt> <dd>

<span data-ttu-id="dbed9-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="dbed9-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="dbed9-112">整個 **VarFileInfo** 區塊的長度（以位元組為單位），包括 **子** 成員所指示的所有結構。</span><span class="sxs-lookup"><span data-stu-id="dbed9-112">The length, in bytes, of the entire **VarFileInfo** block, including all structures indicated by the **Children** member.</span></span>

</dd> <dt>

<span data-ttu-id="dbed9-113">**wValueLength**</span><span class="sxs-lookup"><span data-stu-id="dbed9-113">**wValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="dbed9-114">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="dbed9-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="dbed9-115">這個成員永遠等於零。</span><span class="sxs-lookup"><span data-stu-id="dbed9-115">This member is always equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="dbed9-116">**wType**</span><span class="sxs-lookup"><span data-stu-id="dbed9-116">**wType**</span></span>
</dt> <dd>

<span data-ttu-id="dbed9-117">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="dbed9-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="dbed9-118">版本資源中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="dbed9-118">The type of data in the version resource.</span></span> <span data-ttu-id="dbed9-119">如果版本資源包含文字資料，則此成員為1，如果版本資源包含二進位資料，則為0。</span><span class="sxs-lookup"><span data-stu-id="dbed9-119">This member is 1 if the version resource contains text data and 0 if the version resource contains binary data.</span></span>

</dd> <dt>

<span data-ttu-id="dbed9-120">**szKey**</span><span class="sxs-lookup"><span data-stu-id="dbed9-120">**szKey**</span></span>
</dt> <dd>

<span data-ttu-id="dbed9-121">類型： **WCHAR**</span><span class="sxs-lookup"><span data-stu-id="dbed9-121">Type: **WCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="dbed9-122">Unicode 字串 L "VarFileInfo"。</span><span class="sxs-lookup"><span data-stu-id="dbed9-122">The Unicode string L"VarFileInfo".</span></span>

</dd> <dt>

<span data-ttu-id="dbed9-123">**填補**</span><span class="sxs-lookup"><span data-stu-id="dbed9-123">**Padding**</span></span>
</dt> <dd>

<span data-ttu-id="dbed9-124">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="dbed9-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="dbed9-125">在32位界限上對齊 **子** 成員所需的任意零個單字。</span><span class="sxs-lookup"><span data-stu-id="dbed9-125">As many zero words as necessary to align the **Children** member on a 32-bit boundary.</span></span>

</dd> <dt>

<span data-ttu-id="dbed9-126">**子系**</span><span class="sxs-lookup"><span data-stu-id="dbed9-126">**Children**</span></span>
</dt> <dd>

<span data-ttu-id="dbed9-127">類型： **[ **Var**](var-str.md)**</span><span class="sxs-lookup"><span data-stu-id="dbed9-127">Type: **[**Var**](var-str.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dbed9-128">通常會包含應用程式或 DLL 所支援的語言清單。</span><span class="sxs-lookup"><span data-stu-id="dbed9-128">Typically contains a list of languages that the application or DLL supports.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbed9-129">備註</span><span class="sxs-lookup"><span data-stu-id="dbed9-129">Remarks</span></span>

<span data-ttu-id="dbed9-130">此結構不是真正的 C 語言結構，因為它包含可變長度的成員。</span><span class="sxs-lookup"><span data-stu-id="dbed9-130">This structure is not a true C-language structure because it contains variable-length members.</span></span> <span data-ttu-id="dbed9-131">此結構是專門用來描述版本資源中的資料組織，而不會出現在隨附于 Windows 軟體開發套件 (SDK) 的任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="dbed9-131">This structure was created solely to depict the organization of data in a version resource and does not appear in any of the header files shipped with the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="dbed9-132">[**VS \_ VERSIONINFO**](vs-versioninfo.md)結構的 **子** 成員可以包含零個或一個 **VarFileInfo** 結構。</span><span class="sxs-lookup"><span data-stu-id="dbed9-132">The **Children** member of the [**VS\_VERSIONINFO**](vs-versioninfo.md) structure may contain zero or one **VarFileInfo** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbed9-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbed9-133">Requirements</span></span>



| <span data-ttu-id="dbed9-134">需求</span><span class="sxs-lookup"><span data-stu-id="dbed9-134">Requirement</span></span> | <span data-ttu-id="dbed9-135">值</span><span class="sxs-lookup"><span data-stu-id="dbed9-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="dbed9-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dbed9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dbed9-137">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbed9-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dbed9-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dbed9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dbed9-139">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dbed9-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="dbed9-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbed9-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="dbed9-141">**參考**</span><span class="sxs-lookup"><span data-stu-id="dbed9-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dbed9-142">**無 功**</span><span class="sxs-lookup"><span data-stu-id="dbed9-142">**Var**</span></span>](var-str.md)
</dt> <dt>

[<span data-ttu-id="dbed9-143">**VS \_ VERSIONINFO**</span><span class="sxs-lookup"><span data-stu-id="dbed9-143">**VS\_VERSIONINFO**</span></span>](vs-versioninfo.md)
</dt> <dt>

<span data-ttu-id="dbed9-144">**概念**</span><span class="sxs-lookup"><span data-stu-id="dbed9-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dbed9-145">版本資訊</span><span class="sxs-lookup"><span data-stu-id="dbed9-145">Version Information</span></span>](version-information.md)
</dt> </dl>

 

 





