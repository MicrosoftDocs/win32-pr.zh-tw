---
title: IMsRdpClientAdvancedSettings7 AudioQualityMode 屬性
description: 指定或抓取值，指出重新導向音訊的音訊品質模式設定。 根據預設，這會設定為0。
ms.assetid: 9945c524-ca50-41ae-a7cf-1386cd758c0f
ms.tgt_platform: multiple
keywords:
- AudioQualityMode 屬性遠端桌面服務
- AudioQualityMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，AudioQualityMode 屬性
- AudioQualityMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，AudioQualityMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.AudioQualityMode
- IMsRdpClientAdvancedSettings7.get_AudioQualityMode
- IMsRdpClientAdvancedSettings7.put_AudioQualityMode
- IMsRdpClientAdvancedSettings8.AudioQualityMode
- IMsRdpClientAdvancedSettings8.get_AudioQualityMode
- IMsRdpClientAdvancedSettings8.put_AudioQualityMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdfc19176e03f8979e5adb25bf0c9eaf4ceed9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984961"
---
# <a name="imsrdpclientadvancedsettings7audioqualitymode-property"></a><span data-ttu-id="3356e-109">IMsRdpClientAdvancedSettings7：： AudioQualityMode 屬性</span><span class="sxs-lookup"><span data-stu-id="3356e-109">IMsRdpClientAdvancedSettings7::AudioQualityMode property</span></span>

<span data-ttu-id="3356e-110">指定或抓取值，指出重新導向音訊的音訊品質模式設定。</span><span class="sxs-lookup"><span data-stu-id="3356e-110">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span> <span data-ttu-id="3356e-111">根據預設，這會設定為0。</span><span class="sxs-lookup"><span data-stu-id="3356e-111">By default this is set to 0.</span></span>

<span data-ttu-id="3356e-112">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="3356e-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3356e-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="3356e-113">Syntax</span></span>


```C++
HRESULT put_AudioQualityMode(
  [in]          UINT audioQualityMode
);

HRESULT get_AudioQualityMode(
  [out, retval] UINT *pAudioQualityMode
);
```



## <a name="property-value"></a><span data-ttu-id="3356e-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="3356e-114">Property value</span></span>

<span data-ttu-id="3356e-115">指定音訊品質模式的值。</span><span class="sxs-lookup"><span data-stu-id="3356e-115">A value that specifies the audio quality mode.</span></span>

<span data-ttu-id="3356e-116">可能的值包括：</span><span class="sxs-lookup"><span data-stu-id="3356e-116">The possible values are:</span></span>

<dt>

<span data-ttu-id="3356e-117">0</span><span class="sxs-lookup"><span data-stu-id="3356e-117">0</span></span>
</dt> <dd>

<span data-ttu-id="3356e-118">動態音訊品質。</span><span class="sxs-lookup"><span data-stu-id="3356e-118">Dynamic audio quality.</span></span> <span data-ttu-id="3356e-119">這是預設的音訊品質設定。</span><span class="sxs-lookup"><span data-stu-id="3356e-119">This is the default audio quality setting.</span></span> <span data-ttu-id="3356e-120">伺服器會動態調整音訊輸出品質，以回應網路狀況和用戶端和伺服器功能。</span><span class="sxs-lookup"><span data-stu-id="3356e-120">The server dynamically adjusts audio output quality in response to network conditions and the client and server capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="3356e-121">1</span><span class="sxs-lookup"><span data-stu-id="3356e-121">1</span></span>
</dt> <dd>

<span data-ttu-id="3356e-122">中度音訊品質。</span><span class="sxs-lookup"><span data-stu-id="3356e-122">Medium audio quality.</span></span> <span data-ttu-id="3356e-123">伺服器會針對音訊輸出使用固定但壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="3356e-123">The server uses a fixed but compressed format for audio output.</span></span>

</dd> <dt>

<span data-ttu-id="3356e-124">2</span><span class="sxs-lookup"><span data-stu-id="3356e-124">2</span></span>
</dt> <dd>

<span data-ttu-id="3356e-125">高音訊品質。</span><span class="sxs-lookup"><span data-stu-id="3356e-125">High audio quality.</span></span> <span data-ttu-id="3356e-126">伺服器以未壓縮 PCM 格式提供音訊輸出，延遲的處理負荷較低。</span><span class="sxs-lookup"><span data-stu-id="3356e-126">The server provides audio output in uncompressed PCM format with lower processing overhead for latency.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3356e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3356e-127">Requirements</span></span>



| <span data-ttu-id="3356e-128">需求</span><span class="sxs-lookup"><span data-stu-id="3356e-128">Requirement</span></span> | <span data-ttu-id="3356e-129">值</span><span class="sxs-lookup"><span data-stu-id="3356e-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3356e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3356e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3356e-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3356e-131">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="3356e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3356e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3356e-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3356e-133">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="3356e-134">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3356e-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="3356e-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3356e-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3356e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3356e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3356e-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3356e-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3356e-138">IID</span><span class="sxs-lookup"><span data-stu-id="3356e-138">IID</span></span><br/>                      | <span data-ttu-id="3356e-139">IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="3356e-139">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3356e-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3356e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3356e-141">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3356e-141">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="3356e-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="3356e-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





