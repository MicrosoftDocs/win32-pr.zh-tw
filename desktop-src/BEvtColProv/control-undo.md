---
description: 從先前的備份檔案還原收集器的使用中設定， (由從目前的原始時間戳記) 來判斷。
ms.assetid: 150fa554-9efd-483e-a177-5fc7766a6a6c
ms.tgt_platform: multiple
title: Control 類別的 Undo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Undo
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 285f1ec39ea52f6c388e324f72745d72f65207e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970903"
---
# <a name="undo-method-of-the-control-class"></a><span data-ttu-id="77fd3-103">Control 類別的 Undo 方法</span><span class="sxs-lookup"><span data-stu-id="77fd3-103">Undo method of the Control class</span></span>

<span data-ttu-id="77fd3-104">從先前的備份檔案還原收集器的使用中設定， (由從目前的原始時間戳記) 來判斷。</span><span class="sxs-lookup"><span data-stu-id="77fd3-104">Restore the active configuration of the collector from the previous backup file (determined by going back from the current original timestamp).</span></span> <span data-ttu-id="77fd3-105">如果設定是剛設定的，這表示還原該變更。</span><span class="sxs-lookup"><span data-stu-id="77fd3-105">If the configuration has been just set, this means undoing that change.</span></span> <span data-ttu-id="77fd3-106">連續的呼叫將會復原到先前和先前的設定。</span><span class="sxs-lookup"><span data-stu-id="77fd3-106">The consecutive calls will undo to the earlier and earlier configurations.</span></span> <span data-ttu-id="77fd3-107">在成功時傳回1，錯誤則為0。</span><span class="sxs-lookup"><span data-stu-id="77fd3-107">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="77fd3-108">語法</span><span class="sxs-lookup"><span data-stu-id="77fd3-108">Syntax</span></span>


```mof
Uint32 Undo(
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



## <a name="parameters"></a><span data-ttu-id="77fd3-109">參數</span><span class="sxs-lookup"><span data-stu-id="77fd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77fd3-110">*OldTimestampLow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-110">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-111">設定先前設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="77fd3-111">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="77fd3-112">如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用新的設定。</span><span class="sxs-lookup"><span data-stu-id="77fd3-112">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="77fd3-113">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="77fd3-113">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-114">*OldTimestampHigh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-114">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-115">設定先前設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="77fd3-115">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="77fd3-116">如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用新的設定。</span><span class="sxs-lookup"><span data-stu-id="77fd3-116">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="77fd3-117">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="77fd3-117">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-118">*NewTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-118">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-119">如果呼叫成功，則為設定新設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="77fd3-119">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="77fd3-120">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="77fd3-120">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-121">*NewTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-121">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-122">如果呼叫成功，則為設定新設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="77fd3-122">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="77fd3-123">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="77fd3-123">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-124">*OriginalTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-124">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-125">第一次設定還原設定時的原始時間戳記。</span><span class="sxs-lookup"><span data-stu-id="77fd3-125">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="77fd3-126">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="77fd3-126">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-127">*OriginalTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-127">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-128">第一次設定還原設定時的原始時間戳記。</span><span class="sxs-lookup"><span data-stu-id="77fd3-128">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="77fd3-129">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="77fd3-129">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-130">*ErrorString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-130">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-131">包含錯誤說明的文字字串。</span><span class="sxs-lookup"><span data-stu-id="77fd3-131">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-132">*WarningString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-132">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-133">具有警告的文字字串。</span><span class="sxs-lookup"><span data-stu-id="77fd3-133">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-134">*InfoString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-134">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-135">包含設定相關資訊的文字字串。</span><span class="sxs-lookup"><span data-stu-id="77fd3-135">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-136">*ErrorType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-136">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-137">錯誤的類型：請注意，0或不存在表示成功。</span><span class="sxs-lookup"><span data-stu-id="77fd3-137">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="77fd3-138">0</span><span class="sxs-lookup"><span data-stu-id="77fd3-138">0</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-139">成功。</span><span class="sxs-lookup"><span data-stu-id="77fd3-139">Success.</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-140">1</span><span class="sxs-lookup"><span data-stu-id="77fd3-140">1</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-141">錯誤引數格式</span><span class="sxs-lookup"><span data-stu-id="77fd3-141">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-142">2</span><span class="sxs-lookup"><span data-stu-id="77fd3-142">2</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-143">錯誤的引數值</span><span class="sxs-lookup"><span data-stu-id="77fd3-143">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-144">3</span><span class="sxs-lookup"><span data-stu-id="77fd3-144">3</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-145">資源 (通訊端) 開啟錯誤</span><span class="sxs-lookup"><span data-stu-id="77fd3-145">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-146">4</span><span class="sxs-lookup"><span data-stu-id="77fd3-146">4</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-147">持續性 (檔案寫入) 錯誤</span><span class="sxs-lookup"><span data-stu-id="77fd3-147">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="77fd3-148">5</span><span class="sxs-lookup"><span data-stu-id="77fd3-148">5</span></span>
</dt> <dd>

<span data-ttu-id="77fd3-149">不可部分完成性錯誤 (舊的時間戳記不相符) </span><span class="sxs-lookup"><span data-stu-id="77fd3-149">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77fd3-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="77fd3-150">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="77fd3-151">0</span><span class="sxs-lookup"><span data-stu-id="77fd3-151">0</span></span>

<span data-ttu-id="77fd3-152">失敗</span><span class="sxs-lookup"><span data-stu-id="77fd3-152">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="77fd3-153">1</span><span class="sxs-lookup"><span data-stu-id="77fd3-153">1</span></span>

<span data-ttu-id="77fd3-154">Success</span><span class="sxs-lookup"><span data-stu-id="77fd3-154">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77fd3-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="77fd3-155">Requirements</span></span>



| <span data-ttu-id="77fd3-156">需求</span><span class="sxs-lookup"><span data-stu-id="77fd3-156">Requirement</span></span> | <span data-ttu-id="77fd3-157">值</span><span class="sxs-lookup"><span data-stu-id="77fd3-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77fd3-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77fd3-158">Minimum supported client</span></span><br/> | <span data-ttu-id="77fd3-159">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77fd3-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="77fd3-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77fd3-160">Minimum supported server</span></span><br/> | <span data-ttu-id="77fd3-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="77fd3-161">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="77fd3-162">命名空間</span><span class="sxs-lookup"><span data-stu-id="77fd3-162">Namespace</span></span><br/>                | <span data-ttu-id="77fd3-163">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="77fd3-163">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="77fd3-164">MOF</span><span class="sxs-lookup"><span data-stu-id="77fd3-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77fd3-165"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="77fd3-165"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="77fd3-166">DLL</span><span class="sxs-lookup"><span data-stu-id="77fd3-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77fd3-167"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="77fd3-167"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="77fd3-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77fd3-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77fd3-169">**控制**</span><span class="sxs-lookup"><span data-stu-id="77fd3-169">**Control**</span></span>](control.md)
</dt> </dl>

 

