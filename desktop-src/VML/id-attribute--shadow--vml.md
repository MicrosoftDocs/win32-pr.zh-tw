---
title: 'ID 屬性 (Shadow)  (VML) '
description: 'ID 屬性 (Shadow)  (VML) '
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d51a5917f9ef71e3c4acea7ec1ed2e5cf90aef8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682618"
---
# <a name="id-attribute-shadowvml"></a><span data-ttu-id="83996-103">ID 屬性 (Shadow)  (VML) </span><span class="sxs-lookup"><span data-stu-id="83996-103">ID Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="83996-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="83996-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="83996-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="83996-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="83996-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="83996-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="83996-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="83996-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="83996-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="83996-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="83996-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="83996-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="83996-110">指定為陰影提供唯一識別碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="83996-110">Specifies a name that provides a unique identifier for a shadow.</span></span> <span data-ttu-id="83996-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="83996-111">Read/write.</span></span> <span data-ttu-id="83996-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="83996-112">**String**.</span></span>

<span data-ttu-id="83996-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="83996-113">**Applies To**</span></span>

[<span data-ttu-id="83996-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="83996-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="83996-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="83996-115">**Tag Syntax**</span></span>

<span data-ttu-id="83996-116"><v： *element* id = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="83996-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="83996-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="83996-117">**Script Syntax**</span></span>

<span data-ttu-id="83996-118">*元素* 。 id = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="83996-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="83996-119">*運算式* =*元素*。識別碼</span><span class="sxs-lookup"><span data-stu-id="83996-119">*expression*=*element*.id</span></span>

<span data-ttu-id="83996-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="83996-120">**Remarks**</span></span>

<span data-ttu-id="83996-121">使用 **ID** 來參考特定的陰影。</span><span class="sxs-lookup"><span data-stu-id="83996-121">Use **ID** to refer to a specific shadow.</span></span> <span data-ttu-id="83996-122">一旦您建立了陰影並為其指定識別碼之後，您就可以在想要操作陰影時使用識別碼名稱。</span><span class="sxs-lookup"><span data-stu-id="83996-122">Once you have created a shadow and given it an ID, you can use the ID name when you want to manipulate the shadow.</span></span>

<span data-ttu-id="83996-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="83996-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="83996-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="83996-124">**Example**</span></span>

<span data-ttu-id="83996-125">圖形具有稱為 "myshadow" 的陰影識別碼。</span><span class="sxs-lookup"><span data-stu-id="83996-125">The shape has a shadow ID called "myshadow".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 