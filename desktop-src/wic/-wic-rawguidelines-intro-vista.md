---
description: Windows Vista 中的原始影像格式
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Windows Vista 中的原始影像格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194117"
---
# <a name="raw-image-formats-in-windows-vista"></a><span data-ttu-id="a5f2e-103">Windows Vista 中的原始影像格式</span><span class="sxs-lookup"><span data-stu-id="a5f2e-103">RAW Image Formats in Windows Vista</span></span>

<span data-ttu-id="a5f2e-104">Windows Vista Explorer、Windows Vista 影像中心、Window Live 影像中心和 Windows 7 相片檢視器全部都使用 Windows 影像處理元件 (WIC) ，因此在電腦上安裝適當的編解碼器時，支援原始的影像格式。</span><span class="sxs-lookup"><span data-stu-id="a5f2e-104">Windows Vista Explorer , Windows Vista Photo Gallery, Window Live Photo Gallery, and the Windows 7 Photo Viewer all use Windows Imaging Component (WIC) and therefore support RAW image formats when appropriate codecs are installed on the computer.</span></span>

<span data-ttu-id="a5f2e-105">因為 WIC 是可延伸的映射架構，所以任何 WIC 應用程式都可以在系統上安裝新的編解碼器時，立即取用新的映射格式。</span><span class="sxs-lookup"><span data-stu-id="a5f2e-105">Because WIC is an extensible imaging architecture, any WIC application can consume new image formats as soon as new codecs are installed on the system.</span></span> <span data-ttu-id="a5f2e-106">這讓 WIC 更適合用來做為數位攝影機所產生之原始影像格式的隨插即用解決方案。</span><span class="sxs-lookup"><span data-stu-id="a5f2e-106">This makes WIC ideal as a Plug and Play solution for the RAW image formats that digital cameras produce.</span></span> <span data-ttu-id="a5f2e-107">透過 WIC，只要有更新的編解碼器可供使用時，Windows 應用程式就能取得新相機模型的支援， (最好在新的攝影機) 。</span><span class="sxs-lookup"><span data-stu-id="a5f2e-107">Through WIC, Windows applications can gain support for new camera models whenever updated codecs are made available (ideally in-box with new cameras).</span></span> <span data-ttu-id="a5f2e-108">編解碼器作者可以藉由執行所有映射類型通用的 WIC 介面來支援這些案例，如本檔中的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="a5f2e-108">Codec authors can support these scenarios by implementing WIC interfaces that are common to all image types, as described in more detail in this document.</span></span>

<span data-ttu-id="a5f2e-109">現今，大部分的主要取用者應用程式都不會對原始影像格式有特別的認識，也不會公開使用者介面來調整原始的處理設定。</span><span class="sxs-lookup"><span data-stu-id="a5f2e-109">Today, most mainstream consumer applications have no special knowledge of RAW image formats and do not expose a user interface for adjusting RAW processing settings.</span></span>

<span data-ttu-id="a5f2e-110">不過，為了支援特殊的影像處理應用程式，原始編解碼器作者也必須執行 [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) 介面。</span><span class="sxs-lookup"><span data-stu-id="a5f2e-110">However, to support specialized imaging applications, RAW codec authors must also implement the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="a5f2e-111">此介面會公開原始影像的特殊功能，例如，可進行常見的影像調整，以及處理 (將) 原始影像開發成指定的紅色-綠色-藍色 (RGB) 色彩空間的功能。</span><span class="sxs-lookup"><span data-stu-id="a5f2e-111">This interface exposes special features for RAW images, such as the ability to make common image adjustments and to process (develop) RAW images into specified red-green-blue (RGB) color spaces.</span></span>

<span data-ttu-id="a5f2e-112">其他數個 WIC 介面對於原始編解碼器作者而言很重要。</span><span class="sxs-lookup"><span data-stu-id="a5f2e-112">Several other WIC interfaces are important for RAW codec authors to implement.</span></span> <span data-ttu-id="a5f2e-113">這些主題將在這一系列主題中更詳細地討論。</span><span class="sxs-lookup"><span data-stu-id="a5f2e-113">These are discussed in more detail in this series of topics.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5f2e-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5f2e-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a5f2e-115">**概念**</span><span class="sxs-lookup"><span data-stu-id="a5f2e-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a5f2e-116">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="a5f2e-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="a5f2e-117">相機原始影像格式的 WIC 指導方針</span><span class="sxs-lookup"><span data-stu-id="a5f2e-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="a5f2e-118">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="a5f2e-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



