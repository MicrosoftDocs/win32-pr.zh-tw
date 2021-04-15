---
title: 關於影片壓縮管理員
description: 關於影片壓縮管理員
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- 'Windows 多媒體、視訊壓縮管理員 (BC-VCM-LVM-HYPERV) '
- '多媒體、視訊壓縮管理員 (BC-VCM-LVM-HYPERV) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463060"
---
# <a name="about-the-video-compression-manager"></a><span data-ttu-id="3128d-105">關於影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="3128d-105">About the Video Compression Manager</span></span>

<span data-ttu-id="3128d-106">通常，可安裝的壓縮機會使用儲存在音訊中的影片影像資料（ (AVI) 檔案的影片）來運作。</span><span class="sxs-lookup"><span data-stu-id="3128d-106">Typically, installable compressors operate with video-image data stored in audio-video interleaved (AVI) files.</span></span> <span data-ttu-id="3128d-107">本總覽說明用來透過 BC-VCM-LVM-HYPERV 存取可安裝壓縮機的程式設計技術，並涵蓋下列主題：</span><span class="sxs-lookup"><span data-stu-id="3128d-107">This overview explains the programming techniques used to access installable compressors through VCM and covers the following topics:</span></span>

-   <span data-ttu-id="3128d-108">適用于 Windows 架構的 BC-VCM-LVM-HYPERV 和影片</span><span class="sxs-lookup"><span data-stu-id="3128d-108">VCM and the Video for Windows architecture</span></span>
-   <span data-ttu-id="3128d-109">從應用程式壓縮和解壓縮映射資料</span><span class="sxs-lookup"><span data-stu-id="3128d-109">Compressing and decompressing image data from your application</span></span>
-   <span data-ttu-id="3128d-110">使用 BC-VCM-LVM-HYPERV 轉譯器從您的應用程式中繪製資料</span><span class="sxs-lookup"><span data-stu-id="3128d-110">Using VCM renderers to draw data from your application</span></span>
-   <span data-ttu-id="3128d-111">BC-VCM-LVM-HYPERV 函式和結構</span><span class="sxs-lookup"><span data-stu-id="3128d-111">VCM functions and structures</span></span>

<span data-ttu-id="3128d-112">閱讀此總覽之前，您應該先熟悉 Microsoft Win32 圖形服務。</span><span class="sxs-lookup"><span data-stu-id="3128d-112">Before you read this overview, you should be familiar with the Microsoft Win32 graphic services.</span></span> <span data-ttu-id="3128d-113">尤其是 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 和 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)等點陣圖和點陣圖相關結構會由 bc-vcm-lvm-hyperv 廣泛使用。</span><span class="sxs-lookup"><span data-stu-id="3128d-113">In particular, bitmaps and bitmap-related structures, such as [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) and [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), are used extensively by VCM.</span></span> <span data-ttu-id="3128d-114">如需 **BITMAPINFO** 和 **BITMAPINFOHEADER** 結構的詳細資訊，請參閱 [點陣圖](/previous-versions//ms532349(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3128d-114">For additional information about the **BITMAPINFO** and **BITMAPINFOHEADER** structures, see [Bitmaps](/previous-versions//ms532349(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="3128d-115">音訊壓縮管理員 (的) 提供音訊壓縮和解壓縮驅動程式的系統層級支援。</span><span class="sxs-lookup"><span data-stu-id="3128d-115">The audio compression manager (ACM) provides system-level support for audio compression and decompression drivers.</span></span> <span data-ttu-id="3128d-116">如需音訊壓縮服務的說明，請參閱 [音訊壓縮管理員](audio-compression-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="3128d-116">For a description of the audio compression services, see [Audio Compression Manager](audio-compression-manager.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3128d-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="3128d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3128d-118">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="3128d-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 