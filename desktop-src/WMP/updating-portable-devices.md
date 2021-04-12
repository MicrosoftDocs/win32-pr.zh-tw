---
title: 更新可攜式裝置
description: 更新可攜式裝置
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Windows Media Player 線上商店，更新可攜式裝置
- 線上商店，更新可攜式裝置
- 輸入1個線上商店，更新可攜式裝置
- Windows Media Player 線上商店、可攜式裝置
- 線上商店、可攜式裝置
- 輸入1個線上商店、可攜式裝置
- 更新可攜式裝置
- 可攜式裝置，更新
- 可攜式裝置，Windows Media Player 線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314226"
---
# <a name="updating-portable-devices"></a><span data-ttu-id="b5247-112">更新可攜式裝置</span><span class="sxs-lookup"><span data-stu-id="b5247-112">Updating Portable Devices</span></span>

<span data-ttu-id="b5247-113">Windows Media Player 可讓使用者與可攜式裝置同步處理數位媒體內容。</span><span class="sxs-lookup"><span data-stu-id="b5247-113">Windows Media Player enables users to synchronize digital media content with portable devices.</span></span> <span data-ttu-id="b5247-114">這可能包含從線上商店購買或出租的音樂內容。</span><span class="sxs-lookup"><span data-stu-id="b5247-114">This can include music content purchased or rented from an online store.</span></span> <span data-ttu-id="b5247-115">在某些情況下，線上商店提供者可能會想要在管理存放區所提供的內容時，撰寫程式碼以在連接的可攜式裝置上運作。</span><span class="sxs-lookup"><span data-stu-id="b5247-115">Under some circumstances, online store providers might want to write code to work on a connected portable device as part of managing content provided by the store.</span></span> <span data-ttu-id="b5247-116">為了讓線上商店外掛程式有機會使用連線的裝置，Windows Media Player 會呼叫 [IWMPContentPartner：： UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) ，並提供可攜式裝置的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="b5247-116">To give the online store plug-in the opportunity to work with a connected device, Windows Media Player calls [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) and provides the canonical name of the portable device.</span></span> <span data-ttu-id="b5247-117">如果外掛程式程式碼判斷必須使用連線的裝置來完成一些工作，則在 \_ 繼續執行工作之前，它必須立即從呼叫 **UpdateDevice** 傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="b5247-117">If the plug-in code determines that some work must be done with the connected device, it must immediately return S\_OK from the call to **UpdateDevice** before proceeding to do the work.</span></span> <span data-ttu-id="b5247-118">如果沒有要執行的工作，外掛程式應該會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b5247-118">If there is no work to do, the plug-in should return an error code.</span></span>

<span data-ttu-id="b5247-119">當外掛程式完成使用裝置時，它必須呼叫 [IWMPContentPartnerCallback：： UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) ，以通知 Windows Media Player 裝置可供使用。</span><span class="sxs-lookup"><span data-stu-id="b5247-119">When the plug-in has finished using the device, it must call [IWMPContentPartnerCallback::UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) to notify Windows Media Player that the device is available.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5247-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5247-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5247-121">**類型1線上商店的程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="b5247-121">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




