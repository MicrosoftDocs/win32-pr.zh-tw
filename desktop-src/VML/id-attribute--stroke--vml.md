---
title: 'ID 屬性 (筆觸)  (VML) '
description: 'ID 屬性 (筆觸)  (VML) '
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efc9cfda1b7ddb359812d9ad28b37b851315da8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682617"
---
# <a name="id-attribute-strokevml"></a><span data-ttu-id="b39b0-103">ID 屬性 (筆觸)  (VML) </span><span class="sxs-lookup"><span data-stu-id="b39b0-103">ID Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="b39b0-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="b39b0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b39b0-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="b39b0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b39b0-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="b39b0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b39b0-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="b39b0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b39b0-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="b39b0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b39b0-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="b39b0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b39b0-110">為筆觸提供唯一識別碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="b39b0-110">A name that provides a unique identifier for a stroke.</span></span> <span data-ttu-id="b39b0-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b39b0-111">Read/write.</span></span> <span data-ttu-id="b39b0-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="b39b0-112">**String**.</span></span>

<span data-ttu-id="b39b0-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="b39b0-113">**Applies To**</span></span>

[<span data-ttu-id="b39b0-114">中風</span><span class="sxs-lookup"><span data-stu-id="b39b0-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="b39b0-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="b39b0-115">**Tag Syntax**</span></span>

<span data-ttu-id="b39b0-116"><v： *element* id = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b39b0-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="b39b0-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="b39b0-117">**Script Syntax**</span></span>

<span data-ttu-id="b39b0-118">*元素* 。 id = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b39b0-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="b39b0-119">*運算式* =*元素*。識別碼</span><span class="sxs-lookup"><span data-stu-id="b39b0-119">*expression*=*element*.id</span></span>

<span data-ttu-id="b39b0-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="b39b0-120">**Remarks**</span></span>

<span data-ttu-id="b39b0-121">使用 **ID** 來參考特定筆劃。</span><span class="sxs-lookup"><span data-stu-id="b39b0-121">Use **ID** to refer to a specific stroke.</span></span> <span data-ttu-id="b39b0-122">當您建立筆劃並將其指定為識別碼之後，您可以在想要操作筆劃時使用識別碼名稱。</span><span class="sxs-lookup"><span data-stu-id="b39b0-122">Once you have created a stroke and given it an ID, you can use the ID name when you want to manipulate the stroke.</span></span>

<span data-ttu-id="b39b0-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="b39b0-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="b39b0-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="b39b0-124">**Example**</span></span>

<span data-ttu-id="b39b0-125">圖形具有稱為 "mystroke" 的筆觸識別碼。</span><span class="sxs-lookup"><span data-stu-id="b39b0-125">The shape has a stroke ID called "mystroke".</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 