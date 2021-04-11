---
description: '介紹 (適用于相機原始影像格式的 WIC 指導方針) '
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: '介紹 (適用于相機原始影像格式的 WIC 指導方針) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194116"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a><span data-ttu-id="94c9c-103">介紹 (適用于相機原始影像格式的 WIC 指導方針) </span><span class="sxs-lookup"><span data-stu-id="94c9c-103">Introduction (WIC Guidelines for Camera RAW Image Formats)</span></span>

<span data-ttu-id="94c9c-104">Windows 影像處理元件 (WIC) 提供可延伸的架構，可用於處理影像和影像中繼資料。</span><span class="sxs-lookup"><span data-stu-id="94c9c-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="94c9c-105">WIC 讓軟體和硬體廠商能夠開發編解碼器，讓自己的映射格式可以取得與原生映射格式相同的平臺支援，例如標記的影像檔案格式 (TIFF) 、聯合攝影專家群組 (JPEG) 或 HD 相片。</span><span class="sxs-lookup"><span data-stu-id="94c9c-105">WIC makes it possible for software and hardware vendors to develop codecs so that their own image formats can obtain the same platform support as native image formats such as tagged image file format (TIFF), Joint Photographic Experts Group (JPEG), or HD Photo.</span></span>

<span data-ttu-id="94c9c-106">WIC 針對所有影像處理提供單一且一致的介面集，不論影像格式為何。</span><span class="sxs-lookup"><span data-stu-id="94c9c-106">WIC provides a single, consistent set of interfaces for all image processing, regardless of image format.</span></span> <span data-ttu-id="94c9c-107">因此，任何使用 WIC 的應用程式都會在安裝編解碼器時，立即收到新映射格式的自動支援。</span><span class="sxs-lookup"><span data-stu-id="94c9c-107">Therefore, any application that uses WIC receives automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="94c9c-108">WIC 也提供可延伸的中繼資料架構，讓應用程式可以將自己的專屬中繼資料直接讀取和寫入影像檔案，因此中繼資料永遠不會遺失或與影像分開。</span><span class="sxs-lookup"><span data-stu-id="94c9c-108">WIC also provides an extensible metadata framework that makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata is never lost or separated from the image.</span></span>

<span data-ttu-id="94c9c-109">WIC 包含在 Windows Presentation Foundation (WPF) 中，並內建于 Windows Vista 和更新版本的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="94c9c-109">WIC is included with Windows Presentation Foundation (WPF) and is built into Windows Vista and later Windows versions.</span></span> <span data-ttu-id="94c9c-110">它也可作為 Windows XP 的獨立可轉散發元件。</span><span class="sxs-lookup"><span data-stu-id="94c9c-110">It is also available as a stand-alone redistributable component for Windows XP.</span></span>

<span data-ttu-id="94c9c-111">這些指導方針是設計來協助原始格式製造商開發 WIC 編解碼器。</span><span class="sxs-lookup"><span data-stu-id="94c9c-111">These guidelines are designed to help RAW format manufacturers in their development of WIC codecs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94c9c-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="94c9c-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="94c9c-113">**概念**</span><span class="sxs-lookup"><span data-stu-id="94c9c-113">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="94c9c-114">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="94c9c-114">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="94c9c-115">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="94c9c-115">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="94c9c-116">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="94c9c-116">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



