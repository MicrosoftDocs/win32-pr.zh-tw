---
description: 設定媒體引擎的呈現目標格式。
ms.assetid: 70FFDD44-9FDE-4D86-AD65-60019AC4A2BC
title: 'MF_MEDIA_ENGINE_VIDEO_OUTPUT_FORMAT 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004025da1ad5258e5b04a3afba4a359f50f7444c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696213"
---
# <a name="mf_media_engine_video_output_format-attribute"></a><span data-ttu-id="afcee-103">MF \_ 媒體 \_ 引擎 \_ 影片 \_ 輸出 \_ 格式屬性</span><span class="sxs-lookup"><span data-stu-id="afcee-103">MF\_MEDIA\_ENGINE\_VIDEO\_OUTPUT\_FORMAT attribute</span></span>

<span data-ttu-id="afcee-104">設定媒體引擎的呈現目標格式。</span><span class="sxs-lookup"><span data-stu-id="afcee-104">Sets the render-target format for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="afcee-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="afcee-105">Data type</span></span>

<span data-ttu-id="afcee-106">**DXGI \_** 儲存為 **UINT32** 的格式</span><span class="sxs-lookup"><span data-stu-id="afcee-106">**DXGI\_FORMAT** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="afcee-107">備註</span><span class="sxs-lookup"><span data-stu-id="afcee-107">Remarks</span></span>

<span data-ttu-id="afcee-108">如果您在框架伺服器模式下建立媒體引擎，請設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="afcee-108">Set this attribute if you create the Media Engine in frame-server mode.</span></span> <span data-ttu-id="afcee-109">如需詳細資訊，請參閱 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)。</span><span class="sxs-lookup"><span data-stu-id="afcee-109">For more information, see [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="afcee-110">屬性的值為 [DXGI \_ 格式](../direct3d9/d3dformat.md) 值。</span><span class="sxs-lookup"><span data-stu-id="afcee-110">The value of the attribute is a [DXGI\_FORMAT](../direct3d9/d3dformat.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="afcee-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="afcee-111">Requirements</span></span>



| <span data-ttu-id="afcee-112">需求</span><span class="sxs-lookup"><span data-stu-id="afcee-112">Requirement</span></span> | <span data-ttu-id="afcee-113">值</span><span class="sxs-lookup"><span data-stu-id="afcee-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="afcee-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afcee-114">Minimum supported client</span></span><br/> | <span data-ttu-id="afcee-115">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afcee-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="afcee-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afcee-116">Minimum supported server</span></span><br/> | <span data-ttu-id="afcee-117">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afcee-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="afcee-118">標頭</span><span class="sxs-lookup"><span data-stu-id="afcee-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="afcee-119"><dt>Mfmediaengine。h</dt></span><span class="sxs-lookup"><span data-stu-id="afcee-119"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afcee-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afcee-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afcee-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="afcee-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
