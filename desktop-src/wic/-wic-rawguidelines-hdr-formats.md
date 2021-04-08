---
description: 高動態範圍像素格式
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: 高動態範圍像素格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851207"
---
# <a name="high-dynamic-range-pixel-formats"></a><span data-ttu-id="89780-103">高動態範圍像素格式</span><span class="sxs-lookup"><span data-stu-id="89780-103">High Dynamic Range Pixel Formats</span></span>

<span data-ttu-id="89780-104">編解碼器應該使用 Windows 影像處理元件 (WIC) 像素格式來保留基礎感應器資料的所有動態範圍。</span><span class="sxs-lookup"><span data-stu-id="89780-104">Codecs should use Windows Imaging Component (WIC) pixel formats that preserve all of the dynamic range of the underlying sensor data.</span></span> <span data-ttu-id="89780-105">GUID \_ WICPixelFormat48bppRGB 是可使用的一般固定點（每個通道）（可使用）。</span><span class="sxs-lookup"><span data-stu-id="89780-105">GUID\_WICPixelFormat48bppRGB is a typical fixed-point 16-bit-per-channel format that can be used.</span></span> <span data-ttu-id="89780-106">也可以使用其他更高的精確度格式。</span><span class="sxs-lookup"><span data-stu-id="89780-106">Other higher precision formats can be used also.</span></span> <span data-ttu-id="89780-107">為了啟用 Windows Presentation Foundation 圖形處理器 (GPU) 加速轉譯管線的完整支援，Microsoft 強烈鼓勵支援32位浮點像素格式。</span><span class="sxs-lookup"><span data-stu-id="89780-107">To enable full support for the Windows Presentation Foundation graphics processing unit (GPU)-accelerated rendering pipeline, Microsoft strongly encourages support for a 32-bit floating point pixel format.</span></span>

<span data-ttu-id="89780-108">高彩像素格式：在 Windows 7 中，已加入兩個新的 WIC 像素格式，以支援新的高色彩顯示格式。</span><span class="sxs-lookup"><span data-stu-id="89780-108">High Color Pixel Formats: With Windows 7, two new WIC pixel formats have been added to support the new High Color display formats.</span></span> <span data-ttu-id="89780-109">這些是： GUID \_ WICPixelFormat32bppRGBA1010102 和 guid \_ WICPixelFormat32bppRGBA1010102XR。</span><span class="sxs-lookup"><span data-stu-id="89780-109">These are: GUID\_WICPixelFormat32bppRGBA1010102 and GUID\_WICPixelFormat32bppRGBA1010102XR.</span></span>

<span data-ttu-id="89780-110">現有的 GUID WICPixelFormat64bppRGBAHalf 像素格式支援的每個 (通道16位) float High Color 格式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="89780-110">The 16 bit per channel (bpc) float High Color format is supported by the existing GUID\_WICPixelFormat64bppRGBAHalf pixel format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89780-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="89780-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="89780-112">**概念**</span><span class="sxs-lookup"><span data-stu-id="89780-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="89780-113">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="89780-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="89780-114">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="89780-114">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="89780-115">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="89780-115">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



