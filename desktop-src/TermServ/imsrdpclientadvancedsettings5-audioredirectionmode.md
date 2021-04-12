---
title: IMsRdpClientAdvancedSettings5 AudioRedirectionMode 屬性
description: 設定及抓取音訊重新導向模式和不同的音訊重新導向選項。
ms.assetid: c0f5762b-00fd-40bb-ac97-3351b999f38d
ms.tgt_platform: multiple
keywords:
- AudioRedirectionMode 屬性遠端桌面服務
- AudioRedirectionMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，AudioRedirectionMode 屬性
- AudioRedirectionMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，AudioRedirectionMode 屬性
- AudioRedirectionMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，AudioRedirectionMode 屬性
- AudioRedirectionMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，AudioRedirectionMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings5.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings6.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings7.put_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.get_AudioRedirectionMode
- IMsRdpClientAdvancedSettings8.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40be8b8e63f210d060c0f585c9fe31328ac6ed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317187"
---
# <a name="imsrdpclientadvancedsettings5audioredirectionmode-property"></a><span data-ttu-id="ba499-112">IMsRdpClientAdvancedSettings5：： AudioRedirectionMode 屬性</span><span class="sxs-lookup"><span data-stu-id="ba499-112">IMsRdpClientAdvancedSettings5::AudioRedirectionMode property</span></span>

<span data-ttu-id="ba499-113">設定及抓取音訊重新導向模式和不同的音訊重新導向選項。</span><span class="sxs-lookup"><span data-stu-id="ba499-113">Sets and retrieves the audio redirection mode and different audio redirection options.</span></span>

<span data-ttu-id="ba499-114">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ba499-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba499-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba499-115">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  UINT uiAudioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] UINT *puiAudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="ba499-116">屬性值</span><span class="sxs-lookup"><span data-stu-id="ba499-116">Property value</span></span>

<span data-ttu-id="ba499-117">為音訊重新導向模式設定不同的值。</span><span class="sxs-lookup"><span data-stu-id="ba499-117">Sets different values for the audio redirection mode.</span></span> <span data-ttu-id="ba499-118">此參數具有下列可能的值。</span><span class="sxs-lookup"><span data-stu-id="ba499-118">This parameter has the following possible values.</span></span>

<dt>

<span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span>

<span data-ttu-id="ba499-119">**音訊 \_模式重新 \_ 導向 0** (啟用音訊重新導向，而重新導向的選項為「帶入這部電腦」。</span><span class="sxs-lookup"><span data-stu-id="ba499-119">**AUDIO\_MODE\_REDIRECT 0** (Audio redirection is enabled and the option for redirection is "Bring to this computer".</span></span> <span data-ttu-id="ba499-120">這是預設模式。 ) </span><span class="sxs-lookup"><span data-stu-id="ba499-120">This is the default mode.)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span>

<span data-ttu-id="ba499-121">**音訊 \_\_ \_ 在 \_ 伺服器1上播放的模式** (已啟用音訊重新導向，且此選項為「在遠端電腦上離開」。</span><span class="sxs-lookup"><span data-stu-id="ba499-121">**AUDIO\_MODE\_PLAY\_ON\_SERVER 1** (Audio redirection is enabled and the option is "Leave at remote computer".</span></span> <span data-ttu-id="ba499-122">只有從遠端連線到執行 Windows Vista 的主機電腦時，才支援「離開遠端電腦」選項。</span><span class="sxs-lookup"><span data-stu-id="ba499-122">The "Leave at remote computer" option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="ba499-123">如果連接到執行 Windows Server 2008 的主機電腦，[離開遠端電腦] 選項會變更為 [不播放]。 ) </span><span class="sxs-lookup"><span data-stu-id="ba499-123">If the connection is to a host computer that is running Windows Server 2008, the option "Leave at remote computer" is changed to "Do not play".)</span></span>


</dt> <dd></dd> <dt>

<span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span>

<span data-ttu-id="ba499-124">**音訊 \_模式 \_ NONE 2** (音訊重新導向已啟用，且模式為「不播放」。 ) </span><span class="sxs-lookup"><span data-stu-id="ba499-124">**AUDIO\_MODE\_NONE 2** (Audio redirection is enabled and the mode is "Do not play".)</span></span>


<span data-ttu-id="ba499-125"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ba499-125"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ba499-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba499-126">Requirements</span></span>



| <span data-ttu-id="ba499-127">需求</span><span class="sxs-lookup"><span data-stu-id="ba499-127">Requirement</span></span> | <span data-ttu-id="ba499-128">值</span><span class="sxs-lookup"><span data-stu-id="ba499-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba499-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba499-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ba499-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba499-130">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="ba499-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba499-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ba499-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba499-132">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="ba499-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ba499-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba499-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba499-134"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ba499-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ba499-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba499-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba499-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="ba499-137">IID</span><span class="sxs-lookup"><span data-stu-id="ba499-137">IID</span></span><br/>                      | <span data-ttu-id="ba499-138">IID \_ IMsRdpClientAdvancedSettings5 定義為 FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="ba499-138">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba499-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba499-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba499-140">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ba499-140">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ba499-141">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ba499-141">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ba499-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ba499-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ba499-143">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ba499-143">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





