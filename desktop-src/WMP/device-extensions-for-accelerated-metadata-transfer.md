---
title: 加速中繼資料傳輸的裝置擴充功能
description: 加速中繼資料傳輸的裝置擴充功能
ms.assetid: a79b54d4-dad5-411b-aaff-b58bb549d4d1
keywords:
- Windows Media Player、裝置擴充功能
- Windows Media Player、延伸模組
- Windows Media Player，加速中繼資料傳輸
- Windows Media Player，中繼資料加速傳送
- 加速中繼資料傳輸
- 中繼資料，加速傳送
- 裝置延伸模組，加速中繼資料傳輸
- 延伸模組，加速中繼資料傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe661dff0750f2ad46bef96e537b0852d480db8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021699"
---
# <a name="device-extensions-for-accelerated-metadata-transfer"></a><span data-ttu-id="03fce-111">加速中繼資料傳輸的裝置擴充功能</span><span class="sxs-lookup"><span data-stu-id="03fce-111">Device Extensions for Accelerated Metadata Transfer</span></span>

<span data-ttu-id="03fce-112">Windows Media Player 10 引進了新的擴充功能，可讓您以可攜式裝置同步處理數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="03fce-112">Windows Media Player 10 introduced new and extended functionality for synchronizing digital media files with portable devices.</span></span> <span data-ttu-id="03fce-113">使用者可以將裝置連線到電腦、將內容傳輸到裝置，然後中斷裝置的連線，以享用離開電腦的內容。</span><span class="sxs-lookup"><span data-stu-id="03fce-113">Users can connect a device to a computer, transfer content to the device, and then disconnect the device to enjoy content away from the computer.</span></span>

<span data-ttu-id="03fce-114">當使用者將裝置重新連線至電腦時，裝置上儲存的內容可能會在上一次連線之後變更。</span><span class="sxs-lookup"><span data-stu-id="03fce-114">When the user reconnects the device to the computer, it is possible that the content stored on the device changed since the previous connection.</span></span> <span data-ttu-id="03fce-115">例如，只要播放特定的數位媒體檔案，就會導致該專案的播放次數變更。</span><span class="sxs-lookup"><span data-stu-id="03fce-115">For example, simply playing a particular digital media file causes the play count for that item to change.</span></span> <span data-ttu-id="03fce-116">因為目前的可攜式裝置可儲存大量的數位媒體內容，所以如果需要 Windows Media Player 來列舉和檢查每個數位媒體專案，探索變更的程式會太過耗時。</span><span class="sxs-lookup"><span data-stu-id="03fce-116">Because current portable devices can store large quantities of digital media content, the process of discovering changes would be too time consuming if Windows Media Player were required to enumerate and inspect each digital media item.</span></span> <span data-ttu-id="03fce-117">相反地，可攜式裝置製造商可以實行特殊功能來啟用 Windows Media Player 10 或更新版本，以有效率地取得裝置上所儲存內容變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="03fce-117">Instead, portable device manufacturers can implement special functionality to enable Windows Media Player 10 or later to efficiently retrieve information about changes made to the content stored on a device.</span></span>

<span data-ttu-id="03fce-118">下列各節說明用來執行此功能的慣例。</span><span class="sxs-lookup"><span data-stu-id="03fce-118">The following sections describe the conventions used to implement this functionality.</span></span>

-   [<span data-ttu-id="03fce-119">關於中繼資料</span><span class="sxs-lookup"><span data-stu-id="03fce-119">About the Metadata</span></span>](about-the-metadata.md)
-   [<span data-ttu-id="03fce-120">適用于中繼資料傳輸的 MTP 裝置擴充功能</span><span class="sxs-lookup"><span data-stu-id="03fce-120">MTP Device Extensions for Metadata Transfer</span></span>](mtp-device-extensions-for-metadata-transfer.md)
-   [<span data-ttu-id="03fce-121">適用于中繼資料傳輸的 Windows Media 裝置管理員裝置擴充功能</span><span class="sxs-lookup"><span data-stu-id="03fce-121">Windows Media Device Manager Device Extensions for Metadata Transfer</span></span>](windows-media-device-manager-device-extensions-for-metadata-transfer.md)

## <a name="related-topics"></a><span data-ttu-id="03fce-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="03fce-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03fce-123">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="03fce-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




