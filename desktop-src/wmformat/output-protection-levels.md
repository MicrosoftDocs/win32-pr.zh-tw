---
title: 輸出保護層級
description: 輸出保護層級
ms.assetid: 89a9fc13-5ade-4a33-8304-05a2ec999fc1
keywords:
- 'Windows Media 格式 SDK、輸出保護層級 (OPL) '
- '數位版權管理 (DRM) ，輸出保護層級 (OPL) '
- 'DRM (數位版權管理) ，輸出保護層級 (OPL) '
- '輸出保護層級 (OPL) '
- 'OPL (輸出保護層級) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e5c1e08615b55aa1fb63e6d0c4e7bb82887c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931978"
---
# <a name="output-protection-levels"></a><span data-ttu-id="4d1bb-108">輸出保護層級</span><span class="sxs-lookup"><span data-stu-id="4d1bb-108">Output Protection Levels</span></span>

<span data-ttu-id="4d1bb-109">輸出保護層級 (OPLs) 是與接收數位媒體內容的各種技術相關聯的數值評等。</span><span class="sxs-lookup"><span data-stu-id="4d1bb-109">Output protection levels (OPLs) are numerical ratings associated with various technologies that receive digital media content.</span></span> <span data-ttu-id="4d1bb-110">技術支援的層級取決於它的安全程度。</span><span class="sxs-lookup"><span data-stu-id="4d1bb-110">The level a technology supports depends upon how secure it is.</span></span> <span data-ttu-id="4d1bb-111">在 Windows Media DRM 10 中引進的 OPL 系統，可讓您以比舊版更多的彈性來建立授權。</span><span class="sxs-lookup"><span data-stu-id="4d1bb-111">The OPL system, introduced in Windows Media DRM 10, enables licenses to be created with more flexibility than in previous versions.</span></span> <span data-ttu-id="4d1bb-112">您可以指定播放和複製所需的最小 OPLs。</span><span class="sxs-lookup"><span data-stu-id="4d1bb-112">You can specify minimum OPLs required for playback and for copying.</span></span> <span data-ttu-id="4d1bb-113">此外，您可以指定最小 OPL 的例外狀況，以允許未分級高的技術，或不允許 OPL 超過最小值的技術。</span><span class="sxs-lookup"><span data-stu-id="4d1bb-113">In addition, you can specify exceptions to the minimum OPL, either to allow a technology not rated high enough, or to disallow a technology with an OPL that exceeds the minimum.</span></span>

<span data-ttu-id="4d1bb-114">藉由指定使用 OPLs 的授許可權制，內容擁有者只需要使用兩個動作 (複製和播放) ，其中先前的版本會針對不同類型的裝置定義不同的動作，這些裝置可支援 (SDMI、非 SDMI 和 Red Book 音訊 CD) 進行複製。</span><span class="sxs-lookup"><span data-stu-id="4d1bb-114">By specifying restrictions to licenses using OPLs, a content owner need only use two actions (Copy and Play), where previous versions had separate actions defined for the various kinds of devices supported for copying (SDMI, non-SDMI, and Red Book audio CD).</span></span>

<span data-ttu-id="4d1bb-115">**注意** 此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="4d1bb-115">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d1bb-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d1bb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d1bb-117">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="4d1bb-117">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="4d1bb-118">**使用輸出保護層級**</span><span class="sxs-lookup"><span data-stu-id="4d1bb-118">**Working with Output Protection Levels**</span></span>](working-with-output-protection-levels.md)
</dt> </dl>

 

 




