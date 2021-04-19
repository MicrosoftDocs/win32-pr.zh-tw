---
description: 指出是否已將影片穩定套用至影片畫面。
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: 'MFSampleExtension_VideoDSPMode 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993071"
---
# <a name="mfsampleextension_videodspmode-attribute"></a><span data-ttu-id="07a2b-103">MFSampleExtension \_ VideoDSPMode 屬性</span><span class="sxs-lookup"><span data-stu-id="07a2b-103">MFSampleExtension\_VideoDSPMode attribute</span></span>

<span data-ttu-id="07a2b-104">指出是否已將影片穩定套用至影片畫面。</span><span class="sxs-lookup"><span data-stu-id="07a2b-104">Indicates whether video stabilization was applied to a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="07a2b-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="07a2b-105">Data type</span></span>

<span data-ttu-id="07a2b-106">**MFVideoDSPMode** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="07a2b-106">**MFVideoDSPMode** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="07a2b-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="07a2b-107">Get/set</span></span>

<span data-ttu-id="07a2b-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="07a2b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="07a2b-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="07a2b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="07a2b-110">適用於</span><span class="sxs-lookup"><span data-stu-id="07a2b-110">Applies to</span></span>

[<span data-ttu-id="07a2b-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="07a2b-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="07a2b-112">備註</span><span class="sxs-lookup"><span data-stu-id="07a2b-112">Remarks</span></span>

<span data-ttu-id="07a2b-113">[**影片防震 MFT**](video-stabilization-mft.md)會在其產生的輸出範例上設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="07a2b-113">The [**Video Stabilization MFT**](video-stabilization-mft.md) sets this attribute on the output samples that it produces.</span></span> <span data-ttu-id="07a2b-114">屬性的值是 [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) 列舉值。</span><span class="sxs-lookup"><span data-stu-id="07a2b-114">The value of the attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="07a2b-115">如果值是 **MFVideoDSPMode \_ 穩定**，則表示該 MFT 將映射穩定套用至框架。</span><span class="sxs-lookup"><span data-stu-id="07a2b-115">If the value is **MFVideoDSPMode\_Stabilization**, it means that the MFT applied image stabilization to the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="07a2b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="07a2b-116">Requirements</span></span>



| <span data-ttu-id="07a2b-117">需求</span><span class="sxs-lookup"><span data-stu-id="07a2b-117">Requirement</span></span> | <span data-ttu-id="07a2b-118">值</span><span class="sxs-lookup"><span data-stu-id="07a2b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07a2b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07a2b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="07a2b-120">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07a2b-120">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="07a2b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07a2b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="07a2b-122">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07a2b-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="07a2b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="07a2b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="07a2b-124"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="07a2b-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07a2b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07a2b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a2b-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="07a2b-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="07a2b-127">範例屬性</span><span class="sxs-lookup"><span data-stu-id="07a2b-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="07a2b-128">媒體範例</span><span class="sxs-lookup"><span data-stu-id="07a2b-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="07a2b-129">**影片防震 MFT**</span><span class="sxs-lookup"><span data-stu-id="07a2b-129">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




