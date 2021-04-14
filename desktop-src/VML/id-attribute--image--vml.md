---
title: " (影像)  (VML) 的識別碼屬性"
description: " (影像)  (VML) 的識別碼屬性"
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ac489331699ca6fe040cddc0bebb408d524de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382778"
---
# <a name="id-attribute-imagevml"></a><span data-ttu-id="6417a-103"> (影像)  (VML) 的識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="6417a-103">ID Attribute (Image)(VML)</span></span>

<span data-ttu-id="6417a-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="6417a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6417a-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="6417a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6417a-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="6417a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6417a-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="6417a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6417a-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="6417a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6417a-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="6417a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6417a-110">定義提供映射唯一識別碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="6417a-110">Defines a name that provides a unique identifier for an image.</span></span> <span data-ttu-id="6417a-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6417a-111">Read/write.</span></span> <span data-ttu-id="6417a-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="6417a-112">**String**.</span></span>

<span data-ttu-id="6417a-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="6417a-113">**Applies To**</span></span>

[<span data-ttu-id="6417a-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="6417a-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="6417a-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="6417a-115">**Tag Syntax**</span></span>

<span data-ttu-id="6417a-116"><v： *element* id = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="6417a-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="6417a-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="6417a-117">**Script Syntax**</span></span>

<span data-ttu-id="6417a-118">*元素* 。 id = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="6417a-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="6417a-119">*運算式* =*元素*。識別碼</span><span class="sxs-lookup"><span data-stu-id="6417a-119">*expression*=*element*.id</span></span>

<span data-ttu-id="6417a-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="6417a-120">**Remarks**</span></span>

<span data-ttu-id="6417a-121">使用 **ID** 來參考特定的映射。</span><span class="sxs-lookup"><span data-stu-id="6417a-121">Use **ID** to refer to a specific image.</span></span> <span data-ttu-id="6417a-122">當您建立映射並將其命名為識別碼之後，您可以在想要操作映射時使用識別碼名稱。</span><span class="sxs-lookup"><span data-stu-id="6417a-122">Once you have created an image and given it an ID, you can use the ID name when you want to manipulate the image.</span></span>

<span data-ttu-id="6417a-123">**VML 標準屬性**</span><span class="sxs-lookup"><span data-stu-id="6417a-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="6417a-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="6417a-124">**Example**</span></span>

<span data-ttu-id="6417a-125">圖形具有稱為 "myimage" 的 **ImageData** 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6417a-125">The shape has an **ImageData** ID called "myimage".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 