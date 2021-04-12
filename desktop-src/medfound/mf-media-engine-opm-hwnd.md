---
description: 指定媒體引擎將輸出保護管理員套用 (OPM) 保護的視窗。
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: 'MF_MEDIA_ENGINE_OPM_HWND 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945625"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a><span data-ttu-id="2fb92-103">MF \_ 媒體 \_ 引擎 \_ OPM \_ HWND 屬性</span><span class="sxs-lookup"><span data-stu-id="2fb92-103">MF\_MEDIA\_ENGINE\_OPM\_HWND attribute</span></span>

<span data-ttu-id="2fb92-104">指定媒體引擎將 [輸出保護管理員](output-protection-manager.md) 套用 (OPM) 保護的視窗。</span><span class="sxs-lookup"><span data-stu-id="2fb92-104">Specifies a window for the Media Engine to apply [Output Protection Manager](output-protection-manager.md) (OPM) protections.</span></span>

## <a name="data-type"></a><span data-ttu-id="2fb92-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="2fb92-105">Data type</span></span>

<span data-ttu-id="2fb92-106">**HWND** 儲存為 **UINT64**</span><span class="sxs-lookup"><span data-stu-id="2fb92-106">**HWND** stored as **UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="2fb92-107">備註</span><span class="sxs-lookup"><span data-stu-id="2fb92-107">Remarks</span></span>

<span data-ttu-id="2fb92-108">這個屬性會與 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) 方法搭配使用，以初始化 Media Engine。</span><span class="sxs-lookup"><span data-stu-id="2fb92-108">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="2fb92-109">若要針對影片播放啟用 OPM 保護，應用程式必須執行下列其中一項動作：</span><span class="sxs-lookup"><span data-stu-id="2fb92-109">To enable OPM protections for video playback, the application must do one of the following:</span></span>

-   <span data-ttu-id="2fb92-110">建立媒體引擎時，請設定 [MF \_ media \_ ENGINE \_ 播放 \_ HWND](mf-media-engine-playback-hwnd.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="2fb92-110">Set the [MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND](mf-media-engine-playback-hwnd.md) attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="2fb92-111">建立媒體引擎時，請設定 MF \_ media \_ ENGINE \_ OPM \_ HWND 屬性。</span><span class="sxs-lookup"><span data-stu-id="2fb92-111">Set the MF\_MEDIA\_ENGINE\_OPM\_HWND attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="2fb92-112">在建立媒體引擎之後，但在顯示受保護的內容之前，請在任何時間點呼叫 [**IMFMediaEngineProtectedContent：： SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) 。</span><span class="sxs-lookup"><span data-stu-id="2fb92-112">Call [**IMFMediaEngineProtectedContent::SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) at any point after creating the Media Engine, but before protected content is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fb92-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fb92-113">Requirements</span></span>



| <span data-ttu-id="2fb92-114">需求</span><span class="sxs-lookup"><span data-stu-id="2fb92-114">Requirement</span></span> | <span data-ttu-id="2fb92-115">值</span><span class="sxs-lookup"><span data-stu-id="2fb92-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb92-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fb92-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb92-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fb92-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="2fb92-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fb92-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb92-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fb92-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="2fb92-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2fb92-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fb92-121"><dt>Mfmediaengine。h</dt></span><span class="sxs-lookup"><span data-stu-id="2fb92-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fb92-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fb92-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb92-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="2fb92-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2fb92-124">媒體引擎屬性</span><span class="sxs-lookup"><span data-stu-id="2fb92-124">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> </dl>

 

 




