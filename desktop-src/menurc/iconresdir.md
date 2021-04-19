---
title: ICONRESDIR 結構
description: 包含資源群組中個別圖示影像的維度和色彩格式。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- ICONRESDIR 結構功能表和其他資源
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968563"
---
# <a name="iconresdir-structure"></a><span data-ttu-id="c02cf-105">ICONRESDIR 結構</span><span class="sxs-lookup"><span data-stu-id="c02cf-105">ICONRESDIR structure</span></span>

<span data-ttu-id="c02cf-106">包含資源群組中個別圖示影像的維度和色彩格式。</span><span class="sxs-lookup"><span data-stu-id="c02cf-106">Contains the dimensions and color format of an individual icon image in a resource group.</span></span> <span data-ttu-id="c02cf-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="c02cf-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c02cf-108">語法</span><span class="sxs-lookup"><span data-stu-id="c02cf-108">Syntax</span></span>


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a><span data-ttu-id="c02cf-109">成員</span><span class="sxs-lookup"><span data-stu-id="c02cf-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c02cf-110">**寬度**</span><span class="sxs-lookup"><span data-stu-id="c02cf-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="c02cf-111">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="c02cf-111">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="c02cf-112">圖示的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c02cf-112">The width of the icon, in pixels.</span></span> <span data-ttu-id="c02cf-113">可接受的值為16、32和64。</span><span class="sxs-lookup"><span data-stu-id="c02cf-113">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="c02cf-114">**高度**</span><span class="sxs-lookup"><span data-stu-id="c02cf-114">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="c02cf-115">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="c02cf-115">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="c02cf-116">圖示的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="c02cf-116">The height of the icon, in pixels.</span></span> <span data-ttu-id="c02cf-117">可接受的值為16、32和64。</span><span class="sxs-lookup"><span data-stu-id="c02cf-117">Acceptable values are 16, 32, and 64.</span></span>

</dd> <dt>

<span data-ttu-id="c02cf-118">**ColorCount**</span><span class="sxs-lookup"><span data-stu-id="c02cf-118">**ColorCount**</span></span>
</dt> <dd>

<span data-ttu-id="c02cf-119">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="c02cf-119">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="c02cf-120">圖示中的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="c02cf-120">The number of colors in the icon.</span></span> <span data-ttu-id="c02cf-121">可接受的值為2、8和16。</span><span class="sxs-lookup"><span data-stu-id="c02cf-121">Acceptable values are 2, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="c02cf-122">**保留**</span><span class="sxs-lookup"><span data-stu-id="c02cf-122">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="c02cf-123">類型： **位元組**</span><span class="sxs-lookup"><span data-stu-id="c02cf-123">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="c02cf-124">保護必須設定為圖示檔案標頭中保留字段的相同值。</span><span class="sxs-lookup"><span data-stu-id="c02cf-124">Reserved; must be set to the same value as that of the reserved field in the icon file header.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c02cf-125">備註</span><span class="sxs-lookup"><span data-stu-id="c02cf-125">Remarks</span></span>

<span data-ttu-id="c02cf-126">如果 **RESDIR** 結構描述圖示，則會在 [**RESDIR**](resdir.md)結構中傳遞 **ICONRESDIR** 結構。</span><span class="sxs-lookup"><span data-stu-id="c02cf-126">The **ICONRESDIR** structure is passed in the [**RESDIR**](resdir.md) structure if the **RESDIR** structure describes an icon.</span></span>

## <a name="requirements"></a><span data-ttu-id="c02cf-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c02cf-127">Requirements</span></span>



| <span data-ttu-id="c02cf-128">需求</span><span class="sxs-lookup"><span data-stu-id="c02cf-128">Requirement</span></span> | <span data-ttu-id="c02cf-129">值</span><span class="sxs-lookup"><span data-stu-id="c02cf-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c02cf-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c02cf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c02cf-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c02cf-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c02cf-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c02cf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c02cf-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c02cf-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="c02cf-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c02cf-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="c02cf-135">**參考**</span><span class="sxs-lookup"><span data-stu-id="c02cf-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c02cf-136">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="c02cf-136">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="c02cf-137">**概念**</span><span class="sxs-lookup"><span data-stu-id="c02cf-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c02cf-138">資源</span><span class="sxs-lookup"><span data-stu-id="c02cf-138">Resources</span></span>](resources.md)
</dt> </dl>

 

 





