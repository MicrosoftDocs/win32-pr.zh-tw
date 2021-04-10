---
title: NEWHEADER 結構
description: 包含資源群組中的圖示或游標元件數目。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- NEWHEADER 結構功能表和其他資源
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934052"
---
# <a name="newheader-structure"></a><span data-ttu-id="b74a3-105">NEWHEADER 結構</span><span class="sxs-lookup"><span data-stu-id="b74a3-105">NEWHEADER structure</span></span>

<span data-ttu-id="b74a3-106">包含資源群組中的圖示或游標元件數目。</span><span class="sxs-lookup"><span data-stu-id="b74a3-106">Contains the number of icon or cursor components in a resource group.</span></span> <span data-ttu-id="b74a3-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="b74a3-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b74a3-108">語法</span><span class="sxs-lookup"><span data-stu-id="b74a3-108">Syntax</span></span>


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a><span data-ttu-id="b74a3-109">成員</span><span class="sxs-lookup"><span data-stu-id="b74a3-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b74a3-110">**已保留**</span><span class="sxs-lookup"><span data-stu-id="b74a3-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b74a3-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="b74a3-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b74a3-112">保護必須為零。</span><span class="sxs-lookup"><span data-stu-id="b74a3-112">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b74a3-113">**Azuremmblobcontainer.restype**</span><span class="sxs-lookup"><span data-stu-id="b74a3-113">**ResType**</span></span>
</dt> <dd>

<span data-ttu-id="b74a3-114">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="b74a3-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b74a3-115">資源類型。</span><span class="sxs-lookup"><span data-stu-id="b74a3-115">The resource type.</span></span> <span data-ttu-id="b74a3-116">這個成員必須有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b74a3-116">This member must have one of the following values.</span></span>



| <span data-ttu-id="b74a3-117">值</span><span class="sxs-lookup"><span data-stu-id="b74a3-117">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="b74a3-118">意義</span><span class="sxs-lookup"><span data-stu-id="b74a3-118">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <span data-ttu-id="b74a3-119"><dt>**RES \_資料指標**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b74a3-119"><dt>**RES\_CURSOR**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b74a3-120">Cursor 資源類型。</span><span class="sxs-lookup"><span data-stu-id="b74a3-120">Cursor resource type.</span></span><br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <span data-ttu-id="b74a3-121"><dt>**RES \_圖示**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b74a3-121"><dt>**RES\_ICON**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="b74a3-122">圖示資源類型。</span><span class="sxs-lookup"><span data-stu-id="b74a3-122">Icon resource type.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="b74a3-123">**ResCount**</span><span class="sxs-lookup"><span data-stu-id="b74a3-123">**ResCount**</span></span>
</dt> <dd>

<span data-ttu-id="b74a3-124">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="b74a3-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="b74a3-125">資源群組中的圖示或游標元件數目。</span><span class="sxs-lookup"><span data-stu-id="b74a3-125">The number of icon or cursor components in the resource group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b74a3-126">備註</span><span class="sxs-lookup"><span data-stu-id="b74a3-126">Remarks</span></span>

<span data-ttu-id="b74a3-127">一或多個 [**RESDIR**](resdir.md) 結構會緊接在 .res 檔中的 **NEWHEADER** 結構後面。</span><span class="sxs-lookup"><span data-stu-id="b74a3-127">One or more [**RESDIR**](resdir.md) structures immediately follow the **NEWHEADER** structure in the .res file.</span></span> <span data-ttu-id="b74a3-128">**ResCount** 成員會指定 **RESDIR** 結構的數目。</span><span class="sxs-lookup"><span data-stu-id="b74a3-128">The **ResCount** member specifies the number of **RESDIR** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="b74a3-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b74a3-129">Requirements</span></span>



| <span data-ttu-id="b74a3-130">需求</span><span class="sxs-lookup"><span data-stu-id="b74a3-130">Requirement</span></span> | <span data-ttu-id="b74a3-131">值</span><span class="sxs-lookup"><span data-stu-id="b74a3-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b74a3-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b74a3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b74a3-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b74a3-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b74a3-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b74a3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b74a3-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b74a3-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b74a3-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b74a3-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="b74a3-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="b74a3-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b74a3-138">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="b74a3-138">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="b74a3-139">**概念**</span><span class="sxs-lookup"><span data-stu-id="b74a3-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b74a3-140">資源</span><span class="sxs-lookup"><span data-stu-id="b74a3-140">Resources</span></span>](resources.md)
</dt> </dl>

 

 





