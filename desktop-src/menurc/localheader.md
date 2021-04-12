---
title: LOCALHEADER 結構
description: 包含與 RESDIR 結構所識別之資料指標相關聯之作用點的 x 和 y 座標。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- LOCALHEADER 結構功能表和其他資源
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384849"
---
# <a name="localheader-structure"></a><span data-ttu-id="3402f-105">LOCALHEADER 結構</span><span class="sxs-lookup"><span data-stu-id="3402f-105">LOCALHEADER structure</span></span>

<span data-ttu-id="3402f-106">包含與 [**RESDIR**](resdir.md) 結構所識別之資料指標相關聯之作用點的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="3402f-106">Contains the x- and y-coordinates of a hotspot associated with the cursor identified by a [**RESDIR**](resdir.md) structure.</span></span> <span data-ttu-id="3402f-107">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="3402f-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3402f-108">語法</span><span class="sxs-lookup"><span data-stu-id="3402f-108">Syntax</span></span>


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a><span data-ttu-id="3402f-109">成員</span><span class="sxs-lookup"><span data-stu-id="3402f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="3402f-110">**xHotSpot**</span><span class="sxs-lookup"><span data-stu-id="3402f-110">**xHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="3402f-111">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="3402f-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3402f-112">游標作用點的 x 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="3402f-112">The x-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="3402f-113">**yHotSpot**</span><span class="sxs-lookup"><span data-stu-id="3402f-113">**yHotSpot**</span></span>
</dt> <dd>

<span data-ttu-id="3402f-114">類型： **WORD**</span><span class="sxs-lookup"><span data-stu-id="3402f-114">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="3402f-115">游標作用點的 y 座標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="3402f-115">The y-coordinate of the cursor hot spot, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3402f-116">備註</span><span class="sxs-lookup"><span data-stu-id="3402f-116">Remarks</span></span>

<span data-ttu-id="3402f-117">如果 [**RESDIR**](resdir.md)結構包含資料指標的相關資訊， **LOCALHEADER** 結構就是寫入 [RT 資料 \_ 指標](/windows/desktop/menurc/resource-types)資源的第一個資料。</span><span class="sxs-lookup"><span data-stu-id="3402f-117">The **LOCALHEADER** structure is the first data written to the [RT\_CURSOR](/windows/desktop/menurc/resource-types) resource if a [**RESDIR**](resdir.md) structure contains information about a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="3402f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3402f-118">Requirements</span></span>



| <span data-ttu-id="3402f-119">需求</span><span class="sxs-lookup"><span data-stu-id="3402f-119">Requirement</span></span> | <span data-ttu-id="3402f-120">值</span><span class="sxs-lookup"><span data-stu-id="3402f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3402f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3402f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3402f-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3402f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3402f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3402f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3402f-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3402f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3402f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3402f-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3402f-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="3402f-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3402f-127">**CURSORDIR**</span><span class="sxs-lookup"><span data-stu-id="3402f-127">**CURSORDIR**</span></span>](cursordir.md)
</dt> <dt>

[<span data-ttu-id="3402f-128">**RESDIR**</span><span class="sxs-lookup"><span data-stu-id="3402f-128">**RESDIR**</span></span>](resdir.md)
</dt> <dt>

<span data-ttu-id="3402f-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="3402f-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3402f-130">資源</span><span class="sxs-lookup"><span data-stu-id="3402f-130">Resources</span></span>](resources.md)
</dt> </dl>

 

