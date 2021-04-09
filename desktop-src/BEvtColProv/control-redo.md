---
description: 從較新的備份檔案中重設收集器的使用中設定， (從目前的原始時間戳記) 開始判斷。 如果設定已復原，這表示會重做復原的變更。
ms.assetid: bd153ea3-9148-4e65-a44e-3f9fa1855f2f
ms.tgt_platform: multiple
title: Control 類別的重做方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Redo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5ed77aac62dca0bf81ed13474e8acebb0235ea71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110057"
---
# <a name="redo-method-of-the-control-class"></a><span data-ttu-id="4e1e4-104">Control 類別的重做方法</span><span class="sxs-lookup"><span data-stu-id="4e1e4-104">Redo method of the Control class</span></span>

<span data-ttu-id="4e1e4-105">從較新的備份檔案中重設收集器的使用中設定， (從目前的原始時間戳記) 開始判斷。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-105">Reset the active configuration of the collector from the later backup file (determined by going forward from the current original timestamp).</span></span> <span data-ttu-id="4e1e4-106">如果設定已復原，這表示會重做復原的變更。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-106">If the configuration has been undone, this means redoing the undone change.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1e4-107">語法</span><span class="sxs-lookup"><span data-stu-id="4e1e4-107">Syntax</span></span>


```mof
Uint32 Redo(
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



## <a name="parameters"></a><span data-ttu-id="4e1e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="4e1e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1e4-109">*OldTimestampLow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-110">設定先前設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="4e1e4-111">如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用新的設定。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="4e1e4-112">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-113">*OldTimestampHigh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-114">設定先前設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="4e1e4-115">如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用新的設定。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="4e1e4-116">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-117">*NewTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-118">如果呼叫成功，則為設定新設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="4e1e4-119">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-120">*NewTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-121">如果呼叫成功，則為設定新設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="4e1e4-122">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-123">*OriginalTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-124">第一次設定還原設定時的原始時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="4e1e4-125">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-126">*OriginalTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-127">第一次設定還原設定時的原始時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="4e1e4-128">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-129">*ErrorString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-130">包含錯誤說明的文字字串。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-131">*WarningString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-132">具有警告的文字字串。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-133">*InfoString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-134">包含設定相關資訊的文字字串。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-135">*ErrorType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-136">錯誤的類型。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-136">The type of the error.</span></span> <span data-ttu-id="4e1e4-137">請注意，0或不存在表示成功。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-137">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="4e1e4-138">0</span><span class="sxs-lookup"><span data-stu-id="4e1e4-138">0</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-139">成功。</span><span class="sxs-lookup"><span data-stu-id="4e1e4-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-140">1</span><span class="sxs-lookup"><span data-stu-id="4e1e4-140">1</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-141">錯誤引數格式</span><span class="sxs-lookup"><span data-stu-id="4e1e4-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-142">2</span><span class="sxs-lookup"><span data-stu-id="4e1e4-142">2</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-143">錯誤的引數值</span><span class="sxs-lookup"><span data-stu-id="4e1e4-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-144">3</span><span class="sxs-lookup"><span data-stu-id="4e1e4-144">3</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-145">資源 (通訊端) 開啟錯誤</span><span class="sxs-lookup"><span data-stu-id="4e1e4-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-146">4</span><span class="sxs-lookup"><span data-stu-id="4e1e4-146">4</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-147">持續性 (檔案寫入) 錯誤</span><span class="sxs-lookup"><span data-stu-id="4e1e4-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="4e1e4-148">5</span><span class="sxs-lookup"><span data-stu-id="4e1e4-148">5</span></span>
</dt> <dd>

<span data-ttu-id="4e1e4-149">不可部分完成性錯誤 (舊的時間戳記不相符) </span><span class="sxs-lookup"><span data-stu-id="4e1e4-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e1e4-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e1e4-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="4e1e4-151">0</span><span class="sxs-lookup"><span data-stu-id="4e1e4-151">0</span></span>

<span data-ttu-id="4e1e4-152">失敗</span><span class="sxs-lookup"><span data-stu-id="4e1e4-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4e1e4-153">1</span><span class="sxs-lookup"><span data-stu-id="4e1e4-153">1</span></span>

<span data-ttu-id="4e1e4-154">Success</span><span class="sxs-lookup"><span data-stu-id="4e1e4-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e1e4-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e1e4-155">Requirements</span></span>



| <span data-ttu-id="4e1e4-156">需求</span><span class="sxs-lookup"><span data-stu-id="4e1e4-156">Requirement</span></span> | <span data-ttu-id="4e1e4-157">值</span><span class="sxs-lookup"><span data-stu-id="4e1e4-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1e4-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e1e4-158">Minimum supported client</span></span><br/> | <span data-ttu-id="4e1e4-159">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e1e4-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4e1e4-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e1e4-160">Minimum supported server</span></span><br/> | <span data-ttu-id="4e1e4-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4e1e4-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="4e1e4-162">命名空間</span><span class="sxs-lookup"><span data-stu-id="4e1e4-162">Namespace</span></span><br/>                | <span data-ttu-id="4e1e4-163">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="4e1e4-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="4e1e4-164">MOF</span><span class="sxs-lookup"><span data-stu-id="4e1e4-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e1e4-165"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e1e4-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e1e4-166">DLL</span><span class="sxs-lookup"><span data-stu-id="4e1e4-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e1e4-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4e1e4-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4e1e4-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e1e4-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1e4-169">**控制**</span><span class="sxs-lookup"><span data-stu-id="4e1e4-169">**Control**</span></span>](control.md)
</dt> </dl>

 

