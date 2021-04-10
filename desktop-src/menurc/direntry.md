---
title: DIRENTRY 結構
description: 包含識別字型資源群組中個別字型的唯一序數。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- DIRENTRY 結構功能表和其他資源
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686040"
---
# <a name="direntry-structure"></a><span data-ttu-id="c4cac-105">DIRENTRY 結構</span><span class="sxs-lookup"><span data-stu-id="c4cac-105">DIRENTRY structure</span></span>

<span data-ttu-id="c4cac-106">包含識別字型資源群組中個別字型的唯一序數。</span><span class="sxs-lookup"><span data-stu-id="c4cac-106">Contains a unique ordinal that identifies an individual font in the font resource group.</span></span> <span data-ttu-id="c4cac-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="c4cac-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4cac-108">語法</span><span class="sxs-lookup"><span data-stu-id="c4cac-108">Syntax</span></span>


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a><span data-ttu-id="c4cac-109">成員</span><span class="sxs-lookup"><span data-stu-id="c4cac-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4cac-110">**fontOrdinal**</span><span class="sxs-lookup"><span data-stu-id="c4cac-110">**fontOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="c4cac-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="c4cac-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="c4cac-112">字型資源群組中個別字型的唯一序數識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4cac-112">A unique ordinal identifier for an individual font in a font resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4cac-113">備註</span><span class="sxs-lookup"><span data-stu-id="c4cac-113">Remarks</span></span>

<span data-ttu-id="c4cac-114">指定字型的 [**FONTDIRENTRY**](fontdirentry.md) 結構會直接遵循該字型的 **DIRENTRY** 結構。</span><span class="sxs-lookup"><span data-stu-id="c4cac-114">The [**FONTDIRENTRY**](fontdirentry.md) structure for the specified font directly follows the **DIRENTRY** structure for that font.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4cac-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4cac-115">Requirements</span></span>



| <span data-ttu-id="c4cac-116">需求</span><span class="sxs-lookup"><span data-stu-id="c4cac-116">Requirement</span></span> | <span data-ttu-id="c4cac-117">值</span><span class="sxs-lookup"><span data-stu-id="c4cac-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c4cac-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4cac-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c4cac-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4cac-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c4cac-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4cac-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c4cac-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4cac-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c4cac-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4cac-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4cac-123">**參考**</span><span class="sxs-lookup"><span data-stu-id="c4cac-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c4cac-124">**FONTDIRENTRY**</span><span class="sxs-lookup"><span data-stu-id="c4cac-124">**FONTDIRENTRY**</span></span>](fontdirentry.md)
</dt> <dt>

[<span data-ttu-id="c4cac-125">**FONTGROUPHDR**</span><span class="sxs-lookup"><span data-stu-id="c4cac-125">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="c4cac-126">**概念**</span><span class="sxs-lookup"><span data-stu-id="c4cac-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c4cac-127">資源</span><span class="sxs-lookup"><span data-stu-id="c4cac-127">Resources</span></span>](resources.md)
</dt> </dl>

 

 





