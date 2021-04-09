---
description: 設定媒體引擎影片播放視窗的控制碼。
ms.assetid: 63889D81-12C5-47C1-B52A-6358E68830C3
title: 'MF_MEDIA_ENGINE_PLAYBACK_HWND 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6a9d38d40b04b32244f48289d3334199a7e035
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945622"
---
# <a name="mf_media_engine_playback_hwnd-attribute"></a><span data-ttu-id="33bf9-103">MF \_ 媒體 \_ 引擎 \_ 播放 \_ HWND 屬性</span><span class="sxs-lookup"><span data-stu-id="33bf9-103">MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND attribute</span></span>

<span data-ttu-id="33bf9-104">設定媒體引擎影片播放視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="33bf9-104">Sets a handle to a video playback window for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="33bf9-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="33bf9-105">Data type</span></span>

<span data-ttu-id="33bf9-106">**HWND** 儲存為 **UINT64**</span><span class="sxs-lookup"><span data-stu-id="33bf9-106">**HWND** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="33bf9-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="33bf9-107">Get/set</span></span>

<span data-ttu-id="33bf9-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。</span><span class="sxs-lookup"><span data-stu-id="33bf9-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="33bf9-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。</span><span class="sxs-lookup"><span data-stu-id="33bf9-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="remarks"></a><span data-ttu-id="33bf9-110">備註</span><span class="sxs-lookup"><span data-stu-id="33bf9-110">Remarks</span></span>

<span data-ttu-id="33bf9-111">這個屬性會與 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) 方法搭配使用，以初始化 Media Engine。</span><span class="sxs-lookup"><span data-stu-id="33bf9-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="33bf9-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="33bf9-112">Requirements</span></span>



| <span data-ttu-id="33bf9-113">需求</span><span class="sxs-lookup"><span data-stu-id="33bf9-113">Requirement</span></span> | <span data-ttu-id="33bf9-114">值</span><span class="sxs-lookup"><span data-stu-id="33bf9-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="33bf9-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33bf9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="33bf9-116">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33bf9-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="33bf9-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33bf9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="33bf9-118">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33bf9-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="33bf9-119">標頭</span><span class="sxs-lookup"><span data-stu-id="33bf9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="33bf9-120"><dt>Mfmediaengine。h</dt></span><span class="sxs-lookup"><span data-stu-id="33bf9-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33bf9-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33bf9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33bf9-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="33bf9-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




