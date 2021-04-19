---
title: _WAVEFORMATEX 結構
description: '\_WAVEFORMATEX 結構會定義波形音訊資料的格式。'
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- _WAVEFORMATEX 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d0ede83e22033aee8f18d11b6230e471e0dfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989752"
---
# <a name="_waveformatex-structure"></a><span data-ttu-id="cd82a-104">\_WAVEFORMATEX 結構</span><span class="sxs-lookup"><span data-stu-id="cd82a-104">\_WAVEFORMATEX structure</span></span>

<span data-ttu-id="cd82a-105">**\_ WAVEFORMATEX** 結構會定義波形音訊資料的格式。</span><span class="sxs-lookup"><span data-stu-id="cd82a-105">The **\_WAVEFORMATEX** structure defines the format of waveform-audio data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd82a-106">語法</span><span class="sxs-lookup"><span data-stu-id="cd82a-106">Syntax</span></span>


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a><span data-ttu-id="cd82a-107">成員</span><span class="sxs-lookup"><span data-stu-id="cd82a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd82a-108">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="cd82a-108">**wFormatTag**</span></span>
</dt> <dd>

<span data-ttu-id="cd82a-109">必須設定為裝置支援的格式或格式。</span><span class="sxs-lookup"><span data-stu-id="cd82a-109">Must be set to a format or formats supported by the device.</span></span> <span data-ttu-id="cd82a-110">請注意，舊版 Windows Media 裝置管理員建議您使用 WMDM \_ WAVE \_ FORMAT \_ all 來指出所有格式的支援。</span><span class="sxs-lookup"><span data-stu-id="cd82a-110">Note that previous versions of the Windows Media Device Manager recommended using WMDM\_WAVE\_FORMAT\_ALL to indicate support for all formats.</span></span> <span data-ttu-id="cd82a-111">不過，這不再是建議的作法，因為不同的媒體播放機會以不同的方式來解讀這一點，而只有少數裝置才能真正播放任何檔案格式。</span><span class="sxs-lookup"><span data-stu-id="cd82a-111">However, this is no longer recommended, as different media players will interpret this in different ways, and few devices can truly play any file format.</span></span> <span data-ttu-id="cd82a-112">現在建議您使用 WMDM \_ 列舉 \_ \_ \_ 的有效值 \_ ，以提供任何 [**WMDM 列舉的有效值 \_ \_ \_ \_ \_ 形式**](wmdm-enum-prop-valid-values-form.md) 列舉值，或更好的方式，同時使用 [**WMDM 的 \_ \_ 值 \_ 範圍**](wmdm-prop-values-range.md) 結構來指定格式範圍。</span><span class="sxs-lookup"><span data-stu-id="cd82a-112">It is now recommended that you use the WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY value of the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration, or better yet specify a range of formats with the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd82a-113">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="cd82a-113">**nChannels**</span></span>
</dt> <dd>

<span data-ttu-id="cd82a-114">波形音訊資料中的通道數目。</span><span class="sxs-lookup"><span data-stu-id="cd82a-114">Number of channels in the waveform-audio data.</span></span> <span data-ttu-id="cd82a-115">Monaural 資料會使用一個通道，而身歷聲資料會使用兩個通道。</span><span class="sxs-lookup"><span data-stu-id="cd82a-115">Monaural data uses one channel, and stereo data uses two channels.</span></span>

</dd> <dt>

<span data-ttu-id="cd82a-116">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="cd82a-116">**nSamplesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="cd82a-117">取樣率，以每秒樣本數 (赫茲) ，每個通道都必須播放或記錄。</span><span class="sxs-lookup"><span data-stu-id="cd82a-117">Sample rate, in samples per second (Hertz), at which each channel must be played or recorded.</span></span> <span data-ttu-id="cd82a-118">**NSamplesPerSec** 的常見值是8.0 千赫茲 (kHz) 、11.025 kHz、22.05 khz 和 44.1 khz。</span><span class="sxs-lookup"><span data-stu-id="cd82a-118">Common values for **nSamplesPerSec** are 8.0 kilohertz (kHz), 11.025 kHz, 22.05 kHz, and 44.1 kHz.</span></span>

</dd> <dt>

<span data-ttu-id="cd82a-119">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="cd82a-119">**nAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="cd82a-120">格式標記需要的平均資料傳輸速率（以每秒位元組數為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd82a-120">Required average data-transfer rate for the format tag, in bytes per second.</span></span> <span data-ttu-id="cd82a-121">播放和錄製軟體可以使用 **nAvgBytesPerSec** 成員來預估緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="cd82a-121">Playback and recording software can estimate buffer sizes by using the **nAvgBytesPerSec** member.</span></span>

</dd> <dt>

<span data-ttu-id="cd82a-122">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="cd82a-122">**nBlockAlign**</span></span>
</dt> <dd>

<span data-ttu-id="cd82a-123">區塊對齊（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd82a-123">Block alignment, in bytes.</span></span> <span data-ttu-id="cd82a-124">區塊對齊是 **wFormatTag** 格式類型資料的最小不可部分完成單位。</span><span class="sxs-lookup"><span data-stu-id="cd82a-124">The block alignment is the minimum atomic unit of data for the **wFormatTag** format type.</span></span> <span data-ttu-id="cd82a-125">播放和錄製軟體必須一次處理 **nBlockAlign** 個位元組的資料。</span><span class="sxs-lookup"><span data-stu-id="cd82a-125">Playback and recording software must process a multiple of **nBlockAlign** bytes of data at a time.</span></span> <span data-ttu-id="cd82a-126">從裝置寫入和讀取的資料必須一律從區塊的開頭開始。</span><span class="sxs-lookup"><span data-stu-id="cd82a-126">Data written and read from a device must always start at the beginning of a block.</span></span> <span data-ttu-id="cd82a-127">例如，無法在範例 (（也就是在不封鎖對齊) 的界限）上，正確地開始播放 PCM 資料。</span><span class="sxs-lookup"><span data-stu-id="cd82a-127">For example, it is not possible to correctly start playing PCM data in the middle of a sample (that is, on a boundary that is not block aligned).</span></span>

</dd> <dt>

<span data-ttu-id="cd82a-128">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="cd82a-128">**wBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="cd82a-129">**WFormatTag** 格式類型的每個樣本位數。</span><span class="sxs-lookup"><span data-stu-id="cd82a-129">Bits per sample for the **wFormatTag** format type.</span></span>

</dd> <dt>

<span data-ttu-id="cd82a-130">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="cd82a-130">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="cd82a-131">忽略這個成員。</span><span class="sxs-lookup"><span data-stu-id="cd82a-131">This member is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd82a-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd82a-132">Requirements</span></span>



| <span data-ttu-id="cd82a-133">需求</span><span class="sxs-lookup"><span data-stu-id="cd82a-133">Requirement</span></span> | <span data-ttu-id="cd82a-134">值</span><span class="sxs-lookup"><span data-stu-id="cd82a-134">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cd82a-135">標頭</span><span class="sxs-lookup"><span data-stu-id="cd82a-135">Header</span></span><br/> | <dl> <span data-ttu-id="cd82a-136"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd82a-136"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd82a-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd82a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd82a-138">**IMDSPDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="cd82a-138">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="cd82a-139">**IMDSPStorage::CreateStorage**</span><span class="sxs-lookup"><span data-stu-id="cd82a-139">**IMDSPStorage::CreateStorage**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[<span data-ttu-id="cd82a-140">**IMDSPStorage：： GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="cd82a-140">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="cd82a-141">**IWMDMDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="cd82a-141">**IWMDMDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[<span data-ttu-id="cd82a-142">**IWMDMOperation::GetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="cd82a-142">**IWMDMOperation::GetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[<span data-ttu-id="cd82a-143">**IWMDMOperation::SetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="cd82a-143">**IWMDMOperation::SetObjectAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="cd82a-144">**IWMDMStorage：： GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="cd82a-144">**IWMDMStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[<span data-ttu-id="cd82a-145">**結構**</span><span class="sxs-lookup"><span data-stu-id="cd82a-145">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





