---
description: 針對影片媒體類型，指定3D 影片框架儲存在記憶體中的方式。
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: 'MF_MT_VIDEO_3D_FORMAT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979303"
---
# <a name="mf_mt_video_3d_format-attribute"></a><span data-ttu-id="aa663-103">MF \_ MT \_ VIDEO \_ 3d \_ 格式屬性</span><span class="sxs-lookup"><span data-stu-id="aa663-103">MF\_MT\_VIDEO\_3D\_FORMAT attribute</span></span>

<span data-ttu-id="aa663-104">針對影片媒體類型，指定3D 影片框架儲存在記憶體中的方式。</span><span class="sxs-lookup"><span data-stu-id="aa663-104">For a video media type, specifies how 3D video frames are stored in memory.</span></span>

## <a name="data-type"></a><span data-ttu-id="aa663-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="aa663-105">Data type</span></span>

<span data-ttu-id="aa663-106">**MFVideo3DFormat** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="aa663-106">**MFVideo3DFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="aa663-107">備註</span><span class="sxs-lookup"><span data-stu-id="aa663-107">Remarks</span></span>

<span data-ttu-id="aa663-108">這個屬性的值是 [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="aa663-108">The value of this attribute is a member of the [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) enumeration.</span></span> <span data-ttu-id="aa663-109">只有當 [MF \_ MT \_ VIDEO \_ 3d](mf-mt-video-3d.md) 屬性為 **TRUE** 時，才會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="aa663-109">The attribute applies only if the [MF\_MT\_VIDEO\_3D](mf-mt-video-3d.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="aa663-110">未壓縮的3D 影片格式需要此屬性。</span><span class="sxs-lookup"><span data-stu-id="aa663-110">This attribute is required for uncompressed 3D video formats.</span></span> <span data-ttu-id="aa663-111">這對壓縮的3D 影片是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="aa663-111">It is optional for compressed 3D video.</span></span> <span data-ttu-id="aa663-112">傳遞編碼框架的媒體來源可能可以根據檔案容器中的資訊來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="aa663-112">A media source that delivers encoded frames might be able to set the attribute, based on information in the file container.</span></span> <span data-ttu-id="aa663-113">否則，應該由解碼器的輸出媒體類型中的解碼器來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="aa663-113">Otherwise, the attribute should be set by the decoder in the decoder's output media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa663-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa663-114">Requirements</span></span>



| <span data-ttu-id="aa663-115">需求</span><span class="sxs-lookup"><span data-stu-id="aa663-115">Requirement</span></span> | <span data-ttu-id="aa663-116">值</span><span class="sxs-lookup"><span data-stu-id="aa663-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa663-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa663-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aa663-118">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa663-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="aa663-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa663-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aa663-120">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aa663-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="aa663-121">標頭</span><span class="sxs-lookup"><span data-stu-id="aa663-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa663-122"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa663-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa663-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa663-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa663-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="aa663-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




