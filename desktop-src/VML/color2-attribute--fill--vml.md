---
title: 'Color2 屬性 (填滿)  (的 VML) '
description: 'Color2 屬性 (填滿)  (的 VML) '
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965248"
---
# <a name="color2-attribute-fillvml"></a><span data-ttu-id="8240c-103">Color2 屬性 (填滿)  (的 VML) </span><span class="sxs-lookup"><span data-stu-id="8240c-103">Color2 Attribute (Fill)(VML)</span></span>

<span data-ttu-id="8240c-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="8240c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8240c-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="8240c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8240c-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="8240c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8240c-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="8240c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8240c-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="8240c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8240c-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="8240c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8240c-110">定義填滿的第二個色彩。</span><span class="sxs-lookup"><span data-stu-id="8240c-110">Defines a second color for fills.</span></span> <span data-ttu-id="8240c-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="8240c-111">Read/write.</span></span> <span data-ttu-id="8240c-112">[VgColor](msdn-online-vml-ivgcolor.md) 。</span><span class="sxs-lookup"><span data-stu-id="8240c-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="8240c-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="8240c-113">**Applies To**</span></span>

[<span data-ttu-id="8240c-114">填滿</span><span class="sxs-lookup"><span data-stu-id="8240c-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="8240c-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="8240c-115">**Tag Syntax**</span></span>

<span data-ttu-id="8240c-116"><v： *element* color2 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="8240c-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="8240c-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="8240c-117">**Script Syntax**</span></span>

<span data-ttu-id="8240c-118"> color2 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="8240c-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="8240c-119">*運算式* =\*\* color2</span><span class="sxs-lookup"><span data-stu-id="8240c-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="8240c-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="8240c-120">**Remarks**</span></span>

<span data-ttu-id="8240c-121">當填滿型別是模式或漸層時，就會使用第二個色彩。</span><span class="sxs-lookup"><span data-stu-id="8240c-121">A second color is used when a fill type is a pattern or a gradient.</span></span> <span data-ttu-id="8240c-122">預設值為 **白色**。</span><span class="sxs-lookup"><span data-stu-id="8240c-122">The default value is **White**.</span></span>

<span data-ttu-id="8240c-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="8240c-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="8240c-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="8240c-124">**Example**</span></span>

<span data-ttu-id="8240c-125">圖形的填滿型別是一種模式，其前景填滿是由來源影像所定義，但透明背景則是以第二種色彩來定義。</span><span class="sxs-lookup"><span data-stu-id="8240c-125">The shape's fill type is a pattern where the foreground fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 