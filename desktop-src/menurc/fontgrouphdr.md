---
title: FONTGROUPHDR 結構
description: 包含應用程式存取特定字型所需的資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- FONTGROUPHDR 結構功能表和其他資源
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187303"
---
# <a name="fontgrouphdr-structure"></a><span data-ttu-id="da852-105">FONTGROUPHDR 結構</span><span class="sxs-lookup"><span data-stu-id="da852-105">FONTGROUPHDR structure</span></span>

<span data-ttu-id="da852-106">包含應用程式存取特定字型所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="da852-106">Contains the information necessary for an application to access a specific font.</span></span> <span data-ttu-id="da852-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="da852-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="da852-108">語法</span><span class="sxs-lookup"><span data-stu-id="da852-108">Syntax</span></span>


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a><span data-ttu-id="da852-109">成員</span><span class="sxs-lookup"><span data-stu-id="da852-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="da852-110">**NumberOfFonts**</span><span class="sxs-lookup"><span data-stu-id="da852-110">**NumberOfFonts**</span></span>
</dt> <dd>

<span data-ttu-id="da852-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="da852-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="da852-112">與此資源相關聯的個別字型數目。</span><span class="sxs-lookup"><span data-stu-id="da852-112">The number of individual fonts associated with this resource.</span></span>

</dd> <dt>

<span data-ttu-id="da852-113">**德**</span><span class="sxs-lookup"><span data-stu-id="da852-113">**DE**</span></span>
</dt> <dd>

<span data-ttu-id="da852-114">類型： **[ **DIRENTRY**](direntry.md)**</span><span class="sxs-lookup"><span data-stu-id="da852-114">Type: **[**DIRENTRY**](direntry.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da852-115">結構，其中包含資源中每個字型的唯一序數識別碼。</span><span class="sxs-lookup"><span data-stu-id="da852-115">A structure that contains a unique ordinal identifier for each font in the resource.</span></span> <span data-ttu-id="da852-116">**DE** 成員是 [**DIRENTRY**](direntry.md)結構的可變長度陣列的預留位置。</span><span class="sxs-lookup"><span data-stu-id="da852-116">The **DE** member is a placeholder for the variable-length array of [**DIRENTRY**](direntry.md) structures.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da852-117">備註</span><span class="sxs-lookup"><span data-stu-id="da852-117">Remarks</span></span>

<span data-ttu-id="da852-118">**FONTGROUPHDR** 結構會遵循中個別字型的資料。Res 檔。</span><span class="sxs-lookup"><span data-stu-id="da852-118">The **FONTGROUPHDR** structure follows the data for the individual fonts in the .Res file.</span></span> <span data-ttu-id="da852-119">資源編譯器會自動新增 **FONTGROUPHDR** 結構，通常是檔案中的最後一個專案。</span><span class="sxs-lookup"><span data-stu-id="da852-119">The resource compiler automatically adds the **FONTGROUPHDR** structure, generally as the last entry in the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="da852-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="da852-120">Requirements</span></span>



| <span data-ttu-id="da852-121">需求</span><span class="sxs-lookup"><span data-stu-id="da852-121">Requirement</span></span> | <span data-ttu-id="da852-122">值</span><span class="sxs-lookup"><span data-stu-id="da852-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="da852-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da852-123">Minimum supported client</span></span><br/> | <span data-ttu-id="da852-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da852-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="da852-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da852-125">Minimum supported server</span></span><br/> | <span data-ttu-id="da852-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da852-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="da852-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da852-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="da852-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="da852-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da852-129">**DIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="da852-129">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="da852-130">**FONTDIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="da852-130">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

<span data-ttu-id="da852-131">**概念**</span><span class="sxs-lookup"><span data-stu-id="da852-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="da852-132">資源</span><span class="sxs-lookup"><span data-stu-id="da852-132">Resources</span></span>](resources.md)
</dt> </dl>

 

 





