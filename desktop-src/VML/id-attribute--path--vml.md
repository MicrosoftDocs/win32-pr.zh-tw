---
title: 'ID 屬性 (路徑)  (VML) '
description: 'ID 屬性 (路徑)  (VML) '
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092744"
---
# <a name="id-attribute-pathvml"></a><span data-ttu-id="cc97b-103">ID 屬性 (路徑)  (VML) </span><span class="sxs-lookup"><span data-stu-id="cc97b-103">ID Attribute (Path)(VML)</span></span>

<span data-ttu-id="cc97b-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="cc97b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cc97b-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="cc97b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cc97b-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="cc97b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cc97b-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="cc97b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cc97b-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="cc97b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cc97b-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="cc97b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cc97b-110">為路徑提供唯一識別碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc97b-110">A name that provides a unique identifier for a path.</span></span> <span data-ttu-id="cc97b-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="cc97b-111">Read/write.</span></span> <span data-ttu-id="cc97b-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="cc97b-112">**String**.</span></span>

<span data-ttu-id="cc97b-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="cc97b-113">**Applies To**</span></span>

[<span data-ttu-id="cc97b-114">路徑</span><span class="sxs-lookup"><span data-stu-id="cc97b-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="cc97b-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="cc97b-115">**Tag Syntax**</span></span>

<span data-ttu-id="cc97b-116"><v： *element* id = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="cc97b-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="cc97b-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="cc97b-117">**Script Syntax**</span></span>

<span data-ttu-id="cc97b-118">*元素* 。 id = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="cc97b-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="cc97b-119">*運算式* =*元素*。識別碼</span><span class="sxs-lookup"><span data-stu-id="cc97b-119">*expression*=*element*.id</span></span>

<span data-ttu-id="cc97b-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="cc97b-120">**Remarks**</span></span>

<span data-ttu-id="cc97b-121">使用 **ID** 來參考特定路徑。</span><span class="sxs-lookup"><span data-stu-id="cc97b-121">Use **ID** to refer to a specific path.</span></span> <span data-ttu-id="cc97b-122">當您建立路徑並指定識別碼之後，您可以在想要操作路徑時使用識別碼名稱。</span><span class="sxs-lookup"><span data-stu-id="cc97b-122">Once you have created a path and given it an ID, you can use the ID name when you want to manipulate the path.</span></span>

<span data-ttu-id="cc97b-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="cc97b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="cc97b-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="cc97b-124">**Example**</span></span>

<span data-ttu-id="cc97b-125">圖形具有名為 "myPath" 的路徑識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc97b-125">The shape has a path ID called "myPath".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 