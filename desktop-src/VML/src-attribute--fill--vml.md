---
title: 'Src 屬性 (填滿)  (的 VML) '
description: 'Src 屬性 (填滿)  (的 VML) '
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463185"
---
# <a name="src-attribute-fillvml"></a><span data-ttu-id="efbe7-103">Src 屬性 (填滿)  (的 VML) </span><span class="sxs-lookup"><span data-stu-id="efbe7-103">Src Attribute (Fill)(VML)</span></span>

<span data-ttu-id="efbe7-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="efbe7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="efbe7-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="efbe7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="efbe7-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="efbe7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="efbe7-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="efbe7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="efbe7-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="efbe7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="efbe7-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="efbe7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="efbe7-110">定義要載入填滿的影像。</span><span class="sxs-lookup"><span data-stu-id="efbe7-110">Defines the image to load for a fill.</span></span> <span data-ttu-id="efbe7-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="efbe7-111">Read/write.</span></span> <span data-ttu-id="efbe7-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="efbe7-112">**String**.</span></span>

<span data-ttu-id="efbe7-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="efbe7-113">**Applies To**</span></span>

[<span data-ttu-id="efbe7-114">填滿</span><span class="sxs-lookup"><span data-stu-id="efbe7-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="efbe7-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="efbe7-115">**Tag Syntax**</span></span>

<span data-ttu-id="efbe7-116"><v： *element* src = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="efbe7-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="efbe7-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="efbe7-117">**Script Syntax**</span></span>

<span data-ttu-id="efbe7-118">*element* 。 src = "*expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="efbe7-118">*element* .src="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="efbe7-119">*運算式* =*元素* src</span><span class="sxs-lookup"><span data-stu-id="efbe7-119">*expression*=*element*.src</span></span>

<span data-ttu-id="efbe7-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="efbe7-120">**Remarks**</span></span>

<span data-ttu-id="efbe7-121">影像的 URL，以載入影像和模式填滿。</span><span class="sxs-lookup"><span data-stu-id="efbe7-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="efbe7-122">這個屬性必須一律存在，並指向有效的影像資料，圖片才會出現。</span><span class="sxs-lookup"><span data-stu-id="efbe7-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="efbe7-123">如果這個屬性單獨出現 (也就是沒有 **HRef** 或 **Title** 屬性) ，則會連結影像。</span><span class="sxs-lookup"><span data-stu-id="efbe7-123">If this attribute appears alone (that is, no **HRef** or **Title** attribute), then the image is linked.</span></span>

<span data-ttu-id="efbe7-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="efbe7-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="efbe7-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="efbe7-125">**Example**</span></span>

<span data-ttu-id="efbe7-126">使用檔案 myimage.gif 作為來源的磚影像隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="efbe7-126">A tiled image using the file myimage.gif as a source is displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 