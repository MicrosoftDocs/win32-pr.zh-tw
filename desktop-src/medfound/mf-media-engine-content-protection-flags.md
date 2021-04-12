---
description: 指定媒體引擎是否會播放受保護的內容。
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: 'MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33feb8d3e1d7c216cfd0392a1fcf9df0100f924
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321516"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a><span data-ttu-id="1e299-103">MF \_ 媒體 \_ 引擎 \_ 內容 \_ 保護 \_ 旗標屬性</span><span class="sxs-lookup"><span data-stu-id="1e299-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_FLAGS attribute</span></span>

<span data-ttu-id="1e299-104">指定媒體引擎是否會播放受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="1e299-104">Specifies whether the Media Engine will play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="1e299-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="1e299-105">Data type</span></span>

<span data-ttu-id="1e299-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1e299-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1e299-107">備註</span><span class="sxs-lookup"><span data-stu-id="1e299-107">Remarks</span></span>

<span data-ttu-id="1e299-108">這個屬性的值是來自于 [**MF \_ 媒體 \_ 引擎 \_ 保護 \_ 旗標**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags)列舉的位 **or** of 旗標。</span><span class="sxs-lookup"><span data-stu-id="1e299-108">The value of this attribute is a bitwise **OR** of flags from the [**MF\_MEDIA\_ENGINE\_PROTECTION\_FLAGS**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) enumeration.</span></span> <span data-ttu-id="1e299-109">若要啟用受保護內容的播放，請設定 [ **MF \_ 媒體 \_ 引擎 \_ 啟用 \_ 受保護的 \_ 內容** ] 旗標。</span><span class="sxs-lookup"><span data-stu-id="1e299-109">To enable playback of protected content, set the **MF\_MEDIA\_ENGINE\_ENABLE\_PROTECTED\_CONTENT** flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e299-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e299-110">Requirements</span></span>



| <span data-ttu-id="1e299-111">需求</span><span class="sxs-lookup"><span data-stu-id="1e299-111">Requirement</span></span> | <span data-ttu-id="1e299-112">值</span><span class="sxs-lookup"><span data-stu-id="1e299-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e299-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e299-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1e299-114">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e299-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="1e299-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e299-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1e299-116">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e299-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="1e299-117">標頭</span><span class="sxs-lookup"><span data-stu-id="1e299-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e299-118"><dt>Mfmediaengine。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e299-118"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e299-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e299-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e299-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1e299-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1e299-121">媒體引擎屬性</span><span class="sxs-lookup"><span data-stu-id="1e299-121">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="1e299-122">**IMFMediaEngineClassFactory：： CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="1e299-122">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




