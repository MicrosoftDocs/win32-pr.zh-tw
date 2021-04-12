---
description: 指定是否針對轉碼（而非播放）優化解碼器。
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: 'MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386186"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a><span data-ttu-id="f0771-103">\_ \_ \_ 僅限轉碼 \_ 屬性屬性的 MFT 列舉</span><span class="sxs-lookup"><span data-stu-id="f0771-103">MFT\_ENUM\_TRANSCODE\_ONLY\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="f0771-104">指定是否針對轉碼（而非播放）優化解碼器。</span><span class="sxs-lookup"><span data-stu-id="f0771-104">Specifies whether a decoder is optimized for transcoding rather than for playback.</span></span>

<span data-ttu-id="f0771-105">目前，這個屬性只適用于使用 AVStream 迷你驅動程式的硬體型解碼器。</span><span class="sxs-lookup"><span data-stu-id="f0771-105">Currently, this attribute applies only to hardware-based decoders that use the AVStream mini-driver.</span></span> <span data-ttu-id="f0771-106">屬性會儲存在登錄中的解碼器功能資訊下。</span><span class="sxs-lookup"><span data-stu-id="f0771-106">The attribute is stored in the registry under the decoder's capabilities information.</span></span> <span data-ttu-id="f0771-107">如需詳細資訊，請參閱 [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey)的檔。</span><span class="sxs-lookup"><span data-stu-id="f0771-107">For more information, see the documentation for [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).</span></span>

<span data-ttu-id="f0771-108">應用程式通常不會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="f0771-108">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="f0771-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="f0771-109">Data type</span></span>

<span data-ttu-id="f0771-110">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f0771-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="f0771-111">備註</span><span class="sxs-lookup"><span data-stu-id="f0771-111">Remarks</span></span>

<span data-ttu-id="f0771-112">如果此登錄專案存在且等於1，則 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式會略過此解碼器，除非呼叫端在 **MFTEnumEx** 中指定了 [ **\_ \_ \_ \_ 僅轉碼**] 旗標。</span><span class="sxs-lookup"><span data-stu-id="f0771-112">If this registry entry is present and equal to 1, the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function skips the decoder unless the caller specified the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in **MFTEnumEx**.</span></span>

<span data-ttu-id="f0771-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="f0771-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0771-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0771-114">Requirements</span></span>



| <span data-ttu-id="f0771-115">需求</span><span class="sxs-lookup"><span data-stu-id="f0771-115">Requirement</span></span> | <span data-ttu-id="f0771-116">值</span><span class="sxs-lookup"><span data-stu-id="f0771-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0771-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0771-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0771-118">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0771-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f0771-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0771-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0771-120">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0771-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f0771-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f0771-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0771-122"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0771-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0771-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0771-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0771-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f0771-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f0771-125">**MFTEnumEx**</span><span class="sxs-lookup"><span data-stu-id="f0771-125">**MFTEnumEx**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
