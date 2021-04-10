---
title: 'Src 屬性 (筆觸)  (VML) '
description: 'Src 屬性 (筆觸)  (VML) '
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5833b24abf0f16c6e17fa3319931565ee6c232
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682418"
---
# <a name="src-attribute-strokevml"></a><span data-ttu-id="edcd7-103">Src 屬性 (筆觸)  (VML) </span><span class="sxs-lookup"><span data-stu-id="edcd7-103">Src Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="edcd7-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="edcd7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="edcd7-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="edcd7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="edcd7-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="edcd7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="edcd7-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="edcd7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="edcd7-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="edcd7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="edcd7-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="edcd7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="edcd7-110">定義要為筆觸填滿載入的來源影像。</span><span class="sxs-lookup"><span data-stu-id="edcd7-110">Defines the source image to load for a stroke fill.</span></span> <span data-ttu-id="edcd7-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="edcd7-111">Read/write.</span></span> <span data-ttu-id="edcd7-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="edcd7-112">**String**.</span></span>

<span data-ttu-id="edcd7-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="edcd7-113">**Applies To**</span></span>

[<span data-ttu-id="edcd7-114">中風</span><span class="sxs-lookup"><span data-stu-id="edcd7-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="edcd7-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="edcd7-115">**Tag Syntax**</span></span>

<span data-ttu-id="edcd7-116"><v： *element* src = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="edcd7-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="edcd7-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="edcd7-117">**Script Syntax**</span></span>

<span data-ttu-id="edcd7-118"> src = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="edcd7-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="edcd7-119">*運算式* =*元素* src</span><span class="sxs-lookup"><span data-stu-id="edcd7-119">*expression*=*element*.src</span></span>

<span data-ttu-id="edcd7-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="edcd7-120">**Remarks**</span></span>

<span data-ttu-id="edcd7-121">影像的 URL，以載入影像和模式填滿。</span><span class="sxs-lookup"><span data-stu-id="edcd7-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="edcd7-122">這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。</span><span class="sxs-lookup"><span data-stu-id="edcd7-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="edcd7-123">如果這個屬性單獨出現，亦即沒有 **HRef** 或 **標題**，則會連結影像。</span><span class="sxs-lookup"><span data-stu-id="edcd7-123">If this attribute appears alone, that is, no **HRef** or **Title**, then the image is linked.</span></span>

<span data-ttu-id="edcd7-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="edcd7-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="edcd7-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="edcd7-125">**Example**</span></span>

<span data-ttu-id="edcd7-126">使用 cylinder.gif 檔案所指定的影像來建立筆觸。</span><span class="sxs-lookup"><span data-stu-id="edcd7-126">The stroke is created with the image specified by the cylinder.gif file.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 