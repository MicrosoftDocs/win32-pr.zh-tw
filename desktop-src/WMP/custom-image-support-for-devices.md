---
title: 裝置的自訂映射支援
description: 裝置的自訂映射支援
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Windows Media Player，適用于裝置的自訂映射支援
- Windows Media Player，適用于裝置的映射支援
- 裝置自訂映射支援
- 裝置的自訂映射支援
- 裝置的映射支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968912"
---
# <a name="custom-image-support-for-devices"></a><span data-ttu-id="ed21d-108">裝置的自訂映射支援</span><span class="sxs-lookup"><span data-stu-id="ed21d-108">Custom Image Support for Devices</span></span>

> [!Note]  
> <span data-ttu-id="ed21d-109">本節說明使用 Windows XP 作業系統時可用 Windows Media Player 10 的功能。</span><span class="sxs-lookup"><span data-stu-id="ed21d-109">This section documents a feature of Windows Media Player 10 that is available when using the Windows XP operating system.</span></span> <span data-ttu-id="ed21d-110">它可能在後續版本中無法使用。</span><span class="sxs-lookup"><span data-stu-id="ed21d-110">It may be unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ed21d-111">裝置製造商可以提供兩個特殊的影像檔案，以自訂裝置在 Windows Media Player 10 使用者介面中的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="ed21d-111">Device manufacturers can provide two special image files to customize the way a device is represented in the Windows Media Player 10 user interface.</span></span> <span data-ttu-id="ed21d-112">這兩個檔案是：</span><span class="sxs-lookup"><span data-stu-id="ed21d-112">These two files are:</span></span>

-   <span data-ttu-id="ed21d-113">DevIcon. fil。</span><span class="sxs-lookup"><span data-stu-id="ed21d-113">DevIcon.fil.</span></span> <span data-ttu-id="ed21d-114">代表裝置硬體的 Windows 圖示格式檔案。</span><span class="sxs-lookup"><span data-stu-id="ed21d-114">A Windows icon format file that represents the device hardware.</span></span> <span data-ttu-id="ed21d-115">此影像會顯示在 Windows Media Player 10 的任何位置，圖示會用來代表裝置，例如 **同步** 處理功能中的裝置清單。</span><span class="sxs-lookup"><span data-stu-id="ed21d-115">This image displays in Windows Media Player 10 anywhere an icon is used to represent a device, such as the device list in the **Sync** feature.</span></span>
-   <span data-ttu-id="ed21d-116">DevLogo. fil。</span><span class="sxs-lookup"><span data-stu-id="ed21d-116">DevLogo.fil.</span></span> <span data-ttu-id="ed21d-117">PNG 格式檔案，代表裝置製造商的公司標誌。</span><span class="sxs-lookup"><span data-stu-id="ed21d-117">A PNG format file that represents the corporate logo of the device manufacturer.</span></span> <span data-ttu-id="ed21d-118">此影像會顯示在使用 Windows Media Player 10 位公司商標的位置，例如 [ **裝置設定** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ed21d-118">This image displays in Windows Media Player 10 anywhere corporate branding is used, such as the **Device Setup** dialog box.</span></span>

## <a name="general-guidelines-for-images"></a><span data-ttu-id="ed21d-119">影像的一般方針</span><span class="sxs-lookup"><span data-stu-id="ed21d-119">General Guidelines for Images</span></span>

<span data-ttu-id="ed21d-120">下列指導方針一般適用于自訂映射支援：</span><span class="sxs-lookup"><span data-stu-id="ed21d-120">The following guidelines apply to custom image support in general:</span></span>

-   <span data-ttu-id="ed21d-121">此功能是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ed21d-121">This feature is optional.</span></span> <span data-ttu-id="ed21d-122">未提供映射的裝置將會以預設影像表示。</span><span class="sxs-lookup"><span data-stu-id="ed21d-122">Devices that do not supply images will be represented by default images.</span></span>
-   <span data-ttu-id="ed21d-123">只有已啟用 MTP 的裝置才支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="ed21d-123">This feature is supported for MTP-enabled devices only.</span></span>
-   <span data-ttu-id="ed21d-124">若要防止變更檔案，建議將影像檔儲存在固件或受保護的儲存媒體中，而不是使用使用者建立的檔案。</span><span class="sxs-lookup"><span data-stu-id="ed21d-124">To prevent changes to the files, it is recommended that the image files be stored in firmware or a protected storage medium, not with user-created files.</span></span>
-   <span data-ttu-id="ed21d-125">這些檔案不應該傳回給 Windows Media 裝置管理員用戶端，以列舉裝置的根儲存體。</span><span class="sxs-lookup"><span data-stu-id="ed21d-125">The files should not be returned to Windows Media Device Manager clients that enumerate the root storage of the device.</span></span> <span data-ttu-id="ed21d-126">此外，刪除、移動或重新命名檔案都應該會失敗。</span><span class="sxs-lookup"><span data-stu-id="ed21d-126">Also, deleting, moving, or renaming the files should fail.</span></span>
-   <span data-ttu-id="ed21d-127">如果裝置提供一個以上的儲存媒體，則裝置應該會傳回影像檔案，以回應來自任何媒體的檔案開啟要求。</span><span class="sxs-lookup"><span data-stu-id="ed21d-127">If the device provides more than one storage medium, the device should return the image files in response to file open requests from any medium.</span></span> <span data-ttu-id="ed21d-128">每個儲存媒體可能會傳回不同的裝置圖示。</span><span class="sxs-lookup"><span data-stu-id="ed21d-128">Different device icons may be returned from each storage medium.</span></span>
-   <span data-ttu-id="ed21d-129">裝置管理員針對已啟用1.2 功能的用戶端，這些映射會優先于 Windows 安裝程式機制（例如裝置節點屬性）所提供的圖示屬性。</span><span class="sxs-lookup"><span data-stu-id="ed21d-129">For Windows Media Device Manager 1.2-enabled clients, these images will take precedence over icon properties supplied by Windows setup mechanisms, such as device node properties.</span></span>
-   <span data-ttu-id="ed21d-130">映射不得包含任何需要當地語系化的資訊。</span><span class="sxs-lookup"><span data-stu-id="ed21d-130">The images must not contain any information that requires localization.</span></span>
-   <span data-ttu-id="ed21d-131">針對多函式裝置，只有 Windows XP 的音樂播放功能會使用這些映射。</span><span class="sxs-lookup"><span data-stu-id="ed21d-131">For multi-function devices, only the music playback features of Windows XP will use these images.</span></span>

## <a name="creating-the-device-icon-image"></a><span data-ttu-id="ed21d-132">建立裝置圖示影像</span><span class="sxs-lookup"><span data-stu-id="ed21d-132">Creating the Device Icon Image</span></span>

<span data-ttu-id="ed21d-133">裝置圖示影像檔（DevIcon. fil）必須包含 Windows 圖示格式的檔案。</span><span class="sxs-lookup"><span data-stu-id="ed21d-133">The device icon image file, DevIcon.fil, must contain a file in Windows icon format.</span></span> <span data-ttu-id="ed21d-134">[Win32 中](/previous-versions/ms997538(v=msdn.10))的 MSDN 文章圖示說明如何建立這類檔案。</span><span class="sxs-lookup"><span data-stu-id="ed21d-134">The MSDN article [Icons in Win32](/previous-versions/ms997538(v=msdn.10)) describes how to create such a file.</span></span> <span data-ttu-id="ed21d-135">[建立 WINDOWS Xp 圖示](/previous-versions/ms997636(v=msdn.10))的 MSDN 文章提供 windows xp 圖示的樣式指導方針。</span><span class="sxs-lookup"><span data-stu-id="ed21d-135">The MSDN article [Creating Windows XP Icons](/previous-versions/ms997636(v=msdn.10)) provides style guidelines for Windows XP icons.</span></span> <span data-ttu-id="ed21d-136">裝置圖示影像檔藉由提供四種不同的大小，每個都有三個不同的色彩深度，以將12個影像併入單一檔案中。</span><span class="sxs-lookup"><span data-stu-id="ed21d-136">The device icon image file incorporates twelve images in a single file by providing four different sizes with three different color depths each.</span></span>

<span data-ttu-id="ed21d-137">請務必特別注意下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="ed21d-137">Be certain to pay particular attention to the following guidelines:</span></span>

-   <span data-ttu-id="ed21d-138">建議的大小 (以圖元為單位) 為16x16、32x32、48x48 和256x256。</span><span class="sxs-lookup"><span data-stu-id="ed21d-138">Recommended sizes (in pixels) are 16x16, 32x32, 48x48, and 256x256.</span></span>
-   <span data-ttu-id="ed21d-139">建議的色彩深度為24位、8位 Alpha 色板、具有1位透明度的8位，以及具有1位透明度的4位。</span><span class="sxs-lookup"><span data-stu-id="ed21d-139">Recommended color depths are 24-bit with 8-bit alpha channel, 8-bit with 1-bit transparency, and 4-bit with 1-bit transparency.</span></span>
-   <span data-ttu-id="ed21d-140">使用先前所述 MSDN 文章中所述的透視圖角度和投影建議。</span><span class="sxs-lookup"><span data-stu-id="ed21d-140">Use the perspective angle and drop shadow recommendations described in the MSDN articles mentioned previously.</span></span>

<span data-ttu-id="ed21d-141">一旦您建立了圖示檔，只要將它重新命名為 DevIcon. fil。</span><span class="sxs-lookup"><span data-stu-id="ed21d-141">Once you have created the icon file, simply rename it DevIcon.fil.</span></span>

## <a name="creating-the-corporate-logo-image"></a><span data-ttu-id="ed21d-142">建立公司標誌影像</span><span class="sxs-lookup"><span data-stu-id="ed21d-142">Creating the Corporate Logo Image</span></span>

<span data-ttu-id="ed21d-143">公司標誌影像檔（DevLogo. fil）必須包含 PNG 格式的檔案。</span><span class="sxs-lookup"><span data-stu-id="ed21d-143">The corporate logo image file, DevLogo.fil, must contain a file in PNG format.</span></span> <span data-ttu-id="ed21d-144">建立映射時，請使用下列指導方針：</span><span class="sxs-lookup"><span data-stu-id="ed21d-144">Use the following guidelines when creating the image:</span></span>

-   <span data-ttu-id="ed21d-145">影像的大小上限為150x32 圖元。</span><span class="sxs-lookup"><span data-stu-id="ed21d-145">The maximum dimensions for the image are 150x32 pixels.</span></span>
-   <span data-ttu-id="ed21d-146">影像應該支援 Alpha 混色，以啟用 Windows Media Player 10 使用者介面和標誌之間的平滑轉換。</span><span class="sxs-lookup"><span data-stu-id="ed21d-146">The image should support alpha blending to enable a smooth transition between the Windows Media Player 10 user interface and the logo.</span></span>

<span data-ttu-id="ed21d-147">一旦您建立了公司標誌檔案，只要將它重新命名為 DevLogo. fil。</span><span class="sxs-lookup"><span data-stu-id="ed21d-147">Once you have created the corporate logo file, simply rename it DevLogo.fil.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed21d-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed21d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed21d-149">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="ed21d-149">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 