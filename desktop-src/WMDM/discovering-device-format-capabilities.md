---
title: 探索裝置格式功能
description: 探索裝置格式功能
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Windows Media 裝置管理員，裝置功能
- 裝置管理員，裝置功能
- 程式設計指南，裝置功能
- 桌面應用程式，裝置功能
- 建立 Windows Media 裝置管理員應用程式，裝置功能
- 將檔案寫入裝置、裝置功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ee05476f6b84bc85bb81cc7cff5815649f5842
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968218"
---
# <a name="discovering-device-format-capabilities"></a><span data-ttu-id="803b1-109">探索裝置格式功能</span><span class="sxs-lookup"><span data-stu-id="803b1-109">Discovering Device Format Capabilities</span></span>

<span data-ttu-id="803b1-110">您的應用程式可能會先嘗試判斷裝置的播放功能，然後再將檔案傳送給它。</span><span class="sxs-lookup"><span data-stu-id="803b1-110">Your application might try to determine a device's playback capabilities before sending a file to it.</span></span> <span data-ttu-id="803b1-111">如果裝置無法處理您想要傳送的檔案格式，您的應用程式可能會嘗試將檔案轉碼成裝置可使用的格式，或通知使用者裝置無法支援要求的檔案。</span><span class="sxs-lookup"><span data-stu-id="803b1-111">If a device cannot handle the format of a file you want to send, your application might attempt to transcode the file into a format that the device can use, or notify the user that the device cannot support the requested file.</span></span>

<span data-ttu-id="803b1-112">請注意，某些裝置（例如大型儲存裝置類別）可能只會作為卸除式存放裝置媒體，而不會有播放功能。</span><span class="sxs-lookup"><span data-stu-id="803b1-112">Note that some devices, such as mass storage class devices, might serve only as removable storage media without playback capabilities.</span></span> <span data-ttu-id="803b1-113">在這種情況下，您的應用程式在將檔案傳送到裝置之前，不適合轉碼檔案。</span><span class="sxs-lookup"><span data-stu-id="803b1-113">In this case, it would be inappropriate for your application to transcode a file before sending it to the device.</span></span>

<span data-ttu-id="803b1-114">雖然 [**IWMDMDevice：： GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) 方法可讓裝置報告其功能，但某些裝置會針對此方法傳回不正確的值。</span><span class="sxs-lookup"><span data-stu-id="803b1-114">Although the [**IWMDMDevice::GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) method enables a device to report its capabilities, some devices return incorrect values for this method.</span></span> <span data-ttu-id="803b1-115">將檔案複製到裝置之前，您可能會想要詢問使用者是否要播放，如果是，則嘗試將檔案轉碼為裝置的其中一種回報格式 (或合理格式，如果裝置宣告支援任何格式) 。</span><span class="sxs-lookup"><span data-stu-id="803b1-115">Before copying a file to a device, you might want to ask the user whether playback is intended, and if so, attempt to transcode the file to one of the device's reported formats (or a reasonable format, if the device claims support for any format).</span></span> <span data-ttu-id="803b1-116">另一種方法是假設裝置所支援的任何格式都是要播放，而所有其他檔案則應以未修改的方式傳輸。</span><span class="sxs-lookup"><span data-stu-id="803b1-116">Another approach is to assume that any formats specifically listed as supported by the device are intended for playback, and all other files should be transferred unmodified.</span></span>

<span data-ttu-id="803b1-117">探索要傳送的檔案格式以及裝置所支援的格式之後，您可以決定哪一個是轉碼的最佳目標格式。</span><span class="sxs-lookup"><span data-stu-id="803b1-117">After discovering the format of the file to be transferred, and the formats supported by a device, you can decide which is the best target format for transcoding.</span></span>

<span data-ttu-id="803b1-118">在過去，應用程式通常會針對屬性傳回零，以表示支援該屬性的任何值。</span><span class="sxs-lookup"><span data-stu-id="803b1-118">In the past, it was common for an application to return zero for a property to indicate support for any values of that property.</span></span> <span data-ttu-id="803b1-119">例如， [**\_ WAVEFORMATEX**](-waveformatex.md)的值為零時，nSamplesPerSec 會指出支援任何位元速率。</span><span class="sxs-lookup"><span data-stu-id="803b1-119">For example, a value of zero for [**\_WAVEFORMATEX**](-waveformatex.md).nSamplesPerSec would indicate support for any bit rate.</span></span> <span data-ttu-id="803b1-120">現在，建議的方法是指出對任何值的支援，就是 \_ \_ \_ \_ \_ 在 WMDM 的 [說明] [**\_ \_ DESC**](wmdm-prop-desc.md)中指定 WMDM 列舉的有效值。ValidValuesForm.</span><span class="sxs-lookup"><span data-stu-id="803b1-120">Now, the recommended way to indicate support for any value is to specify WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY in [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md).ValidValuesForm.</span></span> <span data-ttu-id="803b1-121">不過，某些屬性可以合法地傳回零以表示特定的支援。</span><span class="sxs-lookup"><span data-stu-id="803b1-121">Some properties, though, can legitimately return zero to indicate specific support.</span></span> <span data-ttu-id="803b1-122">例如，如果 [**\_ BITMAPINFOHEADER**](-bitmapinfoheader.md). biSizeImage 設定為零，則表示 BI \_ RGB 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="803b1-122">For example, if [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md).biSizeImage is set to zero, this indicates a BI\_RGB bitmap.</span></span> <span data-ttu-id="803b1-123">相關結構的檔中會注明零值的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="803b1-123">Exceptions for zero values are noted in the documentation for the relevant structures.</span></span>

<span data-ttu-id="803b1-124">不過，請務必注意，裝置通常不會正確地報告其格式功能，也不會以標準方式回報。</span><span class="sxs-lookup"><span data-stu-id="803b1-124">However, it is important to note that devices often do not report their format capabilities properly, or in a standard way.</span></span> <span data-ttu-id="803b1-125">例如，裝置通常會回報它們支援任何格式，事實上它們只能處理特定格式，或是格式類型內的特定位費率。</span><span class="sxs-lookup"><span data-stu-id="803b1-125">For example, devices often report that they support any format, when in fact they can only handle specific formats, or specific bit rates within a format type.</span></span> <span data-ttu-id="803b1-126">您可以決定應用程式是否應該接受這類報表，或是否應該對裝置的播放 (能力採用某種上限，例如 192 kbps) 。</span><span class="sxs-lookup"><span data-stu-id="803b1-126">It is up to you to decide whether your application should accept such reports, or whether it should assume some kind of upper limit to a device's playback abilities (for example, 192 kbps).</span></span>

<span data-ttu-id="803b1-127">要求裝置格式支援的建議方法是 [**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)。</span><span class="sxs-lookup"><span data-stu-id="803b1-127">The recommended method for requesting a device's format support is [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span> <span data-ttu-id="803b1-128">如果不支援這個方法，您的應用程式應該會在 [**IWMDMDevice：： GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)回復。</span><span class="sxs-lookup"><span data-stu-id="803b1-128">If this method is not supported, your application should fall back on [**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport).</span></span> <span data-ttu-id="803b1-129">**GetFormatSupport** 與 **GetFormatSupport2** 不同，不會傳回影片資訊。</span><span class="sxs-lookup"><span data-stu-id="803b1-129">**GetFormatSupport**, unlike **GetFormatSupport2**, does not return video information.</span></span>

<span data-ttu-id="803b1-130">應用程式要求裝置格式功能的方式取決於應用程式所支援的介面。</span><span class="sxs-lookup"><span data-stu-id="803b1-130">How an application requests a device's format capabilities depends on which interface the application supports.</span></span> <span data-ttu-id="803b1-131">如需詳細資料，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="803b1-131">For more details, see the following topics:</span></span>

-   [<span data-ttu-id="803b1-132">在支援 IWMDMDevice3 的裝置上取得格式功能</span><span class="sxs-lookup"><span data-stu-id="803b1-132">Getting Format Capabilities on Devices That Support IWMDMDevice3</span></span>](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [<span data-ttu-id="803b1-133">在僅支援 IWMDMDevice 的裝置上取得格式功能</span><span class="sxs-lookup"><span data-stu-id="803b1-133">Getting Format Capabilities on Devices That Support Only IWMDMDevice</span></span>](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a><span data-ttu-id="803b1-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="803b1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="803b1-135">**將檔案寫入至裝置**</span><span class="sxs-lookup"><span data-stu-id="803b1-135">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




