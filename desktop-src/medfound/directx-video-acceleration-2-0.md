---
description: DirectX Video 加速2。0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: DirectX Video 加速2。0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191057"
---
# <a name="directx-video-acceleration-20"></a>DirectX Video 加速2。0

DirectX Video 加速 (DXVA) 是 API 和對應的 DDI，可使用硬體加速來加速影片編解碼器處理。 軟體編解碼器和軟體視頻處理器可以使用 DXVA，將某些需要大量 CPU 的作業卸載至 GPU。 例如，軟體解碼器可以卸載反向離散余弦轉換 (iDCT) 至 GPU。

此章節包含下列主題。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                             | 描述                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [關於 DXVA 2。0](about-dxva-2-0.md)<br/>                                                   | DXVA 2 以及其與 DXVA 1 的關聯性總覽。<br/>                                                                                                                                                        |
| [Direct3D 裝置管理員](direct3d-device-manager.md)<br/>                                 | Microsoft Direct3D 裝置管理員可讓兩個或多個物件共用相同的 Microsoft Direct3D 9 裝置。<br/>                                                                                      |
| [支援 DirectShow 中的 DXVA 2。0](supporting-dxva-2-0-in-directshow.md)<br/>             | 本主題說明如何在 DirectShow 解碼器篩選器中支援 (DXVA) 2.0 的 DirectX 影片加速。<br/>                                                                                             |
| [媒體基礎中支援 DXVA 2。0](supporting-dxva-2-0-in-media-foundation.md)<br/> | 本主題說明如何在使用 Direct3D 9 的媒體基礎轉換 (MFT) 中，支援 DXVA) 2.0 的 DirectX 影片加速 (<br/>                                                                      |
| [DXVA 影片處理](dxva-video-processing.md)<br/>                                     | DXVA 影片處理會封裝圖形硬體的功能，專門用來處理未壓縮的影片影像。 影片處理服務包含去交錯和影片混合。<br/> |
| [DXVA-HD](dxva-hd.md)<br/>                                                                 | Microsoft DirectX Video 加速 High Definition (DXVA-HD) 是用於硬體加速影片處理的 API。 <br/>                                                                                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎程式設計指南](media-foundation-programming-guide.md)
</dt> <dt>

[DXVA 1 規格](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
