---
description: 本指南包含 Microsoft Direct3D 所執行之圖形管線的描述。
ms.assetid: 54c5f8de-a976-4a82-9a23-a7f6cffef5e1
title: Direct3D 9 程式設計指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be451422cca297b08f22f1a0eee19e4a1934187
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467779"
---
# <a name="programming-guide-for-direct3d-9"></a><span data-ttu-id="8d2e3-103">Direct3D 9 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="8d2e3-103">Programming Guide for Direct3D 9</span></span>

<span data-ttu-id="8d2e3-104">本指南包含 Microsoft Direct3D 所執行之圖形管線的描述。</span><span class="sxs-lookup"><span data-stu-id="8d2e3-104">This guide contains a description of the graphics pipeline implemented by Microsoft Direct3D.</span></span> <span data-ttu-id="8d2e3-105">這是在應用程式中執行 Direct3D 圖形功能的開發人員所適用的指南。</span><span class="sxs-lookup"><span data-stu-id="8d2e3-105">It is a guide for developers who implement Direct3D graphics functionality into their applications.</span></span> <span data-ttu-id="8d2e3-106">本指南包含架構描述、功能區塊圖表，以及管線中的構成組塊，以及程式碼片段和範例應用程式的描述。</span><span class="sxs-lookup"><span data-stu-id="8d2e3-106">The guide contains architecture descriptions, functional block diagrams, and descriptions of the building blocks in the pipeline, as well as code snippets and sample applications.</span></span> <span data-ttu-id="8d2e3-107">此資訊分成下列各節：</span><span class="sxs-lookup"><span data-stu-id="8d2e3-107">The information is divided into the following sections:</span></span>

-   <span data-ttu-id="8d2e3-108">[開始使用](getting-started.md) -本節包含管線和教學課程的總覽，可協助您在幾分鐘內就能取得簡單的圖形應用程式。</span><span class="sxs-lookup"><span data-stu-id="8d2e3-108">[Getting Started](getting-started.md) - This section contains both an overview of the pipeline and tutorials that can help you get a simple graphics application running in a few minutes.</span></span>
-   <span data-ttu-id="8d2e3-109">[效果](effects.md) ：本節涵蓋的效果和效果檔案可用於建立可在各種硬體平臺上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8d2e3-109">[Effects](effects.md) - This section covers effects and effect files for building applications that can run on a variety of hardware platforms.</span></span>
-   <span data-ttu-id="8d2e3-110">[Advanced 主題](advanced-topics.md) -本節包含您可以實行的不同特殊效果類型範例。</span><span class="sxs-lookup"><span data-stu-id="8d2e3-110">[Advanced Topics](advanced-topics.md) - This section contains examples of different types of special effects you can implement.</span></span> <span data-ttu-id="8d2e3-111">環境和增加對應、消除鋸齒、頂點混色、補間、高動態範圍 (HDR) 照明和預先計算 radiance 傳輸 (PRT) 示範如何將頂尖特殊效果套用至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8d2e3-111">Topics such as environment and bump mapping, antialiasing, vertex blending, tweening, high dynamic range (HDR) lighting, and precomputed radiance transfer (PRT) show how to apply leading-edge special effects to your application.</span></span>
-   <span data-ttu-id="8d2e3-112">程式[設計秘訣](programming-tips.md)-本節包含的資訊可協助您有效率地開發 Direct3D 圖形應用程式。</span><span class="sxs-lookup"><span data-stu-id="8d2e3-112">[Programming Tips](programming-tips.md) - This section contains information to help you develop Direct3D graphics applications efficiently.</span></span>

<span data-ttu-id="8d2e3-113">如需特定 API 方法的詳細資訊，請參閱 [參考](dx9-graphics-reference.md) 頁面。</span><span class="sxs-lookup"><span data-stu-id="8d2e3-113">For more information about specific API methods, see the [Reference](dx9-graphics-reference.md) pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d2e3-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d2e3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d2e3-115">Direct3D 9 圖形</span><span class="sxs-lookup"><span data-stu-id="8d2e3-115">Direct3D 9 Graphics</span></span>](dx9-graphics.md)
</dt> </dl>

 

 



