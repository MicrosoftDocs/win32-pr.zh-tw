---
title: CURSORDIR 結構
description: 包含資源群組中個別資料指標影像的維度。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- CURSORDIR 結構功能表和其他資源
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385126"
---
# <a name="cursordir-structure"></a><span data-ttu-id="8384c-105">CURSORDIR 結構</span><span class="sxs-lookup"><span data-stu-id="8384c-105">CURSORDIR structure</span></span>

<span data-ttu-id="8384c-106">包含資源群組中個別資料指標影像的維度。</span><span class="sxs-lookup"><span data-stu-id="8384c-106">Contains the dimensions of an individual cursor image in a resource group.</span></span> <span data-ttu-id="8384c-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="8384c-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8384c-108">語法</span><span class="sxs-lookup"><span data-stu-id="8384c-108">Syntax</span></span>


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a><span data-ttu-id="8384c-109">成員</span><span class="sxs-lookup"><span data-stu-id="8384c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8384c-110">**寬度**</span><span class="sxs-lookup"><span data-stu-id="8384c-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="8384c-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="8384c-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="8384c-112">游標的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="8384c-112">The width of the cursor, in pixels.</span></span> <span data-ttu-id="8384c-113">可接受的值為16、32和64。</span><span class="sxs-lookup"><span data-stu-id="8384c-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="8384c-114">**高度**</span><span class="sxs-lookup"><span data-stu-id="8384c-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="8384c-115">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="8384c-115">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="8384c-116">資料指標的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="8384c-116">The height of the cursor, in pixels.</span></span> <span data-ttu-id="8384c-117">可接受的值為16、32和64。</span><span class="sxs-lookup"><span data-stu-id="8384c-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8384c-118">備註</span><span class="sxs-lookup"><span data-stu-id="8384c-118">Remarks</span></span>

<span data-ttu-id="8384c-119">如果 **RESDIR** 結構描述資料指標，則會在 [**RESDIR**](resdir.md)結構中傳遞 **CURSORDIR** 結構。</span><span class="sxs-lookup"><span data-stu-id="8384c-119">The **CURSORDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="8384c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="8384c-120">Requirements</span></span>



| <span data-ttu-id="8384c-121">需求</span><span class="sxs-lookup"><span data-stu-id="8384c-121">Requirement</span></span> | <span data-ttu-id="8384c-122">值</span><span class="sxs-lookup"><span data-stu-id="8384c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8384c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8384c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8384c-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8384c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8384c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8384c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8384c-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8384c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8384c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8384c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="8384c-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="8384c-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8384c-129">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="8384c-129">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="8384c-130">**概念**</span><span class="sxs-lookup"><span data-stu-id="8384c-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8384c-131">資源</span><span class="sxs-lookup"><span data-stu-id="8384c-131">Resources</span></span>](resources.md)
</dt> </dl>

 

 





