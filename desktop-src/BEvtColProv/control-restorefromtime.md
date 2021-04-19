---
description: 從以時間戳記選取的備份檔案還原收集器的使用中設定。
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Control 類別的 RestoreFromTime 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998440"
---
# <a name="restorefromtime-method-of-the-control-class"></a><span data-ttu-id="fe20f-103">Control 類別的 RestoreFromTime 方法</span><span class="sxs-lookup"><span data-stu-id="fe20f-103">RestoreFromTime method of the Control class</span></span>

<span data-ttu-id="fe20f-104">從以時間戳記選取的備份檔案還原收集器的使用中設定。</span><span class="sxs-lookup"><span data-stu-id="fe20f-104">Restore the active configuration of the collector from a backup file, selected by a timestamp.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe20f-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe20f-105">Syntax</span></span>


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="fe20f-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe20f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe20f-107">*TargetTimestampLow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-107">*TargetTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-108">請在此時間戳記還原至備份檔案。</span><span class="sxs-lookup"><span data-stu-id="fe20f-108">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="fe20f-109">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="fe20f-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-110">*TargetTimestampHigh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-110">*TargetTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-111">請在此時間戳記還原至備份檔案。</span><span class="sxs-lookup"><span data-stu-id="fe20f-111">Restore to the backup file at this timestamp.</span></span> <span data-ttu-id="fe20f-112">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="fe20f-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-113">*OldTimestampLow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-113">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-114">設定先前設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="fe20f-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="fe20f-115">如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用新的設定。</span><span class="sxs-lookup"><span data-stu-id="fe20f-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="fe20f-116">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="fe20f-116">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-117">*OldTimestampHigh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-117">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-118">設定先前設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="fe20f-118">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="fe20f-119">如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用新的設定。</span><span class="sxs-lookup"><span data-stu-id="fe20f-119">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="fe20f-120">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="fe20f-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-121">*NewTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-121">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-122">如果呼叫成功，則為設定新設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="fe20f-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="fe20f-123">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="fe20f-123">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-124">*NewTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-124">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-125">如果呼叫成功，則為設定新設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="fe20f-125">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="fe20f-126">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="fe20f-126">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-127">*OriginalTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-127">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-128">第一次設定還原設定時的原始時間戳記。</span><span class="sxs-lookup"><span data-stu-id="fe20f-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="fe20f-129">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="fe20f-129">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-130">*OriginalTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-130">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-131">第一次設定還原設定時的原始時間戳記。</span><span class="sxs-lookup"><span data-stu-id="fe20f-131">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="fe20f-132">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="fe20f-132">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-133">*ErrorString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-133">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-134">包含錯誤說明的文字字串。</span><span class="sxs-lookup"><span data-stu-id="fe20f-134">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-135">*WarningString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-135">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-136">具有警告的文字字串。</span><span class="sxs-lookup"><span data-stu-id="fe20f-136">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-137">*InfoString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-137">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-138">包含設定相關資訊的文字字串。</span><span class="sxs-lookup"><span data-stu-id="fe20f-138">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-139">*ErrorType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-139">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-140">錯誤的類型：請注意，0或不存在表示成功。</span><span class="sxs-lookup"><span data-stu-id="fe20f-140">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="fe20f-141">0</span><span class="sxs-lookup"><span data-stu-id="fe20f-141">0</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-142">成功。</span><span class="sxs-lookup"><span data-stu-id="fe20f-142">Success.</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-143">1</span><span class="sxs-lookup"><span data-stu-id="fe20f-143">1</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-144">錯誤引數格式</span><span class="sxs-lookup"><span data-stu-id="fe20f-144">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-145">2</span><span class="sxs-lookup"><span data-stu-id="fe20f-145">2</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-146">錯誤的引數值</span><span class="sxs-lookup"><span data-stu-id="fe20f-146">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-147">3</span><span class="sxs-lookup"><span data-stu-id="fe20f-147">3</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-148">資源 (通訊端) 開啟錯誤</span><span class="sxs-lookup"><span data-stu-id="fe20f-148">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-149">4</span><span class="sxs-lookup"><span data-stu-id="fe20f-149">4</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-150">持續性 (檔案寫入) 錯誤</span><span class="sxs-lookup"><span data-stu-id="fe20f-150">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="fe20f-151">5</span><span class="sxs-lookup"><span data-stu-id="fe20f-151">5</span></span>
</dt> <dd>

<span data-ttu-id="fe20f-152">不可部分完成性錯誤 (舊的時間戳記不相符) </span><span class="sxs-lookup"><span data-stu-id="fe20f-152">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe20f-153">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe20f-153">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="fe20f-154">0</span><span class="sxs-lookup"><span data-stu-id="fe20f-154">0</span></span>

<span data-ttu-id="fe20f-155">失敗</span><span class="sxs-lookup"><span data-stu-id="fe20f-155">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fe20f-156">1</span><span class="sxs-lookup"><span data-stu-id="fe20f-156">1</span></span>

<span data-ttu-id="fe20f-157">Success</span><span class="sxs-lookup"><span data-stu-id="fe20f-157">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe20f-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe20f-158">Requirements</span></span>



| <span data-ttu-id="fe20f-159">需求</span><span class="sxs-lookup"><span data-stu-id="fe20f-159">Requirement</span></span> | <span data-ttu-id="fe20f-160">值</span><span class="sxs-lookup"><span data-stu-id="fe20f-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe20f-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe20f-161">Minimum supported client</span></span><br/> | <span data-ttu-id="fe20f-162">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe20f-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fe20f-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe20f-163">Minimum supported server</span></span><br/> | <span data-ttu-id="fe20f-164">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fe20f-164">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="fe20f-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="fe20f-165">Namespace</span></span><br/>                | <span data-ttu-id="fe20f-166">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="fe20f-166">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="fe20f-167">MOF</span><span class="sxs-lookup"><span data-stu-id="fe20f-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe20f-168"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe20f-168"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe20f-169">DLL</span><span class="sxs-lookup"><span data-stu-id="fe20f-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe20f-170"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fe20f-170"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fe20f-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe20f-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe20f-172">**控制**</span><span class="sxs-lookup"><span data-stu-id="fe20f-172">**Control**</span></span>](control.md)
</dt> </dl>

 

