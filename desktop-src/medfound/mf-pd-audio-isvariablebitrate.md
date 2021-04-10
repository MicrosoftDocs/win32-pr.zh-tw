---
description: 指定簡報中的音訊資料流程是否具有變數位元速率。
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: 'MF_PD_AUDIO_ISVARIABLEBITRATE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a34d3dd64f9100050dc9aae37e811d00c9d58af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193623"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a><span data-ttu-id="e324f-103">MF \_ PD \_ 音訊 \_ ISVARIABLEBITRATE 屬性</span><span class="sxs-lookup"><span data-stu-id="e324f-103">MF\_PD\_AUDIO\_ISVARIABLEBITRATE attribute</span></span>

<span data-ttu-id="e324f-104">指定簡報中的音訊資料流程是否具有變數位元速率。</span><span class="sxs-lookup"><span data-stu-id="e324f-104">Specifies whether the audio streams in a presentation have a variable bit rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="e324f-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e324f-105">Data type</span></span>

<span data-ttu-id="e324f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e324f-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e324f-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="e324f-107">Get/set</span></span>

<span data-ttu-id="e324f-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="e324f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e324f-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="e324f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e324f-110">套用至</span><span class="sxs-lookup"><span data-stu-id="e324f-110">Applies To</span></span>

[<span data-ttu-id="e324f-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e324f-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="e324f-112">備註</span><span class="sxs-lookup"><span data-stu-id="e324f-112">Remarks</span></span>

<span data-ttu-id="e324f-113">這是表示描述項的選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="e324f-113">This is an optional attribute for presentation descriptors.</span></span> <span data-ttu-id="e324f-114">如果屬性為 **TRUE** (非零) ，表示簡報至少會包含一個可變位速率 (VBR) 音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e324f-114">If the attribute is **TRUE** (nonzero), the presentation contains at least one variable-bit-rate (VBR) audio stream.</span></span> <span data-ttu-id="e324f-115">如果屬性為 **FALSE**，則所有音訊串流都有固定的位元速率。</span><span class="sxs-lookup"><span data-stu-id="e324f-115">If the attribute is **FALSE**, all of the audio streams have a constant bit rate.</span></span>

<span data-ttu-id="e324f-116">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e324f-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e324f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e324f-117">Requirements</span></span>



| <span data-ttu-id="e324f-118">需求</span><span class="sxs-lookup"><span data-stu-id="e324f-118">Requirement</span></span> | <span data-ttu-id="e324f-119">值</span><span class="sxs-lookup"><span data-stu-id="e324f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e324f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e324f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e324f-121">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e324f-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e324f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e324f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e324f-123">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e324f-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="e324f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e324f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e324f-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e324f-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e324f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e324f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e324f-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e324f-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e324f-128">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="e324f-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




