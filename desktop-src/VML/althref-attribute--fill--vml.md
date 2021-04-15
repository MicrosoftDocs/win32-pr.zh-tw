---
title: 'AltHRef 屬性 (填滿)  (的 VML) '
description: 'AltHRef 屬性 (填滿)  (的 VML) '
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463309"
---
# <a name="althref-attribute-fillvml"></a><span data-ttu-id="1ef26-103">AltHRef 屬性 (填滿)  (的 VML) </span><span class="sxs-lookup"><span data-stu-id="1ef26-103">AltHRef Attribute (Fill)(VML)</span></span>

<span data-ttu-id="1ef26-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="1ef26-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1ef26-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="1ef26-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1ef26-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="1ef26-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1ef26-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="1ef26-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1ef26-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="1ef26-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1ef26-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="1ef26-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1ef26-110">定義影像的替代參考。</span><span class="sxs-lookup"><span data-stu-id="1ef26-110">Defines an alternate reference for an image.</span></span> <span data-ttu-id="1ef26-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1ef26-111">Read/write.</span></span> <span data-ttu-id="1ef26-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="1ef26-112">**String**.</span></span>

<span data-ttu-id="1ef26-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="1ef26-113">**Applies To**</span></span>

[<span data-ttu-id="1ef26-114">填滿</span><span class="sxs-lookup"><span data-stu-id="1ef26-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="1ef26-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="1ef26-115">**Tag Syntax**</span></span>

<span data-ttu-id="1ef26-116"><v： *element* o:althref = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="1ef26-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="1ef26-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="1ef26-117">**Script Syntax**</span></span>

<span data-ttu-id="1ef26-118"> althref = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="1ef26-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="1ef26-119">*運算式* =\*\* althref</span><span class="sxs-lookup"><span data-stu-id="1ef26-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="1ef26-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="1ef26-120">**Remarks**</span></span>

<span data-ttu-id="1ef26-121">支援透過 HTML roundtripping 保留 PICT 資料。</span><span class="sxs-lookup"><span data-stu-id="1ef26-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="1ef26-122">在 HTML 寫入時，如果已儲存來自 Apple Macintosh) 的檔案，則替代表示 (原始的 PICT 資料。</span><span class="sxs-lookup"><span data-stu-id="1ef26-122">On HTML write, the alternate representation (the original PICT data if the file originated from the Apple Macintosh) is saved.</span></span> <span data-ttu-id="1ef26-123">HTML 讀取時， **AltHRef** 優先于 **Src**。</span><span class="sxs-lookup"><span data-stu-id="1ef26-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="1ef26-124">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="1ef26-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="1ef26-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="1ef26-125">**Example**</span></span>

<span data-ttu-id="1ef26-126">圖形的填滿具有指向名為 myimage.gif 之檔案的 **AltHRef** 。</span><span class="sxs-lookup"><span data-stu-id="1ef26-126">The fill of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 