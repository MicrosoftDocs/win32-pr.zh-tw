---
title: 'MCI_WAVE_SET_PARMS 結構 (Mciapi .h) '
description: MCI \_ WAVE \_ set PARMS 結構包含適用于 wave \_ 音訊裝置之 mci \_ SET 命令的資訊。
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- MCI_WAVE_SET_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11446eda931da1a645b9bb6218c93898862b59bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844227"
---
# <a name="mci_wave_set_parms-structure"></a><span data-ttu-id="eb492-104">MCI \_ WAVE \_ SET \_ PARMS 結構</span><span class="sxs-lookup"><span data-stu-id="eb492-104">MCI\_WAVE\_SET\_PARMS structure</span></span>

<span data-ttu-id="eb492-105">**Mci \_ WAVE \_ set \_ PARMS** 結構包含適用于 wave 音訊裝置之 [**mci \_ SET**](mci-set.md)命令的資訊。</span><span class="sxs-lookup"><span data-stu-id="eb492-105">The **MCI\_WAVE\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for waveform-audio devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb492-106">語法</span><span class="sxs-lookup"><span data-stu-id="eb492-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="eb492-107">成員</span><span class="sxs-lookup"><span data-stu-id="eb492-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="eb492-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="eb492-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-109">低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="eb492-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="eb492-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-111">裝置的時間格式。</span><span class="sxs-lookup"><span data-stu-id="eb492-111">Device's time format.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="eb492-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-113">音訊輸出的頻道號碼。</span><span class="sxs-lookup"><span data-stu-id="eb492-113">Channel number for audio output.</span></span> <span data-ttu-id="eb492-114">通常用來開啟或關閉通道。</span><span class="sxs-lookup"><span data-stu-id="eb492-114">Typically used when turning a channel on or off.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-115">**wInput**</span><span class="sxs-lookup"><span data-stu-id="eb492-115">**wInput**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-116">音訊輸入通道。</span><span class="sxs-lookup"><span data-stu-id="eb492-116">Audio input channel.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-117">**wOutput**</span><span class="sxs-lookup"><span data-stu-id="eb492-117">**wOutput**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-118">要使用的輸出裝置。</span><span class="sxs-lookup"><span data-stu-id="eb492-118">Output device to use.</span></span> <span data-ttu-id="eb492-119">例如，如果系統有兩個已安裝的音效卡，則此值可能是2。</span><span class="sxs-lookup"><span data-stu-id="eb492-119">For example, this value could be 2 if a system had two installed sound cards.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-120">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="eb492-120">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-121">波形音訊資料的格式，例如 WAVE \_ 格式 \_ PCM。</span><span class="sxs-lookup"><span data-stu-id="eb492-121">Format of the waveform-audio data, such as WAVE\_FORMAT\_PCM.</span></span> <span data-ttu-id="eb492-122">可能的值定義于 Mmreg 中。</span><span class="sxs-lookup"><span data-stu-id="eb492-122">Possible values are defined in Mmreg.h.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-123">**wReserved2**</span><span class="sxs-lookup"><span data-stu-id="eb492-123">**wReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-124">保留的。</span><span class="sxs-lookup"><span data-stu-id="eb492-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-125">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="eb492-125">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-126">Mono (1) 或身歷聲 (2) 。</span><span class="sxs-lookup"><span data-stu-id="eb492-126">Mono (1) or stereo (2).</span></span>

</dd> <dt>

<span data-ttu-id="eb492-127">**wReserved3**</span><span class="sxs-lookup"><span data-stu-id="eb492-127">**wReserved3**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-128">保留的。</span><span class="sxs-lookup"><span data-stu-id="eb492-128">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-129">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="eb492-129">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-130">每秒樣本數。</span><span class="sxs-lookup"><span data-stu-id="eb492-130">Samples per second.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-131">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="eb492-131">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-132">取樣率（位元組/秒）。</span><span class="sxs-lookup"><span data-stu-id="eb492-132">Sample rate in bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-133">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="eb492-133">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-134">封鎖資料的對齊。</span><span class="sxs-lookup"><span data-stu-id="eb492-134">Block alignment of the data.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-135">**wReserved4**</span><span class="sxs-lookup"><span data-stu-id="eb492-135">**wReserved4**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-136">保留的。</span><span class="sxs-lookup"><span data-stu-id="eb492-136">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-137">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="eb492-137">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-138">每個樣本的位數。</span><span class="sxs-lookup"><span data-stu-id="eb492-138">Bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="eb492-139">**wReserved5**</span><span class="sxs-lookup"><span data-stu-id="eb492-139">**wReserved5**</span></span>
</dt> <dd>

<span data-ttu-id="eb492-140">保留的。</span><span class="sxs-lookup"><span data-stu-id="eb492-140">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb492-141">備註</span><span class="sxs-lookup"><span data-stu-id="eb492-141">Remarks</span></span>

<span data-ttu-id="eb492-142">將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。</span><span class="sxs-lookup"><span data-stu-id="eb492-142">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb492-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb492-143">Requirements</span></span>



| <span data-ttu-id="eb492-144">需求</span><span class="sxs-lookup"><span data-stu-id="eb492-144">Requirement</span></span> | <span data-ttu-id="eb492-145">值</span><span class="sxs-lookup"><span data-stu-id="eb492-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="eb492-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb492-146">Minimum supported client</span></span><br/> | <span data-ttu-id="eb492-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb492-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="eb492-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb492-148">Minimum supported server</span></span><br/> | <span data-ttu-id="eb492-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb492-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="eb492-150">標頭</span><span class="sxs-lookup"><span data-stu-id="eb492-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb492-151"><dt>Mciapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb492-151"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb492-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb492-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb492-153">**Mci**</span><span class="sxs-lookup"><span data-stu-id="eb492-153">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="eb492-154">**MCI 結構**</span><span class="sxs-lookup"><span data-stu-id="eb492-154">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="eb492-155">**MCI \_ 組**</span><span class="sxs-lookup"><span data-stu-id="eb492-155">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="eb492-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb492-156">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

