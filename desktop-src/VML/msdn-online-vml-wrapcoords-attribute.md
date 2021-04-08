---
title: VML WrapCoords 屬性
description: VML WrapCoords 屬性
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682523"
---
# <a name="vml-wrapcoords-attribute"></a><span data-ttu-id="be0de-103">VML WrapCoords 屬性</span><span class="sxs-lookup"><span data-stu-id="be0de-103">VML WrapCoords Attribute</span></span>

<span data-ttu-id="be0de-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="be0de-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="be0de-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="be0de-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="be0de-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="be0de-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="be0de-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="be0de-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="be0de-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="be0de-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="be0de-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="be0de-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="be0de-110">定義圍繞形狀的周框多邊形。</span><span class="sxs-lookup"><span data-stu-id="be0de-110">Defines the bounding polygon that surrounds a shape.</span></span> <span data-ttu-id="be0de-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="be0de-111">Read/write.</span></span> <span data-ttu-id="be0de-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="be0de-112">**String**.</span></span>

<span data-ttu-id="be0de-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="be0de-113">**Applies To**</span></span>

[<span data-ttu-id="be0de-114">形狀</span><span class="sxs-lookup"><span data-stu-id="be0de-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="be0de-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="be0de-115">**Tag Syntax**</span></span>

<span data-ttu-id="be0de-116"><v： *element* o:wrapcoords = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="be0de-116"><v: *element* o:wrapcoords=" *expression* "></span></span>

<span data-ttu-id="be0de-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="be0de-117">**Remarks**</span></span>

<span data-ttu-id="be0de-118">描述以逗號分隔的 x 和 ycoordinates 清單;也就是「x1、y1、x2、y2、x3、y3,...」這是在文字與圖形緊密環繞時使用。</span><span class="sxs-lookup"><span data-stu-id="be0de-118">Describes a comma-delimited list of x and ycoordinates; that is, "x1,y1,x2,y2,x3,y3,..." This is used when text is tightly wrapped around a shape.</span></span> <span data-ttu-id="be0de-119">預設值為 **Null** (空) 字串，直到 **MSO 自動換行模式** 屬性設定為 [ **緊密型** ] 或 [ **到**] 為止。</span><span class="sxs-lookup"><span data-stu-id="be0de-119">The default is **NULL** (an empty string) until the **MSO-Wrap-Mode** attribute is set to **tight** or **through**.</span></span>

<span data-ttu-id="be0de-120">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="be0de-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="be0de-121">**範例**</span><span class="sxs-lookup"><span data-stu-id="be0de-121">**Example**</span></span>

<span data-ttu-id="be0de-122">圖形具有文字環繞周框方塊，其為大於路徑的5個單位。</span><span class="sxs-lookup"><span data-stu-id="be0de-122">The shape has a text wrap bounding box that is 5 units larger than the path.</span></span>


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 