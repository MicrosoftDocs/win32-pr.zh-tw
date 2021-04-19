---
description: 影片裁剪視窗的控制碼。
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: 'MF_ACTI加值稅E_VIDEO_WINDOW 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994382"
---
# <a name="mf_activate_video_window-attribute"></a><span data-ttu-id="5e6b2-103">MF \_ 啟用 \_ 影片 \_ 視窗屬性</span><span class="sxs-lookup"><span data-stu-id="5e6b2-103">MF\_ACTIVATE\_VIDEO\_WINDOW attribute</span></span>

<span data-ttu-id="5e6b2-104">影片裁剪視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5e6b2-104">Handle to the video clipping window.</span></span>

## <a name="data-type"></a><span data-ttu-id="5e6b2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5e6b2-105">Data type</span></span>

<span data-ttu-id="5e6b2-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="5e6b2-106">**UINT64**</span></span>

<span data-ttu-id="5e6b2-107">視為 **DWORD \_ PTR** (**HWND**) 。</span><span class="sxs-lookup"><span data-stu-id="5e6b2-107">Treat as **DWORD\_PTR** (**HWND**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e6b2-108">備註</span><span class="sxs-lookup"><span data-stu-id="5e6b2-108">Remarks</span></span>

<span data-ttu-id="5e6b2-109">這個屬性會套用至增強型影片轉譯器的啟用物件 (EVR) 。</span><span class="sxs-lookup"><span data-stu-id="5e6b2-109">This attribute applies to the activation object for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="5e6b2-110">當您呼叫 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) 來建立 EVR 啟用物件時，會自動設定此值。</span><span class="sxs-lookup"><span data-stu-id="5e6b2-110">The value is set automatically when you call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the EVR activation object.</span></span>

<span data-ttu-id="5e6b2-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="5e6b2-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e6b2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e6b2-112">Requirements</span></span>



| <span data-ttu-id="5e6b2-113">需求</span><span class="sxs-lookup"><span data-stu-id="5e6b2-113">Requirement</span></span> | <span data-ttu-id="5e6b2-114">值</span><span class="sxs-lookup"><span data-stu-id="5e6b2-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e6b2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e6b2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5e6b2-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e6b2-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e6b2-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e6b2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5e6b2-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e6b2-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e6b2-119">標頭</span><span class="sxs-lookup"><span data-stu-id="5e6b2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e6b2-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e6b2-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e6b2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e6b2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e6b2-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="5e6b2-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e6b2-123">增強的影片轉譯器屬性</span><span class="sxs-lookup"><span data-stu-id="5e6b2-123">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e6b2-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="5e6b2-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="5e6b2-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="5e6b2-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="5e6b2-126">啟用物件</span><span class="sxs-lookup"><span data-stu-id="5e6b2-126">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




