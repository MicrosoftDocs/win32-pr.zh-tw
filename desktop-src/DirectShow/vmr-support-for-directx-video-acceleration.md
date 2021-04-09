---
description: VMR DirectX Video 加速支援
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: VMR DirectX Video 加速支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691583"
---
# <a name="vmr-support-for-directx-video-acceleration"></a><span data-ttu-id="f71b1-103">VMR DirectX Video 加速支援</span><span class="sxs-lookup"><span data-stu-id="f71b1-103">VMR Support for DirectX Video Acceleration</span></span>

<span data-ttu-id="f71b1-104">DirectX Video 加速是 (API) 的應用程式開發介面，以及對應的設備磁碟機介面 (適用于硬體加速數位視訊解碼處理的 DDI) ，可支援子圖片 DVD 的支援。</span><span class="sxs-lookup"><span data-stu-id="f71b1-104">DirectX Video Acceleration is an Application Programming Interface (API) and a corresponding Device Driver Interface (DDI) for hardware acceleration of digital video decoding processing, with support of alpha blending for such purposes as DVD subpicture support.</span></span> <span data-ttu-id="f71b1-105">DirectX VA 記載于 Windows DDK 中。</span><span class="sxs-lookup"><span data-stu-id="f71b1-105">DirectX VA is documented in the Windows DDK.</span></span> <span data-ttu-id="f71b1-106">[**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)介面（可提供硬體裝置上的 DirectX VA 功能的使用者模式存取）記載于此 SDK 中。</span><span class="sxs-lookup"><span data-stu-id="f71b1-106">The [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, which provides user mode access to DirectX VA functionality on a hardware device, is documented in this SDK.</span></span>

<span data-ttu-id="f71b1-107">VMR 支援 [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)，而其執行與舊的重迭混音器完全相同，但有一個重要的差異。</span><span class="sxs-lookup"><span data-stu-id="f71b1-107">The VMR supports [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), and its implementation is identical to the old Overlay Mixer except for one important difference.</span></span> <span data-ttu-id="f71b1-108">覆迭混音器保證輸出會轉譯成重迭表面，而 VMR 可以傳送輸出以進行進一步的處理，例如3D 作業，或可能會將輸出傳送至螢幕介面，然後 blitted 至主要介面。</span><span class="sxs-lookup"><span data-stu-id="f71b1-108">The Overlay Mixer guaranteed that the output is rendered into an overlay surface, while the VMR can send the output for further processing, for example a 3D operation, or it might send the output to an offscreen surface which is then blitted to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f71b1-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="f71b1-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f71b1-110">關於 DirectX Video 加速</span><span class="sxs-lookup"><span data-stu-id="f71b1-110">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



