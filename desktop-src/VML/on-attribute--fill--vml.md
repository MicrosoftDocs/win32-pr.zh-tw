---
title: '在屬性 (填滿)  (的 VML) '
description: '在屬性 (填滿)  (的 VML) '
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e25e805be23b4678b1be828b711365a8624f10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106999591"
---
# <a name="on-attribute-fillvml"></a><span data-ttu-id="b89ec-103">在屬性 (填滿)  (的 VML) </span><span class="sxs-lookup"><span data-stu-id="b89ec-103">On Attribute (Fill)(VML)</span></span>

<span data-ttu-id="b89ec-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b89ec-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b89ec-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b89ec-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b89ec-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b89ec-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b89ec-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b89ec-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b89ec-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b89ec-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b89ec-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b89ec-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b89ec-110">決定是否會顯示填滿。</span><span class="sxs-lookup"><span data-stu-id="b89ec-110">Determines whether the fill will be displayed.</span></span> <span data-ttu-id="b89ec-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b89ec-111">Read/write.</span></span> <span data-ttu-id="b89ec-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="b89ec-112">**VgTriState**.</span></span>

<span data-ttu-id="b89ec-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b89ec-113">**Applies To**</span></span>

[<span data-ttu-id="b89ec-114">填滿</span><span class="sxs-lookup"><span data-stu-id="b89ec-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="b89ec-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b89ec-115">**Tag Syntax**</span></span>

<span data-ttu-id="b89ec-116"><v： *element* on = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b89ec-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="b89ec-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b89ec-117">**Script Syntax**</span></span>

<span data-ttu-id="b89ec-118">*element* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b89ec-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="b89ec-119">*運算式* =*元素*。開啟</span><span class="sxs-lookup"><span data-stu-id="b89ec-119">*expression*=*element*.on</span></span>

<span data-ttu-id="b89ec-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b89ec-120">**Remarks**</span></span>

<span data-ttu-id="b89ec-121">如果 **為 False**，則不會顯示填滿。</span><span class="sxs-lookup"><span data-stu-id="b89ec-121">If **False**, the fill is not displayed.</span></span> <span data-ttu-id="b89ec-122">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="b89ec-122">The default is **True**.</span></span>

<span data-ttu-id="b89ec-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="b89ec-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="b89ec-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="b89ec-124">**Example**</span></span>

<span data-ttu-id="b89ec-125">雖然填滿定義為紅色，但不會顯示。</span><span class="sxs-lookup"><span data-stu-id="b89ec-125">Even though the fill is defined to be red, it is not displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 