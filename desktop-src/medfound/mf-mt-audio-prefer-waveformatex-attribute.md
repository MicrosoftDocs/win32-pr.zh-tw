---
description: 指定轉換音訊媒體類型時要使用的慣用舊版格式結構。
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: 'MF_MT_AUDIO_PREFER_WAVEFORMATEX 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512824"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a><span data-ttu-id="e8701-103">MF \_ MT \_ 音訊 \_ 偏好 \_ WAVEFORMATEX 屬性</span><span class="sxs-lookup"><span data-stu-id="e8701-103">MF\_MT\_AUDIO\_PREFER\_WAVEFORMATEX attribute</span></span>

<span data-ttu-id="e8701-104">指定轉換音訊媒體類型時要使用的慣用舊版格式結構。</span><span class="sxs-lookup"><span data-stu-id="e8701-104">Specifies the preferred legacy format structure to use when converting an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="e8701-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e8701-105">Data type</span></span>

<span data-ttu-id="e8701-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e8701-106">**UINT32**</span></span>

<span data-ttu-id="e8701-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="e8701-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8701-108">備註</span><span class="sxs-lookup"><span data-stu-id="e8701-108">Remarks</span></span>

<span data-ttu-id="e8701-109">這個屬性會提供 [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) 函數的提示。</span><span class="sxs-lookup"><span data-stu-id="e8701-109">This attribute provides a hint to the [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) function.</span></span> <span data-ttu-id="e8701-110">如果屬性為 **TRUE**，則函式會盡可能將音訊媒體類型轉換成 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構，而不是將它轉換成 [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="e8701-110">If the attribute is **TRUE**, the function converts the audio media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure whenever possible, instead of converting it to a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="e8701-111">[**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex)函式會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e8701-111">The [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) function sets this attribute.</span></span> <span data-ttu-id="e8701-112">您可以覆寫這個屬性的值，但是將此屬性設定為 **TRUE** 並不保證音訊媒體類型可以轉換成 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 形式。</span><span class="sxs-lookup"><span data-stu-id="e8701-112">You can override the value of this attribute, but setting this attribute to **TRUE** does not guarantee that an audio media type can be converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) form.</span></span>

<span data-ttu-id="e8701-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e8701-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8701-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8701-114">Requirements</span></span>



| <span data-ttu-id="e8701-115">需求</span><span class="sxs-lookup"><span data-stu-id="e8701-115">Requirement</span></span> | <span data-ttu-id="e8701-116">值</span><span class="sxs-lookup"><span data-stu-id="e8701-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8701-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8701-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e8701-118">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8701-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e8701-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8701-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e8701-120">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8701-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e8701-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e8701-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8701-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8701-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8701-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8701-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8701-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e8701-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e8701-125">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e8701-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e8701-126">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e8701-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e8701-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e8701-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="e8701-128">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="e8701-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
