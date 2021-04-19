---
description: 針對媒體類型指定範例的大小是否固定。
ms.assetid: 2d67864a-fd2f-400d-8a1e-e71dc1920593
title: 'MF_MT_FIXED_SIZE_SAMPLES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1bb5bdd4e1330e4744902ed1b37cc55b7a67a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971707"
---
# <a name="mf_mt_fixed_size_samples-attribute"></a><span data-ttu-id="18df7-103">MF \_ MT \_ 固定 \_ 大小 \_ 範例屬性</span><span class="sxs-lookup"><span data-stu-id="18df7-103">MF\_MT\_FIXED\_SIZE\_SAMPLES attribute</span></span>

<span data-ttu-id="18df7-104">針對媒體類型指定範例的大小是否固定。</span><span class="sxs-lookup"><span data-stu-id="18df7-104">Specifies for a media type whether the samples have a fixed size.</span></span>

## <a name="data-type"></a><span data-ttu-id="18df7-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="18df7-105">Data type</span></span>

<span data-ttu-id="18df7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="18df7-106">**UINT32**</span></span>

<span data-ttu-id="18df7-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="18df7-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18df7-108">備註</span><span class="sxs-lookup"><span data-stu-id="18df7-108">Remarks</span></span>

<span data-ttu-id="18df7-109">如果這個屬性為 **TRUE**，則資料流程中的每個範例都是相同大小 (以位元組為單位）) 。</span><span class="sxs-lookup"><span data-stu-id="18df7-109">If this attribute is **TRUE**, every sample in the stream is the same size (in bytes).</span></span> <span data-ttu-id="18df7-110">否則，範例的大小可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="18df7-110">Otherwise, samples might vary in size.</span></span>

<span data-ttu-id="18df7-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="18df7-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="18df7-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="18df7-112">Requirements</span></span>



| <span data-ttu-id="18df7-113">需求</span><span class="sxs-lookup"><span data-stu-id="18df7-113">Requirement</span></span> | <span data-ttu-id="18df7-114">值</span><span class="sxs-lookup"><span data-stu-id="18df7-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18df7-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18df7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="18df7-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18df7-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="18df7-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18df7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="18df7-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18df7-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="18df7-119">標頭</span><span class="sxs-lookup"><span data-stu-id="18df7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="18df7-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="18df7-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18df7-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18df7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18df7-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="18df7-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18df7-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="18df7-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="18df7-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="18df7-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="18df7-125">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="18df7-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="18df7-126">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="18df7-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




