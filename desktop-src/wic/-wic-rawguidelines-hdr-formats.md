---
description: 高動態範圍像素格式
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: 高動態範圍像素格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a544d2331cc32943e3bc74400e1751111aac69e0a1448103e7651cb51da9353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086911"
---
# <a name="high-dynamic-range-pixel-formats"></a>高動態範圍像素格式

編解碼器應該使用 Windows 影像處理元件 (WIC) 像素格式來保留基礎感應器資料的所有動態範圍。 GUID \_ WICPixelFormat48bppRGB 是可使用的一般固定點（每個通道）（可使用）。 也可以使用其他更高的精確度格式。 為了啟用 Windows Presentation Foundation 圖形處理器 (GPU) 加速轉譯管線的完整支援，Microsoft 強烈鼓勵支援32位浮點像素格式。

高彩像素格式：在 Windows 7 中，已加入兩個新的 WIC 像素格式，以支援新的高色彩顯示格式。 這些是： GUID \_ WICPixelFormat32bppRGBA1010102 和 guid \_ WICPixelFormat32bppRGBA1010102XR。

現有的 GUID WICPixelFormat64bppRGBAHalf 像素格式支援的每個 (通道16位) float High Color 格式 \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



