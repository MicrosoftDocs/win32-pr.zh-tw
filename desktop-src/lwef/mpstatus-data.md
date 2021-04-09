---
title: 'MPSTATUS_DATA 結構 (MpClient .h) '
description: 包含產品元件目前狀態的相關資料。
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA 結構舊版 Windows 環境功能
- PMPSTATUS_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686108"
---
# <a name="mpstatus_data-structure"></a><span data-ttu-id="f760d-105">MPSTATUS \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="f760d-105">MPSTATUS\_DATA structure</span></span>

<span data-ttu-id="f760d-106">包含產品元件目前狀態的相關資料。</span><span class="sxs-lookup"><span data-stu-id="f760d-106">Contains data about the current status of a component of the product.</span></span>

## <a name="syntax"></a><span data-ttu-id="f760d-107">語法</span><span class="sxs-lookup"><span data-stu-id="f760d-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a><span data-ttu-id="f760d-108">成員</span><span class="sxs-lookup"><span data-stu-id="f760d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f760d-109">**ComponentID**</span><span class="sxs-lookup"><span data-stu-id="f760d-109">**ComponentID**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-110">類型： **[ **MPCOMPONENT \_ 識別碼**](mpcomponent-id.md)**</span><span class="sxs-lookup"><span data-stu-id="f760d-110">Type: **[**MPCOMPONENT\_ID**](mpcomponent-id.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-111">報告狀態的特定元件識別碼。</span><span class="sxs-lookup"><span data-stu-id="f760d-111">Specific component ID for which status is reported.</span></span>

</dd> <dt>

<span data-ttu-id="f760d-112">**fEnable**</span><span class="sxs-lookup"><span data-stu-id="f760d-112">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-113">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="f760d-113">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-114">元件的要求狀態。</span><span class="sxs-lookup"><span data-stu-id="f760d-114">Status requested for the component.</span></span> <span data-ttu-id="f760d-115">回呼資料中的 **hResult** 表示要求成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="f760d-115">**hResult** in the callback data signifies success or failure for the request.</span></span>

</dd> <dt>

<span data-ttu-id="f760d-116">**ComponentStatus**</span><span class="sxs-lookup"><span data-stu-id="f760d-116">**ComponentStatus**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-117">根據 **元件** 值的額外狀態資料。</span><span class="sxs-lookup"><span data-stu-id="f760d-117">Extra status data depending on value of **ComponentID**.</span></span>

> [!Note]  
> <span data-ttu-id="f760d-118">目前會導致所有適用于 **元件** 的可能值的虛擬結構指標。</span><span class="sxs-lookup"><span data-stu-id="f760d-118">Currently results in a pointer to a dummy structure for all possible values of **ComponentID**.</span></span>

 

<dl> <dt>

<span data-ttu-id="f760d-119">**p1**</span><span class="sxs-lookup"><span data-stu-id="f760d-119">**p1**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-120">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-120">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-121">當 **元件**  ==  **MPCOMPONENT \_ 為 \_** 簽章時。</span><span class="sxs-lookup"><span data-stu-id="f760d-121">When **ComponentID** == **MPCOMPONENT\_AS\_SIGNATURE**.</span></span> <span data-ttu-id="f760d-122">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-122">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="f760d-123">**又**</span><span class="sxs-lookup"><span data-stu-id="f760d-123">**p2**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-124">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-124">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-125">當 **元件**  ==  **MPCOMPONENT \_ AV \_** 簽章時。</span><span class="sxs-lookup"><span data-stu-id="f760d-125">When **ComponentID** == **MPCOMPONENT\_AV\_SIGNATURE**.</span></span> <span data-ttu-id="f760d-126">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-126">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="f760d-127">**p3**</span><span class="sxs-lookup"><span data-stu-id="f760d-127">**p3**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-128">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-128">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-129">當 **元件**  ==  **MPCOMPONENT \_ 即時 \_ 監視** 時。</span><span class="sxs-lookup"><span data-stu-id="f760d-129">When **ComponentID** == **MPCOMPONENT\_REALTIME\_MONITOR**.</span></span> <span data-ttu-id="f760d-130">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-130">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="f760d-131">**p4**</span><span class="sxs-lookup"><span data-stu-id="f760d-131">**p4**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-132">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-132">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-133">當 **元件**  ==  **MPCOMPONENT \_ ONACCESS \_ 保護** 時。</span><span class="sxs-lookup"><span data-stu-id="f760d-133">When **ComponentID** == **MPCOMPONENT\_ONACCESS\_PROTECTION**.</span></span> <span data-ttu-id="f760d-134">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-134">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="f760d-135">**p5**</span><span class="sxs-lookup"><span data-stu-id="f760d-135">**p5**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-136">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-136">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-137">當 **元件**  ==  **MPCOMPONENT \_ IOAV \_ 保護** 時。</span><span class="sxs-lookup"><span data-stu-id="f760d-137">When **ComponentID** == **MPCOMPONENT\_IOAV\_PROTECTION**.</span></span> <span data-ttu-id="f760d-138">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-138">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="f760d-139">**p6**</span><span class="sxs-lookup"><span data-stu-id="f760d-139">**p6**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-140">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-140">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-141">當 **元件**  ==  **MPCOMPONENT \_ 行為 \_ 監視器** 時。</span><span class="sxs-lookup"><span data-stu-id="f760d-141">When **ComponentID** == **MPCOMPONENT\_BEHAVIOR\_MONITOR**.</span></span> <span data-ttu-id="f760d-142">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-142">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="f760d-143">**p7**</span><span class="sxs-lookup"><span data-stu-id="f760d-143">**p7**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-144">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-144">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-145">當 **元件**  ==  **MPCOMPONENT \_ 自動 \_ 掃描** 時。</span><span class="sxs-lookup"><span data-stu-id="f760d-145">When **ComponentID** == **MPCOMPONENT\_AUTO\_SCAN**.</span></span> <span data-ttu-id="f760d-146">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-146">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="f760d-147">**p8**</span><span class="sxs-lookup"><span data-stu-id="f760d-147">**p8**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-148">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-148">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-149">當 **元件**  ==  **MPCOMPONENT \_ 自動 \_ SIGUPDATE** 時。</span><span class="sxs-lookup"><span data-stu-id="f760d-149">When **ComponentID** == **MPCOMPONENT\_AUTO\_SIGUPDATE**.</span></span> <span data-ttu-id="f760d-150">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-150">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="f760d-151">**p9**</span><span class="sxs-lookup"><span data-stu-id="f760d-151">**p9**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-152">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-152">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-153">當 **元件**  ==  **MPCOMPONENT \_ IPC** 時。</span><span class="sxs-lookup"><span data-stu-id="f760d-153">When **ComponentID** == **MPCOMPONENT\_IPC**.</span></span> <span data-ttu-id="f760d-154">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-154">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="f760d-155">**pa**</span><span class="sxs-lookup"><span data-stu-id="f760d-155">**pa**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-156">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-156">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-157">當 **元件**  ==  **MPCOMPONENT \_ NIS** 時。</span><span class="sxs-lookup"><span data-stu-id="f760d-157">When **ComponentID** == **MPCOMPONENT\_NIS**.</span></span> <span data-ttu-id="f760d-158">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-158">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="f760d-159">**鉛**</span><span class="sxs-lookup"><span data-stu-id="f760d-159">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="f760d-160">類型： **\_ \_ 未使用的 PMPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-160">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="f760d-161">當 **元件**  ==  **MPCOMPONENT \_ ELAM** 時。</span><span class="sxs-lookup"><span data-stu-id="f760d-161">When **ComponentID** == **MPCOMPONENT\_ELAM**.</span></span> <span data-ttu-id="f760d-162">請參閱 [**MPSTATUS \_ DATAEX \_ 未使用**](mpstatus-dataex-unused.md)。</span><span class="sxs-lookup"><span data-stu-id="f760d-162">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f760d-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="f760d-163">Requirements</span></span>



| <span data-ttu-id="f760d-164">需求</span><span class="sxs-lookup"><span data-stu-id="f760d-164">Requirement</span></span> | <span data-ttu-id="f760d-165">值</span><span class="sxs-lookup"><span data-stu-id="f760d-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f760d-166">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f760d-166">Minimum supported client</span></span><br/> | <span data-ttu-id="f760d-167">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f760d-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f760d-168">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f760d-168">Minimum supported server</span></span><br/> | <span data-ttu-id="f760d-169">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f760d-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f760d-170">標頭</span><span class="sxs-lookup"><span data-stu-id="f760d-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="f760d-171"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="f760d-171"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f760d-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f760d-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f760d-173">**MPCOMPONENT \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="f760d-173">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="f760d-174">**\_ \_ 未使用的 MPSTATUS DATAEX**</span><span class="sxs-lookup"><span data-stu-id="f760d-174">**MPSTATUS\_DATAEX\_UNUSED**</span></span>](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





