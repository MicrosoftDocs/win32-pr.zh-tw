---
title: 'MCI_VCR_SET_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ set \_ PARMS 結構包含適用于 vcd 燒錄機之 mci \_ SET 命令的參數。
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- MCI_VCR_SET_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385138"
---
# <a name="mci_vcr_set_parms-structure"></a><span data-ttu-id="a77ac-104">MCI \_ VCR \_ SET \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="a77ac-104">MCI\_VCR\_SET\_PARMS structure</span></span>

<span data-ttu-id="a77ac-105">**Mci \_ VCR \_ set \_ PARMS** 結構包含適用于 vcd 燒錄機之 [**mci \_ SET**](mci-set.md)命令的參數。</span><span class="sxs-lookup"><span data-stu-id="a77ac-105">The **MCI\_VCR\_SET\_PARMS** structure contains parameters for the [**MCI\_SET**](mci-set.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="a77ac-106">語法</span><span class="sxs-lookup"><span data-stu-id="a77ac-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="a77ac-107">成員</span><span class="sxs-lookup"><span data-stu-id="a77ac-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a77ac-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="a77ac-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a77ac-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="a77ac-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-111">目前的時間格式。</span><span class="sxs-lookup"><span data-stu-id="a77ac-111">Current time format.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="a77ac-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="a77ac-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-114">**dwTimeMode**</span><span class="sxs-lookup"><span data-stu-id="a77ac-114">**dwTimeMode**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-115">常數，指定裝置所使用的時間來源。</span><span class="sxs-lookup"><span data-stu-id="a77ac-115">Constant that specifies the timing source used by the device.</span></span> <span data-ttu-id="a77ac-116">時間來源是記錄在磁帶上的時間碼，或是裝置中有意義磁帶移動的計數器。</span><span class="sxs-lookup"><span data-stu-id="a77ac-116">The timing source is either a timecode recorded on videotape, or the counters in the device that sense videotape movement.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-117">**dwRecordFormat**</span><span class="sxs-lookup"><span data-stu-id="a77ac-117">**dwRecordFormat**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-118">錄製速率。</span><span class="sxs-lookup"><span data-stu-id="a77ac-118">Recording rate.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-119">**dwCounterFormat**</span><span class="sxs-lookup"><span data-stu-id="a77ac-119">**dwCounterFormat**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-120">新計數器時間值的格式。</span><span class="sxs-lookup"><span data-stu-id="a77ac-120">Format of a new counter time value.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-121">**dwIndex**</span><span class="sxs-lookup"><span data-stu-id="a77ac-121">**dwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-122">螢幕上顯示的內容。</span><span class="sxs-lookup"><span data-stu-id="a77ac-122">Contents of on-screen display.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-123">**dwTracking**</span><span class="sxs-lookup"><span data-stu-id="a77ac-123">**dwTracking**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-124">追蹤 VCR 播放速率時使用的速度調整。</span><span class="sxs-lookup"><span data-stu-id="a77ac-124">Speed adjustment used when tracking the VCR playback rate.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-125">**dwSpeed**</span><span class="sxs-lookup"><span data-stu-id="a77ac-125">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-126">裝置用來作為整數的播放速度。</span><span class="sxs-lookup"><span data-stu-id="a77ac-126">Playback speed used by the device as an integer.</span></span> <span data-ttu-id="a77ac-127">正常播放速度為1000、雙速度為2000，而半速度為500。</span><span class="sxs-lookup"><span data-stu-id="a77ac-127">Normal playback speed is 1000, double speed is 2000, and half speed is 500.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-128">**dwLength**</span><span class="sxs-lookup"><span data-stu-id="a77ac-128">**dwLength**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-129">裝置無法偵測長度時的磁帶長度。</span><span class="sxs-lookup"><span data-stu-id="a77ac-129">Videotape length when the length is undetectable by the device.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-130">**dwCounter**</span><span class="sxs-lookup"><span data-stu-id="a77ac-130">**dwCounter**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-131">新計數器值。</span><span class="sxs-lookup"><span data-stu-id="a77ac-131">New counter value.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-132">**dwClock**</span><span class="sxs-lookup"><span data-stu-id="a77ac-132">**dwClock**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-133">新的時鐘時間。</span><span class="sxs-lookup"><span data-stu-id="a77ac-133">New clock time.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-134">**dwPauseTimeout**</span><span class="sxs-lookup"><span data-stu-id="a77ac-134">**dwPauseTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-135">Pause 命令的新超時值。</span><span class="sxs-lookup"><span data-stu-id="a77ac-135">New timeout value for pause command.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-136">**dwPrerollDuration**</span><span class="sxs-lookup"><span data-stu-id="a77ac-136">**dwPrerollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-137">穩定 VCR 輸出所需的磁帶長度。</span><span class="sxs-lookup"><span data-stu-id="a77ac-137">Videotape length needed to stabilize the VCR output.</span></span>

</dd> <dt>

<span data-ttu-id="a77ac-138">**dwPostrollDuration**</span><span class="sxs-lookup"><span data-stu-id="a77ac-138">**dwPostrollDuration**</span></span>
</dt> <dd>

<span data-ttu-id="a77ac-139">發出 [**mci \_ STOP**](mci-stop.md) 或 [**mci \_ PAUSE**](mci-pause.md) 命令時，煞車 VCR 傳輸所需的磁帶長度。</span><span class="sxs-lookup"><span data-stu-id="a77ac-139">Videotape length needed to brake the VCR transport when a [**MCI\_STOP**](mci-stop.md) or [**MCI\_PAUSE**](mci-pause.md) command is issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a77ac-140">備註</span><span class="sxs-lookup"><span data-stu-id="a77ac-140">Remarks</span></span>

<span data-ttu-id="a77ac-141">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="a77ac-141">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="a77ac-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="a77ac-142">Requirements</span></span>



| <span data-ttu-id="a77ac-143">需求</span><span class="sxs-lookup"><span data-stu-id="a77ac-143">Requirement</span></span> | <span data-ttu-id="a77ac-144">值</span><span class="sxs-lookup"><span data-stu-id="a77ac-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a77ac-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a77ac-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a77ac-146">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a77ac-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a77ac-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a77ac-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a77ac-148">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a77ac-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a77ac-149">標頭</span><span class="sxs-lookup"><span data-stu-id="a77ac-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a77ac-150"><dt>Vcr</dt></span><span class="sxs-lookup"><span data-stu-id="a77ac-150"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a77ac-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a77ac-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a77ac-152">**Mci**</span><span class="sxs-lookup"><span data-stu-id="a77ac-152">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a77ac-153">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="a77ac-153">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="a77ac-154">**MCI \_ 暫停**</span><span class="sxs-lookup"><span data-stu-id="a77ac-154">**MCI\_PAUSE**</span></span>](mci-pause.md)
</dt> <dt>

[<span data-ttu-id="a77ac-155">**MCI \_ 組**</span><span class="sxs-lookup"><span data-stu-id="a77ac-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

[<span data-ttu-id="a77ac-156">**MCI \_ 停止**</span><span class="sxs-lookup"><span data-stu-id="a77ac-156">**MCI\_STOP**</span></span>](mci-stop.md)
</dt> <dt>

<span data-ttu-id="a77ac-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a77ac-157">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

