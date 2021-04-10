---
title: 'Src 屬性 (ImageData)  (VML) '
description: 'Src 屬性 (ImageData)  (VML) '
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023539"
---
# <a name="src-attribute-imagedatavml"></a><span data-ttu-id="09021-103">Src 屬性 (ImageData)  (VML) </span><span class="sxs-lookup"><span data-stu-id="09021-103">Src Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="09021-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="09021-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="09021-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="09021-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="09021-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="09021-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="09021-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="09021-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="09021-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="09021-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="09021-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="09021-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="09021-110">定義影像的來源。</span><span class="sxs-lookup"><span data-stu-id="09021-110">Defines a source for the image.</span></span> <span data-ttu-id="09021-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="09021-111">Read/write.</span></span> <span data-ttu-id="09021-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="09021-112">**String**.</span></span>

<span data-ttu-id="09021-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="09021-113">**Applies To**</span></span>

[<span data-ttu-id="09021-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="09021-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="09021-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="09021-115">**Tag Syntax**</span></span>

<span data-ttu-id="09021-116"><v： *element* src = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="09021-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="09021-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="09021-117">**Script Syntax**</span></span>

<span data-ttu-id="09021-118"> src = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="09021-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="09021-119">*運算式* =*元素* src</span><span class="sxs-lookup"><span data-stu-id="09021-119">*expression*=*element*.src</span></span>

<span data-ttu-id="09021-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="09021-120">**Remarks**</span></span>

<span data-ttu-id="09021-121">此屬性一律必須與 [ImageData](msdn-online-vml-imagedata-element.md) 專案搭配使用，並指向有效的影像資料，才能顯示圖片。</span><span class="sxs-lookup"><span data-stu-id="09021-121">This attribute must always be used with the [ImageData](msdn-online-vml-imagedata-element.md) element and point to valid image data for a picture to be displayed.</span></span> <span data-ttu-id="09021-122">如果出現沒有 [HRef](https://www.bing.com/search?q=HRef) 或 [Title](title-attribute--imagedata--vml.md)的屬性，則會連結影像。</span><span class="sxs-lookup"><span data-stu-id="09021-122">If this attribute appears without [HRef](https://www.bing.com/search?q=HRef) or [Title](title-attribute--imagedata--vml.md), then the image is linked.</span></span>

<span data-ttu-id="09021-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="09021-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="09021-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="09021-124">**Example**</span></span>

<span data-ttu-id="09021-125">影像的來源是名為 "kids.jpg" 的檔案。</span><span class="sxs-lookup"><span data-stu-id="09021-125">The source of the image is a file named "kids.jpg".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 