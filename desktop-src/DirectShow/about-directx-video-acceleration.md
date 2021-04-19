---
description: 關於 DirectX Video 加速
ms.assetid: 50f402e5-7e85-4e80-ad72-9c3887efcd10
title: 關於 DirectX Video 加速
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051178549e59a8b85995b697d2d9788a40337eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970703"
---
# <a name="about-directx-video-acceleration"></a><span data-ttu-id="a3426-103">關於 DirectX Video 加速</span><span class="sxs-lookup"><span data-stu-id="a3426-103">About DirectX Video Acceleration</span></span>

<span data-ttu-id="a3426-104">DirectX VA 說明 (API) 的應用程式開發介面，以及對應的設備磁碟機介面 (適用于硬體加速數位視訊解碼處理的 DDI) ，可支援子圖片 DVD 的支援。</span><span class="sxs-lookup"><span data-stu-id="a3426-104">DirectX VA describes an Application Programming Interface (API) and a corresponding Device Driver Interface (DDI) for hardware acceleration of digital video decoding processing, with support of alpha blending for such purposes as DVD subpicture support.</span></span> <span data-ttu-id="a3426-105">它提供的介面定義著重于支援 MPEG-2 「主要設定檔」影片 (正式的 262 \| ISO/IEC 13818-2) ，但也可支援其他重要的視頻編碼器 (例如，Itu-t 建議 H. 263 和 .h 261，以及 mpeg-2 和 mpeg 4) 。</span><span class="sxs-lookup"><span data-stu-id="a3426-105">It provides an interface definition focused on support of MPEG-2 "main profile" video (formally ITU-T H.262 \| ISO/IEC 13818-2), but is also intended to support other key video codecs (for example, ITU-T Recommendations H.263 and H.261, and MPEG-1 and MPEG-4).</span></span> <span data-ttu-id="a3426-106">DirectX VA 也會指定設備磁碟機如何執行消除交錯和畫面播放速率轉換作業。</span><span class="sxs-lookup"><span data-stu-id="a3426-106">DirectX VA also specifies how device drivers can implement de-interlacing and frame rate conversion operations.</span></span>

> [!Note]  
> <span data-ttu-id="a3426-107">DirectX VA 規格現在位於 Microsoft Platform DDK 中。</span><span class="sxs-lookup"><span data-stu-id="a3426-107">The DirectX VA specification is now located in the Microsoft Platform DDK.</span></span> <span data-ttu-id="a3426-108">軟體解碼器和設備磁碟機的開發人員應該參考該規格。</span><span class="sxs-lookup"><span data-stu-id="a3426-108">Developers of software decoders as well as device drivers should refer to that specification.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a3426-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3426-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3426-110">解碼器介面和規格</span><span class="sxs-lookup"><span data-stu-id="a3426-110">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



