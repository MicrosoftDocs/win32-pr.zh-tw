---
title: IMsRdpClientAdvancedSettings7 介面
description: 公開管理 ActiveX 控制項之 advanced 設定的方法和屬性。
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106994973"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a><span data-ttu-id="b0bc2-105">IMsRdpClientAdvancedSettings7 介面</span><span class="sxs-lookup"><span data-stu-id="b0bc2-105">IMsRdpClientAdvancedSettings7 interface</span></span>

<span data-ttu-id="b0bc2-106">公開管理 ActiveX 控制項之 advanced 設定的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-106">Exposes methods and properties that manage advanced settings of the ActiveX control.</span></span>

<span data-ttu-id="b0bc2-107">若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-107">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="b0bc2-108">然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings7** 傳遞給 **QueryInterface**。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-108">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings7** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="b0bc2-109">成員</span><span class="sxs-lookup"><span data-stu-id="b0bc2-109">Members</span></span>

<span data-ttu-id="b0bc2-110">**IMsRdpClientAdvancedSettings7** 介面繼承自 **IMsRdpClientAdvancedSettings6**。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-110">The **IMsRdpClientAdvancedSettings7** interface inherits from **IMsRdpClientAdvancedSettings6**.</span></span> <span data-ttu-id="b0bc2-111">**IMsRdpClientAdvancedSettings7** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b0bc2-111">**IMsRdpClientAdvancedSettings7** also has these types of members:</span></span>

-   [<span data-ttu-id="b0bc2-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b0bc2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0bc2-113">屬性</span><span class="sxs-lookup"><span data-stu-id="b0bc2-113">Properties</span></span>

<span data-ttu-id="b0bc2-114">**IMsRdpClientAdvancedSettings7** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-114">The **IMsRdpClientAdvancedSettings7** interface has these properties.</span></span>



| <span data-ttu-id="b0bc2-115">屬性</span><span class="sxs-lookup"><span data-stu-id="b0bc2-115">Property</span></span>                                                                                                    | <span data-ttu-id="b0bc2-116">存取類型</span><span class="sxs-lookup"><span data-stu-id="b0bc2-116">Access type</span></span>           | <span data-ttu-id="b0bc2-117">Description</span><span class="sxs-lookup"><span data-stu-id="b0bc2-117">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0bc2-118">**AudioCaptureRedirectionMode**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-118">**AudioCaptureRedirectionMode**</span></span>](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | <span data-ttu-id="b0bc2-119">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b0bc2-119">Read/write</span></span><br/> | <span data-ttu-id="b0bc2-120">指定或抓取值，指出是否將預設音訊輸入裝置從用戶端重新導向至遠端會話。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-120">Specifies or retrieves a value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span><br/> |
| [<span data-ttu-id="b0bc2-121">**AudioQualityMode**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-121">**AudioQualityMode**</span></span>](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | <span data-ttu-id="b0bc2-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b0bc2-122">Read/write</span></span><br/> | <span data-ttu-id="b0bc2-123">指定或抓取值，指出重新導向音訊的音訊品質模式設定。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-123">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span><br/>                                        |
| [<span data-ttu-id="b0bc2-124">**EnableSuperPan**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-124">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | <span data-ttu-id="b0bc2-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b0bc2-125">Read/write</span></span><br/> | <span data-ttu-id="b0bc2-126">指定或抓取值，指出 SuperPan 是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-126">Specifies or retrieves a value that indicates whether SuperPan is enabled or disabled.</span></span><br/>                                                    |
| [<span data-ttu-id="b0bc2-127">**NetworkConnectionType**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-127">**NetworkConnectionType**</span></span>](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | <span data-ttu-id="b0bc2-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b0bc2-128">Read/write</span></span><br/> | <span data-ttu-id="b0bc2-129">指定或抓取表示網路連接類型的值。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-129">Specifies or retrieves a value that indicates the network connection type.</span></span><br/>                                                                |
| [<span data-ttu-id="b0bc2-130">**RedirectDirectX**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-130">**RedirectDirectX**</span></span>](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | <span data-ttu-id="b0bc2-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b0bc2-131">Read/write</span></span><br/> | <span data-ttu-id="b0bc2-132">不會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-132">This property is not used.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="b0bc2-133">**SuperPanAccelerationFactor**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-133">**SuperPanAccelerationFactor**</span></span>](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | <span data-ttu-id="b0bc2-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b0bc2-134">Read/write</span></span><br/> | <span data-ttu-id="b0bc2-135">指定或抓取表示 SuperPan 加速因素的值。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-135">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span><br/>                                                           |
| [<span data-ttu-id="b0bc2-136">**VideoPlaybackMode**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-136">**VideoPlaybackMode**</span></span>](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | <span data-ttu-id="b0bc2-137">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b0bc2-137">Read/write</span></span><br/> | <span data-ttu-id="b0bc2-138">指定或抓取表示影片播放模式的值。</span><span class="sxs-lookup"><span data-stu-id="b0bc2-138">Specifies or retrieves a value that indicates the video playback mode.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="b0bc2-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0bc2-139">Requirements</span></span>



| <span data-ttu-id="b0bc2-140">需求</span><span class="sxs-lookup"><span data-stu-id="b0bc2-140">Requirement</span></span> | <span data-ttu-id="b0bc2-141">值</span><span class="sxs-lookup"><span data-stu-id="b0bc2-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0bc2-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0bc2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b0bc2-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b0bc2-143">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="b0bc2-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0bc2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b0bc2-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b0bc2-145">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="b0bc2-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b0bc2-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="b0bc2-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0bc2-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b0bc2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="b0bc2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0bc2-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0bc2-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b0bc2-150">IID</span><span class="sxs-lookup"><span data-stu-id="b0bc2-150">IID</span></span><br/>                      | <span data-ttu-id="b0bc2-151">IID \_ IMsRdpClientAdvancedSettings7 定義為26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="b0bc2-151">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0bc2-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0bc2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0bc2-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b0bc2-154">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-154">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b0bc2-155">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-155">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b0bc2-156">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-156">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="b0bc2-157">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-157">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b0bc2-158">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-158">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b0bc2-159">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b0bc2-159">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

