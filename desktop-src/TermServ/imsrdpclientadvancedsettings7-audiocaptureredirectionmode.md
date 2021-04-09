---
title: IMsRdpClientAdvancedSettings7 AudioCaptureRedirectionMode 屬性
description: 指定或抓取布林值，指出是否將預設音訊輸入裝置從用戶端重新導向至遠端會話。
ms.assetid: e75add5e-4652-41a7-b2cb-2c60793cd079
ms.tgt_platform: multiple
keywords:
- AudioCaptureRedirectionMode 屬性遠端桌面服務
- AudioCaptureRedirectionMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，AudioCaptureRedirectionMode 屬性
- AudioCaptureRedirectionMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，AudioCaptureRedirectionMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioCaptureRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioCaptureRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c752315067ed70103da2e048e9e8f613665ae919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934582"
---
# <a name="imsrdpclientadvancedsettings7audiocaptureredirectionmode-property"></a><span data-ttu-id="9c543-108">IMsRdpClientAdvancedSettings7：： AudioCaptureRedirectionMode 屬性</span><span class="sxs-lookup"><span data-stu-id="9c543-108">IMsRdpClientAdvancedSettings7::AudioCaptureRedirectionMode property</span></span>

<span data-ttu-id="9c543-109">指定或抓取布林值，指出是否將預設音訊輸入裝置從用戶端重新導向至遠端會話。</span><span class="sxs-lookup"><span data-stu-id="9c543-109">Specifies or retrieves a Boolean value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span>

<span data-ttu-id="9c543-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9c543-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c543-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c543-111">Syntax</span></span>


```C++
HRESULT put_AudioCaptureRedirectionMode(
  [in]          VARIANT_BOOL fRedir
);

HRESULT get_AudioCaptureRedirectionMode(
  [out, retval] VARIANT_BOOL *pfRedir
);
```



## <a name="property-value"></a><span data-ttu-id="9c543-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="9c543-112">Property value</span></span>

<span data-ttu-id="9c543-113">**VARIANT \_ BOOL** 值，指定是否重新導向音訊捕獲。</span><span class="sxs-lookup"><span data-stu-id="9c543-113">A **VARIANT\_BOOL** value that specifies whether audio capture is redirected.</span></span> <span data-ttu-id="9c543-114">如果您想要重新導向音訊捕捉，請指定 **VARIANT \_ TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="9c543-114">Specify **VARIANT\_TRUE** if you want audio capture to be redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c543-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c543-115">Requirements</span></span>



| <span data-ttu-id="9c543-116">需求</span><span class="sxs-lookup"><span data-stu-id="9c543-116">Requirement</span></span> | <span data-ttu-id="9c543-117">值</span><span class="sxs-lookup"><span data-stu-id="9c543-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c543-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c543-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9c543-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9c543-119">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="9c543-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c543-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9c543-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9c543-121">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="9c543-122">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9c543-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c543-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c543-123"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9c543-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9c543-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c543-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c543-125"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="9c543-126">IID</span><span class="sxs-lookup"><span data-stu-id="9c543-126">IID</span></span><br/>                      | <span data-ttu-id="9c543-127">IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="9c543-127">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c543-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c543-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c543-129">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9c543-129">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9c543-130">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9c543-130">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





