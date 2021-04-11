---
title: VML MSO-換行距離-左方屬性
description: VML MSO-換行距離-左方屬性
ms.assetid: 25dcb5d0-a839-4a4b-8969-8e5dcf1baa47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d1e47fff0f9dceff5fd98ad526208bf487d851
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315430"
---
# <a name="vml-mso-wrap-distance-left-attribute"></a><span data-ttu-id="d920b-103">VML MSO-換行距離-左方屬性</span><span class="sxs-lookup"><span data-stu-id="d920b-103">VML MSO-Wrap-Distance-Left Attribute</span></span>

<span data-ttu-id="d920b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="d920b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d920b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="d920b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d920b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="d920b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d920b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="d920b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d920b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="d920b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d920b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="d920b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d920b-110">定義從圖形左邊到換行文字的距離。</span><span class="sxs-lookup"><span data-stu-id="d920b-110">Defines the distance from the left side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="d920b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d920b-111">Read/write.</span></span> <span data-ttu-id="d920b-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="d920b-112">**String**.</span></span>

<span data-ttu-id="d920b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="d920b-113">**Applies To**</span></span>

[<span data-ttu-id="d920b-114">形狀</span><span class="sxs-lookup"><span data-stu-id="d920b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d920b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="d920b-115">**Tag Syntax**</span></span>

<span data-ttu-id="d920b-116"><v： *element* style = "mso-wrap-left： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d920b-116"><v: *element* style="mso-wrap-distance-left: *expression* "></span></span>

<span data-ttu-id="d920b-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="d920b-117">**Remarks**</span></span>

<span data-ttu-id="d920b-118">請注意，這個屬性與 CSS **Margin** 屬性不同。</span><span class="sxs-lookup"><span data-stu-id="d920b-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="d920b-119">**邊界** 會變更圖形的原點以包含邊界區域，但 Microsoft Office 中的換行距離不會變更圖形的原點。</span><span class="sxs-lookup"><span data-stu-id="d920b-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="d920b-120">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="d920b-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="d920b-121">**範例**</span><span class="sxs-lookup"><span data-stu-id="d920b-121">**Example**</span></span>

<span data-ttu-id="d920b-122">圖形的左邊緣為10點。</span><span class="sxs-lookup"><span data-stu-id="d920b-122">The shape has a left wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-left:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 