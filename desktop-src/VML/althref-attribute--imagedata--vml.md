---
title: 'AltHRef 屬性 (ImageData)  (VML) '
description: 'AltHRef 屬性 (ImageData)  (VML) '
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023662"
---
# <a name="althref-attribute-imagedatavml"></a><span data-ttu-id="d1a4e-103">AltHRef 屬性 (ImageData)  (VML) </span><span class="sxs-lookup"><span data-stu-id="d1a4e-103">AltHRef Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="d1a4e-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d1a4e-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d1a4e-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d1a4e-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d1a4e-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d1a4e-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d1a4e-110">指定影像的替代參考。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="d1a4e-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1a4e-111">Read/write.</span></span> <span data-ttu-id="d1a4e-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-112">**String**.</span></span>

<span data-ttu-id="d1a4e-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="d1a4e-113">**Applies To**</span></span>

[<span data-ttu-id="d1a4e-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="d1a4e-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="d1a4e-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="d1a4e-115">**Tag Syntax**</span></span>

<span data-ttu-id="d1a4e-116"><v： *element* o:althref = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d1a4e-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="d1a4e-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="d1a4e-117">**Script Syntax**</span></span>

<span data-ttu-id="d1a4e-118"> althref = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d1a4e-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="d1a4e-119">*運算式* =\*\* althref</span><span class="sxs-lookup"><span data-stu-id="d1a4e-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="d1a4e-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="d1a4e-120">**Remarks**</span></span>

<span data-ttu-id="d1a4e-121">支援透過 HTML roundtripping 保留 PICT 資料。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="d1a4e-122">在 HTML 寫入時，如果儲存來自 Macintosh) 的檔案，替代表示 (也就是原始的 PICT 資料。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-122">On HTML write, the alternate representation (that is, the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="d1a4e-123">HTML 讀取時， **AltHRef** 優先于 **Src**。</span><span class="sxs-lookup"><span data-stu-id="d1a4e-123">On an HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="d1a4e-124">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="d1a4e-124">*Microsoft Office Extensions Attribute*</span></span>

 

 