---
title: IMsRdpClientAdvancedSettings7 VideoPlaybackMode 屬性
description: 指定或抓取表示影片播放模式的值。
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- VideoPlaybackMode 屬性遠端桌面服務
- VideoPlaybackMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，VideoPlaybackMode 屬性
- VideoPlaybackMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，VideoPlaybackMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385286"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a><span data-ttu-id="bcf94-108">IMsRdpClientAdvancedSettings7：： VideoPlaybackMode 屬性</span><span class="sxs-lookup"><span data-stu-id="bcf94-108">IMsRdpClientAdvancedSettings7::VideoPlaybackMode property</span></span>

<span data-ttu-id="bcf94-109">指定或抓取表示影片播放模式的值。</span><span class="sxs-lookup"><span data-stu-id="bcf94-109">Specifies or retrieves a value that indicates the video playback mode.</span></span>

<span data-ttu-id="bcf94-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bcf94-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf94-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcf94-111">Syntax</span></span>


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a><span data-ttu-id="bcf94-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="bcf94-112">Property value</span></span>

<span data-ttu-id="bcf94-113">指定影片播放模式的值。</span><span class="sxs-lookup"><span data-stu-id="bcf94-113">A value that specifies the video playback mode.</span></span>

<span data-ttu-id="bcf94-114">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="bcf94-114">The possible values are:</span></span>

<dt>

<span data-ttu-id="bcf94-115">1</span><span class="sxs-lookup"><span data-stu-id="bcf94-115">1</span></span>
</dt> <dd>

<span data-ttu-id="bcf94-116">預設的影片播放模式。</span><span class="sxs-lookup"><span data-stu-id="bcf94-116">The default video playback mode.</span></span> <span data-ttu-id="bcf94-117">當影片播放模式設定為此值時，影片重新導向是由 [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="bcf94-117">When the video playback mode is set to this value, video redirection is controlled by the [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) property.</span></span> <span data-ttu-id="bcf94-118">當 [ **AudioRedirectionMode** ] 屬性設定為 [ **音訊 \_ 模式重新 \_ 導向]** 時，會在用戶端上將影片解碼和轉譯。</span><span class="sxs-lookup"><span data-stu-id="bcf94-118">When the **AudioRedirectionMode** property is set to **AUDIO\_MODE\_REDIRECT**, video is decoded and rendered on the client.</span></span>

</dd> <dt>

<span data-ttu-id="bcf94-119">0</span><span class="sxs-lookup"><span data-stu-id="bcf94-119">0</span></span>
</dt> <dd>

<span data-ttu-id="bcf94-120">即使 [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) 設為 **音訊 \_ 模式重新 \_ 導向**，也會停用影片播放重新導向。</span><span class="sxs-lookup"><span data-stu-id="bcf94-120">Video playback redirection is disabled, even when [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) is set to **AUDIO\_MODE\_REDIRECT**.</span></span> <span data-ttu-id="bcf94-121">在此模式中，影片會在 RD 工作階段主機伺服器上進行解碼和轉譯。</span><span class="sxs-lookup"><span data-stu-id="bcf94-121">In this mode, video is decoded and rendered on the RD Session Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcf94-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcf94-122">Requirements</span></span>



| <span data-ttu-id="bcf94-123">需求</span><span class="sxs-lookup"><span data-stu-id="bcf94-123">Requirement</span></span> | <span data-ttu-id="bcf94-124">值</span><span class="sxs-lookup"><span data-stu-id="bcf94-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf94-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcf94-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf94-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bcf94-126">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="bcf94-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcf94-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf94-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bcf94-128">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="bcf94-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bcf94-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="bcf94-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf94-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bcf94-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf94-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcf94-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf94-132"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bcf94-133">IID</span><span class="sxs-lookup"><span data-stu-id="bcf94-133">IID</span></span><br/>                      | <span data-ttu-id="bcf94-134">IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="bcf94-134">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bcf94-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcf94-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf94-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bcf94-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bcf94-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bcf94-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





