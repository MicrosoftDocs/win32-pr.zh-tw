---
description: VMR DirectX Video 加速支援
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: VMR DirectX Video 加速支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f1998f5e55d7aa4d191ac2a312995db69d9e248349034e119ded8e99774c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696728"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>VMR DirectX Video 加速支援

DirectX Video 加速是 (API) 的應用程式開發介面，以及對應的設備磁碟機介面 (適用于硬體加速數位視訊解碼處理的 DDI) ，可支援子圖片 DVD 的支援。 DirectX VA 記載于 Windows DDK 中。 [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)介面（可提供硬體裝置上的 DirectX VA 功能的使用者模式存取）記載于此 SDK 中。

VMR 支援 [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)，而其執行與舊的重迭 Mixer 相同，但有一個重要的差異。 重迭 Mixer 保證輸出會轉譯成重迭表面，而 VMR 可以傳送輸出以進行進一步的處理，例如3d 作業，或者它可能會將輸出傳送至螢幕介面，然後 blitted 至主要介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DirectX Video 加速](about-directx-video-acceleration.md)
</dt> </dl>

 

 



