---
description: 如果目前的設定是復原/重做/還原的結果，請將它標示為已明確設定，讓歷程記錄保留設定的時間，並在下一次設定變更時建立備份檔案。
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: 'Control 類別的 Checkpoint 方法 (Srrestoreptapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 44453f647d55f29a9a6cfc5622e29dcc88ad2446
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110064"
---
# <a name="checkpoint-method-of-the-control-class"></a><span data-ttu-id="4d663-103">Control 類別的 Checkpoint 方法</span><span class="sxs-lookup"><span data-stu-id="4d663-103">Checkpoint method of the Control class</span></span>

<span data-ttu-id="4d663-104">如果目前的設定是復原/重做/還原的結果，請將它標示為已明確設定，讓歷程記錄保留設定的時間，並在下一次設定變更時建立備份檔案。</span><span class="sxs-lookup"><span data-stu-id="4d663-104">If the current configuration is a result of the Undo/Redo/Restore, marks it as if it has been set explicitly, so that the history will preserve the time when it was set, and a backup file will be created for it on the next configuration change.</span></span> <span data-ttu-id="4d663-105">如果已明確設定目前的設定，就不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="4d663-105">If the current configuration was already set explicitly, has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d663-106">語法</span><span class="sxs-lookup"><span data-stu-id="4d663-106">Syntax</span></span>


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="4d663-107">參數</span><span class="sxs-lookup"><span data-stu-id="4d663-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d663-108">*OldTimestampLow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d663-108">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d663-109">設定目前設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4d663-109">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="4d663-110">如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用動作。</span><span class="sxs-lookup"><span data-stu-id="4d663-110">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="4d663-111">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="4d663-111">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4d663-112">*OldTimestampHigh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d663-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d663-113">設定目前設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4d663-113">The timestamp of when the current configuration was set.</span></span> <span data-ttu-id="4d663-114">如果不是0，則會啟用不可部分完成性檢查：只有在舊設定的時間戳記符合 (（亦即) 之間的設定未變更）時，才會套用動作。</span><span class="sxs-lookup"><span data-stu-id="4d663-114">If not 0, enables the atomicity check: the action will be applied only if the timestamp of the old configuration matches (i.e. the configuration was not changed in between).</span></span> <span data-ttu-id="4d663-115">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="4d663-115">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4d663-116">*ErrorString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d663-116">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d663-117">包含錯誤說明的文字字串。</span><span class="sxs-lookup"><span data-stu-id="4d663-117">The text string with explanation of the error.</span></span>

</dd> <dt>

<span data-ttu-id="4d663-118">*WarningString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d663-118">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d663-119">具有警告的文字字串。</span><span class="sxs-lookup"><span data-stu-id="4d663-119">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="4d663-120">*InfoString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d663-120">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d663-121">包含設定相關資訊的文字字串。</span><span class="sxs-lookup"><span data-stu-id="4d663-121">The text string with information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4d663-122">*ErrorType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d663-122">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d663-123">錯誤的類型。</span><span class="sxs-lookup"><span data-stu-id="4d663-123">The type of the error.</span></span> <span data-ttu-id="4d663-124">請注意，0或不存在表示成功。</span><span class="sxs-lookup"><span data-stu-id="4d663-124">Note that 0 or absent indicates success.</span></span>

<dt>

<span data-ttu-id="4d663-125">0</span><span class="sxs-lookup"><span data-stu-id="4d663-125">0</span></span>
</dt> <dd>

<span data-ttu-id="4d663-126">成功。</span><span class="sxs-lookup"><span data-stu-id="4d663-126">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4d663-127">1</span><span class="sxs-lookup"><span data-stu-id="4d663-127">1</span></span>
</dt> <dd>

<span data-ttu-id="4d663-128">錯誤引數格式</span><span class="sxs-lookup"><span data-stu-id="4d663-128">bad argument format</span></span>

</dd> <dt>

<span data-ttu-id="4d663-129">2</span><span class="sxs-lookup"><span data-stu-id="4d663-129">2</span></span>
</dt> <dd>

<span data-ttu-id="4d663-130">錯誤的引數值</span><span class="sxs-lookup"><span data-stu-id="4d663-130">bad argument value</span></span>

</dd> <dt>

<span data-ttu-id="4d663-131">3</span><span class="sxs-lookup"><span data-stu-id="4d663-131">3</span></span>
</dt> <dd>

<span data-ttu-id="4d663-132">資源 (通訊端) 開啟錯誤</span><span class="sxs-lookup"><span data-stu-id="4d663-132">resource (socket) open error</span></span>

</dd> <dt>

<span data-ttu-id="4d663-133">4</span><span class="sxs-lookup"><span data-stu-id="4d663-133">4</span></span>
</dt> <dd>

<span data-ttu-id="4d663-134">持續性 (檔案寫入) 錯誤</span><span class="sxs-lookup"><span data-stu-id="4d663-134">persistence (file write) error</span></span>

</dd> <dt>

<span data-ttu-id="4d663-135">5</span><span class="sxs-lookup"><span data-stu-id="4d663-135">5</span></span>
</dt> <dd>

<span data-ttu-id="4d663-136">不可部分完成性錯誤 (舊的時間戳記不相符) </span><span class="sxs-lookup"><span data-stu-id="4d663-136">atomicity error (the old timestamp didn't match)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d663-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d663-137">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="4d663-138">0</span><span class="sxs-lookup"><span data-stu-id="4d663-138">0</span></span>

<span data-ttu-id="4d663-139">失敗</span><span class="sxs-lookup"><span data-stu-id="4d663-139">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="4d663-140">1</span><span class="sxs-lookup"><span data-stu-id="4d663-140">1</span></span>

<span data-ttu-id="4d663-141">Success</span><span class="sxs-lookup"><span data-stu-id="4d663-141">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d663-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d663-142">Requirements</span></span>



| <span data-ttu-id="4d663-143">需求</span><span class="sxs-lookup"><span data-stu-id="4d663-143">Requirement</span></span> | <span data-ttu-id="4d663-144">值</span><span class="sxs-lookup"><span data-stu-id="4d663-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d663-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d663-145">Minimum supported client</span></span><br/> | <span data-ttu-id="4d663-146">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d663-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4d663-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d663-147">Minimum supported server</span></span><br/> | <span data-ttu-id="4d663-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4d663-148">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="4d663-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="4d663-149">Namespace</span></span><br/>                | <span data-ttu-id="4d663-150">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="4d663-150">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="4d663-151">標頭</span><span class="sxs-lookup"><span data-stu-id="4d663-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d663-152"><dt>Srrestoreptapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="4d663-152"><dt>Srrestoreptapi.h</dt></span></span> </dl>          |
| <span data-ttu-id="4d663-153">MOF</span><span class="sxs-lookup"><span data-stu-id="4d663-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d663-154"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d663-154"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d663-155">DLL</span><span class="sxs-lookup"><span data-stu-id="4d663-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d663-156"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d663-156"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4d663-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d663-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d663-158">**控制**</span><span class="sxs-lookup"><span data-stu-id="4d663-158">**Control**</span></span>](control.md)
</dt> </dl>

 

