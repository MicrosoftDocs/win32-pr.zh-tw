---
description: 指定影片媒體類型是否需要強制執行禁止複製。
ms.assetid: fb12ba38-a4f4-44fe-bf31-e731c56bb145
title: 'MF_MT_DRM_FLAGS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ef771cb72050b2273d822ce799092ce51e64c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979251"
---
# <a name="mf_mt_drm_flags-attribute"></a><span data-ttu-id="9d9b2-103">MF \_ MT \_ DRM \_ 旗標屬性</span><span class="sxs-lookup"><span data-stu-id="9d9b2-103">MF\_MT\_DRM\_FLAGS attribute</span></span>

<span data-ttu-id="9d9b2-104">指定影片媒體類型是否需要強制執行禁止複製。</span><span class="sxs-lookup"><span data-stu-id="9d9b2-104">Specifies whether a video media type requires the enforcement of copy protection.</span></span>

## <a name="data-type"></a><span data-ttu-id="9d9b2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9d9b2-105">Data type</span></span>

<span data-ttu-id="9d9b2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9d9b2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9d9b2-107">備註</span><span class="sxs-lookup"><span data-stu-id="9d9b2-107">Remarks</span></span>

<span data-ttu-id="9d9b2-108">這個屬性的值是 [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="9d9b2-108">The value of this attribute is a member of the [**MFVideoDRMFlags**](/windows/desktop/api/mfapi/ne-mfapi-mfvideodrmflags) enumeration.</span></span>

<span data-ttu-id="9d9b2-109">這個屬性會提供應用程式的提示。</span><span class="sxs-lookup"><span data-stu-id="9d9b2-109">This attribute provides a hint to the application.</span></span> <span data-ttu-id="9d9b2-110">它不會用來強制執行禁止複製或指定禁止複製機制。</span><span class="sxs-lookup"><span data-stu-id="9d9b2-110">It is not used to enforce copy protection or to specify the copy protection mechanism.</span></span>

<span data-ttu-id="9d9b2-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="9d9b2-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d9b2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d9b2-112">Requirements</span></span>



| <span data-ttu-id="9d9b2-113">需求</span><span class="sxs-lookup"><span data-stu-id="9d9b2-113">Requirement</span></span> | <span data-ttu-id="9d9b2-114">值</span><span class="sxs-lookup"><span data-stu-id="9d9b2-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9b2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d9b2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9d9b2-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d9b2-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="9d9b2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d9b2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9d9b2-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d9b2-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9d9b2-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9d9b2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d9b2-120"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d9b2-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d9b2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d9b2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d9b2-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9d9b2-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9d9b2-123">已 \_ 保護 MF SD \_</span><span class="sxs-lookup"><span data-stu-id="9d9b2-123">MF\_SD\_PROTECTED</span></span>](mf-sd-protected-attribute.md)
</dt> <dt>

[<span data-ttu-id="9d9b2-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9d9b2-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9d9b2-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9d9b2-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="9d9b2-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="9d9b2-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="9d9b2-127">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="9d9b2-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




