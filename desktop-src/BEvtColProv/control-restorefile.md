---
description: 從備份檔案還原收集器的主動式設定。
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: Control 類別的 RestoreFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFile
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 330486da86c9cac5c5f700d2aea91e0844fdca09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936067"
---
# <a name="restorefile-method-of-the-control-class"></a><span data-ttu-id="cf301-103">Control 類別的 RestoreFile 方法</span><span class="sxs-lookup"><span data-stu-id="cf301-103">RestoreFile method of the Control class</span></span>

<span data-ttu-id="cf301-104">從備份檔案還原收集器的主動式設定。</span><span class="sxs-lookup"><span data-stu-id="cf301-104">Restore the active configuration of the collector from a backup file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf301-105">語法</span><span class="sxs-lookup"><span data-stu-id="cf301-105">Syntax</span></span>


```mof
Uint32 RestoreFile(
  [in]  string File,
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



## <a name="parameters"></a><span data-ttu-id="cf301-106">參數</span><span class="sxs-lookup"><span data-stu-id="cf301-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf301-107">檔案 \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf301-107">*File* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-108">要還原之備份檔案的名稱，從 ListBackups () 傳回的清單中。</span><span class="sxs-lookup"><span data-stu-id="cf301-108">Name of the backup file to restore, from the list returned by ListBackups().</span></span>

</dd> <dt>

<span data-ttu-id="cf301-109">*OldTimestampLow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf301-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-110">設定先前設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cf301-110">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="cf301-111">如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用新的設定。</span><span class="sxs-lookup"><span data-stu-id="cf301-111">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="cf301-112">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="cf301-112">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cf301-113">*OldTimestampHigh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf301-113">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-114">設定先前設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cf301-114">The timestamp of when the previous configuration was set.</span></span> <span data-ttu-id="cf301-115">如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用新的設定。</span><span class="sxs-lookup"><span data-stu-id="cf301-115">If not 0, enables the atomicity check: the new configuration will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="cf301-116">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="cf301-116">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cf301-117">*NewTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf301-117">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-118">如果呼叫成功，則為設定新設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cf301-118">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="cf301-119">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="cf301-119">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cf301-120">*NewTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf301-120">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-121">如果呼叫成功，則為設定新設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cf301-121">The timestamp of when the new configuration was set, if the call succeeds.</span></span> <span data-ttu-id="cf301-122">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="cf301-122">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cf301-123">*OriginalTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf301-123">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-124">第一次設定還原設定時的原始時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cf301-124">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="cf301-125">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="cf301-125">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cf301-126">*OriginalTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf301-126">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-127">第一次設定還原設定時的原始時間戳記。</span><span class="sxs-lookup"><span data-stu-id="cf301-127">The original timestamp of when the restored configuration was set for the first time.</span></span> <span data-ttu-id="cf301-128">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="cf301-128">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="cf301-129">*ErrorString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf301-129">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-130">包含錯誤說明的文字字串。</span><span class="sxs-lookup"><span data-stu-id="cf301-130">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="cf301-131">*WarningString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf301-131">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-132">具有警告的文字字串。</span><span class="sxs-lookup"><span data-stu-id="cf301-132">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="cf301-133">*InfoString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf301-133">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-134">包含設定相關資訊的文字字串。</span><span class="sxs-lookup"><span data-stu-id="cf301-134">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="cf301-135">*ErrorType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf301-135">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf301-136">錯誤的類型：請注意，0或不存在表示成功。</span><span class="sxs-lookup"><span data-stu-id="cf301-136">The type of the error: note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="cf301-137">0</span><span class="sxs-lookup"><span data-stu-id="cf301-137">0</span></span>
</dt> <dd>

<span data-ttu-id="cf301-138">成功。</span><span class="sxs-lookup"><span data-stu-id="cf301-138">Success.</span></span>

</dd> <dt>

<span data-ttu-id="cf301-139">1</span><span class="sxs-lookup"><span data-stu-id="cf301-139">1</span></span>
</dt> <dd>

<span data-ttu-id="cf301-140">錯誤引數格式</span><span class="sxs-lookup"><span data-stu-id="cf301-140">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="cf301-141">2</span><span class="sxs-lookup"><span data-stu-id="cf301-141">2</span></span>
</dt> <dd>

<span data-ttu-id="cf301-142">錯誤的引數值</span><span class="sxs-lookup"><span data-stu-id="cf301-142">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="cf301-143">3</span><span class="sxs-lookup"><span data-stu-id="cf301-143">3</span></span>
</dt> <dd>

<span data-ttu-id="cf301-144">資源 (通訊端) 開啟錯誤</span><span class="sxs-lookup"><span data-stu-id="cf301-144">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="cf301-145">4</span><span class="sxs-lookup"><span data-stu-id="cf301-145">4</span></span>
</dt> <dd>

<span data-ttu-id="cf301-146">持續性 (檔案寫入) 錯誤</span><span class="sxs-lookup"><span data-stu-id="cf301-146">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="cf301-147">5</span><span class="sxs-lookup"><span data-stu-id="cf301-147">5</span></span>
</dt> <dd>

<span data-ttu-id="cf301-148">不可部分完成性錯誤 (舊的時間戳記不相符) </span><span class="sxs-lookup"><span data-stu-id="cf301-148">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf301-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf301-149">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="cf301-150">0</span><span class="sxs-lookup"><span data-stu-id="cf301-150">0</span></span>

<span data-ttu-id="cf301-151">失敗</span><span class="sxs-lookup"><span data-stu-id="cf301-151">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="cf301-152">1</span><span class="sxs-lookup"><span data-stu-id="cf301-152">1</span></span>

<span data-ttu-id="cf301-153">Success</span><span class="sxs-lookup"><span data-stu-id="cf301-153">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf301-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf301-154">Requirements</span></span>



| <span data-ttu-id="cf301-155">需求</span><span class="sxs-lookup"><span data-stu-id="cf301-155">Requirement</span></span> | <span data-ttu-id="cf301-156">值</span><span class="sxs-lookup"><span data-stu-id="cf301-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf301-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf301-157">Minimum supported client</span></span><br/> | <span data-ttu-id="cf301-158">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cf301-158">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cf301-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf301-159">Minimum supported server</span></span><br/> | <span data-ttu-id="cf301-160">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cf301-160">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="cf301-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="cf301-161">Namespace</span></span><br/>                | <span data-ttu-id="cf301-162">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="cf301-162">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="cf301-163">MOF</span><span class="sxs-lookup"><span data-stu-id="cf301-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf301-164"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf301-164"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf301-165">DLL</span><span class="sxs-lookup"><span data-stu-id="cf301-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf301-166"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf301-166"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="cf301-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf301-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf301-168">**控制**</span><span class="sxs-lookup"><span data-stu-id="cf301-168">**Control**</span></span>](control.md)
</dt> </dl>

 

