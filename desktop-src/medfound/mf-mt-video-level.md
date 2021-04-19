---
description: 指定影片媒體類型中的 MPEG-2 或 h.264 層級。 這是 MF \_ MT \_ MPEG2 \_ 層級的別名。
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: 'MF_MT_VIDEO_LEVEL 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2c5eb00390df1b5c18cab7e04a5f7449f84fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985370"
---
# <a name="mf_mt_video_level-attribute"></a><span data-ttu-id="2459f-104">MF \_ MT \_ 影片 \_ 層級屬性</span><span class="sxs-lookup"><span data-stu-id="2459f-104">MF\_MT\_VIDEO\_LEVEL attribute</span></span>

<span data-ttu-id="2459f-105">指定影片媒體類型中的 MPEG-2 或 h.264 層級。</span><span class="sxs-lookup"><span data-stu-id="2459f-105">Specifies the MPEG-2 or H.264 level in a video media type.</span></span> <span data-ttu-id="2459f-106">這是 [MF \_ MT \_ MPEG2 \_ 層級](mf-mt-mpeg2-level-attribute.md)的別名。</span><span class="sxs-lookup"><span data-stu-id="2459f-106">This is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="2459f-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="2459f-107">Data type</span></span>

<span data-ttu-id="2459f-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2459f-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2459f-109">備註</span><span class="sxs-lookup"><span data-stu-id="2459f-109">Remarks</span></span>

<span data-ttu-id="2459f-110">**H.264 編碼器：**</span><span class="sxs-lookup"><span data-stu-id="2459f-110">**H.264 encoders:**</span></span>

<span data-ttu-id="2459f-111">擴充支援的層級，以包含 [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel)。</span><span class="sxs-lookup"><span data-stu-id="2459f-111">Supported levels are extended to include the [**eAVEncH264VLevel5\_2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).</span></span>

<span data-ttu-id="2459f-112">預設值：建議的預設值是選取符合影片編碼設定的最小層級（包括解析度、畫面播放速率等）。</span><span class="sxs-lookup"><span data-stu-id="2459f-112">Default : Recommended default is to select the minimum level to match video encoding configuration including resolution, frame rate etc.</span></span>

<span data-ttu-id="2459f-113">建議的預設值：選取符合影片編碼設定的最小層級，包括解析度、畫面播放速率等等。</span><span class="sxs-lookup"><span data-stu-id="2459f-113">Recommended default: select the minimum level to match video encoding configuration including resolution, frame rate, etc.</span></span>

## <a name="requirements"></a><span data-ttu-id="2459f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2459f-114">Requirements</span></span>



| <span data-ttu-id="2459f-115">需求</span><span class="sxs-lookup"><span data-stu-id="2459f-115">Requirement</span></span> | <span data-ttu-id="2459f-116">值</span><span class="sxs-lookup"><span data-stu-id="2459f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2459f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2459f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2459f-118">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2459f-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2459f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2459f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2459f-120">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2459f-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2459f-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2459f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2459f-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2459f-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2459f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2459f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2459f-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="2459f-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




