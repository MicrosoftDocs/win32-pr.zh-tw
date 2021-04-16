---
title: 取得必要的 DRM 程式庫
description: 取得必要的 DRM 程式庫
ms.assetid: 7bd13b77-439e-40cf-99e8-b359247da74d
keywords:
- Windows Media Format SDK，取得必要的 DRM 程式庫
- Advanced Systems Format (ASF) ，取得必要的 DRM 程式庫
- ASF (Advanced Systems Format) ，取得必要的 DRM 程式庫
- 數位版權管理 (DRM) ，取得必要的程式庫
- DRM (數位版權管理) ，取得必要的程式庫
- 數位版權管理 (DRM) ，組建資訊
- DRM (數位版權管理) ，組建資訊
- 數位版權管理 (DRM) ，調試資訊
- DRM (數位版權管理) ，調試資訊
- 偵測 DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c124c1e7edf0bba736b9dd392e852aac97e96
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383130"
---
# <a name="obtaining-the-required-drm-library"></a><span data-ttu-id="a1078-113">取得必要的 DRM 程式庫</span><span class="sxs-lookup"><span data-stu-id="a1078-113">Obtaining the Required DRM Library</span></span>

<span data-ttu-id="a1078-114">若要建立或播放受 DRM 保護的數位媒體檔案，您的應用程式必須連結至 Microsoft 以二進位格式提供的靜態程式庫。</span><span class="sxs-lookup"><span data-stu-id="a1078-114">To create or play DRM-protected digital media files, your application must link to a static library that is provided in binary form by Microsoft.</span></span> <span data-ttu-id="a1078-115">此程式庫有時稱為存根程式庫或「stublib」，它可唯一識別您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a1078-115">This library is sometimes called a stub library or "stublib" and it uniquely identifies your application.</span></span>

<span data-ttu-id="a1078-116">在此檔中，DRM 程式庫稱為「WMStubDRM .lib」。</span><span class="sxs-lookup"><span data-stu-id="a1078-116">In this documentation, the DRM library is referred to as "WMStubDRM.lib".</span></span> <span data-ttu-id="a1078-117">您所收到的程式庫名稱將包含識別編號。</span><span class="sxs-lookup"><span data-stu-id="a1078-117">The name of the library you receive will include an identifying number.</span></span> <span data-ttu-id="a1078-118">若要取得此程式庫，您必須簽署 Microsoft 的授權合約。</span><span class="sxs-lookup"><span data-stu-id="a1078-118">To obtain this library, you must sign a license agreement with Microsoft.</span></span> <span data-ttu-id="a1078-119">合約條款可能會根據您是否要求評估授權或生產授權而有所不同。</span><span class="sxs-lookup"><span data-stu-id="a1078-119">The terms of the agreement may differ depending on whether you request an evaluation license or a production license.</span></span> <span data-ttu-id="a1078-120">如需 DRM 授權流程的詳細資訊，請參閱 [Microsoft](https://www.microsoft.com/licensing/default)網站上的 Windows Media 授權表單。</span><span class="sxs-lookup"><span data-stu-id="a1078-120">For more information on the DRM licensing process, see the Windows Media Licensing Form at the [Microsoft Web site](https://www.microsoft.com/licensing/default).</span></span>

<span data-ttu-id="a1078-121">您收到的程式庫具有 DRM 安全性等級，這取決於您輸入的授權合約類型。</span><span class="sxs-lookup"><span data-stu-id="a1078-121">The library that you receive has a DRM security level that depends on the type of license agreement you enter into.</span></span> <span data-ttu-id="a1078-122">DRM 授權可以在指定的安全性層級下，限制具有 DRM 元件的應用程式存取檔案內容。</span><span class="sxs-lookup"><span data-stu-id="a1078-122">A DRM license can restrict applications with DRM components below a specified security level from accessing the file contents.</span></span> <span data-ttu-id="a1078-123">此安全性層級與 DRM 的個人化層級不同，它與輸出保護層級的任何數值 (OPLs) 無關。</span><span class="sxs-lookup"><span data-stu-id="a1078-123">This security level is not the same as the DRM individualization level, nor is it related to any of the numerical values of output protection levels (OPLs).</span></span> <span data-ttu-id="a1078-124">下表顯示不同播放程式和可攜式裝置的 DRM 安全性層級範例。</span><span class="sxs-lookup"><span data-stu-id="a1078-124">The following table shows examples of DRM security levels for different players and portable devices.</span></span>



| <span data-ttu-id="a1078-125">安全性層級</span><span class="sxs-lookup"><span data-stu-id="a1078-125">Security level</span></span> | <span data-ttu-id="a1078-126">播放機和可攜式裝置</span><span class="sxs-lookup"><span data-stu-id="a1078-126">Players and portable devices</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="a1078-127">範例</span><span class="sxs-lookup"><span data-stu-id="a1078-127">Example</span></span>                                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1078-128">150</span><span class="sxs-lookup"><span data-stu-id="a1078-128">150</span></span>            | <span data-ttu-id="a1078-129">不支援 Windows Media DRM 的裝置。</span><span class="sxs-lookup"><span data-stu-id="a1078-129">Devices that do not support Windows Media DRM.</span></span> <span data-ttu-id="a1078-130">將內容傳輸到這類裝置時，會移除 DRM 保護。</span><span class="sxs-lookup"><span data-stu-id="a1078-130">DRM protection is removed when content is transferred to such a device.</span></span>                                                                                                                                                                                                         | <span data-ttu-id="a1078-131">支援 Windows Media 內容但不受保護內容的裝置</span><span class="sxs-lookup"><span data-stu-id="a1078-131">Devices that support Windows Media-based content but not protected content</span></span>                                                                                                                       |
| <span data-ttu-id="a1078-132">1,000</span><span class="sxs-lookup"><span data-stu-id="a1078-132">1,000</span></span>          | <span data-ttu-id="a1078-133">以 Windows Media Format 9.5 SDK 或更早版本為基礎的播放機應用程式，不符合等級2000的其他需求。以 Windows Media 可攜式裝置 DRM v1 為基礎的裝置。</span><span class="sxs-lookup"><span data-stu-id="a1078-133">Player applications based on the Windows Media Format 9.5 SDK or earlier that do not meet additional requirements for level 2000.Devices based on Windows Media Portable Device DRM v1.</span></span><br/> <span data-ttu-id="a1078-134">以 Windows CE 4.2 和更新版本為基礎的裝置。</span><span class="sxs-lookup"><span data-stu-id="a1078-134">Devices based on Windows CE 4.2 and later.</span></span><br/>                                                                       | <span data-ttu-id="a1078-135">Windows Media Player 6.4，Windows Media Player 7Portable 支援 Windows Media 可攜式裝置 DRM v1 的媒體裝置。</span><span class="sxs-lookup"><span data-stu-id="a1078-135">Windows Media Player 6.4, Windows Media Player 7Portable media devices that support Windows Media Portable Device DRM v1.</span></span><br/>                                                             |
| <span data-ttu-id="a1078-136">2,000</span><span class="sxs-lookup"><span data-stu-id="a1078-136">2,000</span></span>          | <span data-ttu-id="a1078-137">以 Windows Media Format 9 系列 SDK 或更新版本為基礎的播放程式應用程式，並遵循比層級1000的應用程式更嚴格的內容保護指導方針。以 Windows Media DRM 10 作為可攜式裝置的裝置為基礎。</span><span class="sxs-lookup"><span data-stu-id="a1078-137">Player applications that are based on Windows Media Format 9 Series SDK or later, and that follow a stricter set of content protection guidelines than applications at level 1000.Devices based on Windows Media DRM 10 for Portable Devices.</span></span><br/> <span data-ttu-id="a1078-138">以 Windows Media DRM 10 為基礎的裝置，適用于網路裝置。</span><span class="sxs-lookup"><span data-stu-id="a1078-138">Devices based on Windows Media DRM 10 for Network Devices.</span></span><br/> | <span data-ttu-id="a1078-139">適用于可攜式裝置的 Windows Media Player 9 系列和 laterPortable 媒體裝置支援 Windows Media DRM 10</span><span class="sxs-lookup"><span data-stu-id="a1078-139">Windows Media Player 9 Series and laterPortable media devices that support Windows Media DRM 10 for Portable Devices</span></span><br/> <span data-ttu-id="a1078-140">以 Windows Mobile 為基礎的便攜 Media Center 裝置</span><span class="sxs-lookup"><span data-stu-id="a1078-140">Portable Media Center devices based on Windows Mobile</span></span><br/> |



 

## <a name="build-and-debugging-information"></a><span data-ttu-id="a1078-141">組建和調試資訊</span><span class="sxs-lookup"><span data-stu-id="a1078-141">Build and Debugging Information</span></span>

<span data-ttu-id="a1078-142">當您連結到 WMStubDRM 時，請不要連結至 wmvcore .lib。</span><span class="sxs-lookup"><span data-stu-id="a1078-142">When you link to WMStubDRM.lib, do NOT link to wmvcore.lib.</span></span> <span data-ttu-id="a1078-143">如果應用程式連結至這兩個程式庫，DRM 元件將無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="a1078-143">The DRM component will not work properly if the application links to both libraries.</span></span>

<span data-ttu-id="a1078-144">DRM 元件中的使用者中斷點可防止應用程式的 debug 和 release 版本在偵錯工具內執行時存取受保護的內容。</span><span class="sxs-lookup"><span data-stu-id="a1078-144">A user breakpoint in the DRM component will prevent both debug and release versions of applications from accessing protected content when running inside the debugger.</span></span> <span data-ttu-id="a1078-145">若要針對應用程式中的 DRM 相關函式進行疑難排解，您必須撰寫自己的追蹤常式，將 **HRESULT** 值之類的資訊儲存到某個位置，例如記錄檔。</span><span class="sxs-lookup"><span data-stu-id="a1078-145">To troubleshoot DRM-related functions in your application, you must write your own trace routines that save information such as **HRESULT** values to some location such as a log file.</span></span>

<span data-ttu-id="a1078-146">如果您嘗試在已安裝 (的 SDK bits 的偵測版本的系統上執行應用程式的發行版本，或使用另一種方式進行) ，您將會在播放 DRM 版本7內容時遇到堆積錯誤。</span><span class="sxs-lookup"><span data-stu-id="a1078-146">If you attempt to run a release version of an application on a system with a debug version of the SDK bits installed (or the other way around), you will encounter heap errors during playback of DRM version 7 content.</span></span> <span data-ttu-id="a1078-147">請務必透過 debug SDK bits 來執行 debug 應用程式，並透過版本位發行應用程式。</span><span class="sxs-lookup"><span data-stu-id="a1078-147">Be sure to run debug applications over debug SDK bits, and release applications over release bits.</span></span> <span data-ttu-id="a1078-148">如果您以個別的 DRM 元件執行 SDK 的偵錯工具版本，則會發生相同的問題， (一律為發行組建) 。</span><span class="sxs-lookup"><span data-stu-id="a1078-148">The same problem will occur if you run a debug version of the SDK with an individualized DRM component (which is always a release build).</span></span>

<span data-ttu-id="a1078-149">**附注** 此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="a1078-149">**Notes** DRM is not supported by the x64-based version of this SDK.</span></span>

<span data-ttu-id="a1078-150">與 Windows Media Format 9.5 SDK 相關聯的 WMStubDRM .lib 檔案只能搭配 Microsoft Visual Studio .NET 2003 的元件使用。</span><span class="sxs-lookup"><span data-stu-id="a1078-150">The WMStubDRM.lib files that are associated with the Windows Media Format 9.5 SDK can be used only with the components of Microsoft Visual Studio  .NET 2003.</span></span> <span data-ttu-id="a1078-151">如果您使用較舊版本的存根程式庫，則不會有任何新的限制可供使用。</span><span class="sxs-lookup"><span data-stu-id="a1078-151">If you are using an older version of the stub library, there are no new restrictions for its use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1078-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="a1078-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1078-153">**啟用 DRM 支援**</span><span class="sxs-lookup"><span data-stu-id="a1078-153">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 





