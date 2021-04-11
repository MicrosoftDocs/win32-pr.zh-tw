---
title: VML ShadowOK 屬性
description: VML ShadowOK 屬性
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9e6b4ca6b98ce66208e906c45fd560324121e8a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023509"
---
# <a name="vml-shadowok-attribute"></a><span data-ttu-id="ec85d-103">VML ShadowOK 屬性</span><span class="sxs-lookup"><span data-stu-id="ec85d-103">VML ShadowOK Attribute</span></span>

<span data-ttu-id="ec85d-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ec85d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ec85d-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ec85d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ec85d-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ec85d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ec85d-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ec85d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ec85d-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ec85d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ec85d-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ec85d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ec85d-110">決定是否會顯示陰影。</span><span class="sxs-lookup"><span data-stu-id="ec85d-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="ec85d-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ec85d-111">Read/write.</span></span> <span data-ttu-id="ec85d-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="ec85d-112">**VgTriState**.</span></span>

<span data-ttu-id="ec85d-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ec85d-113">**Applies To**</span></span>

[<span data-ttu-id="ec85d-114">路徑</span><span class="sxs-lookup"><span data-stu-id="ec85d-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="ec85d-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ec85d-115">**Tag Syntax**</span></span>

<span data-ttu-id="ec85d-116"><v： *element* shadowok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ec85d-116"><v: *element* shadowok=" *expression* "></span></span>

<span data-ttu-id="ec85d-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="ec85d-117">**Script Syntax**</span></span>

<span data-ttu-id="ec85d-118"> shadowok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ec85d-118">*element* .shadowok="*expression*"</span></span>

<span data-ttu-id="ec85d-119">*運算式* =\*\* shadowok</span><span class="sxs-lookup"><span data-stu-id="ec85d-119">*expression*=*element*.shadowok</span></span>

<span data-ttu-id="ec85d-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="ec85d-120">**Remarks**</span></span>

<span data-ttu-id="ec85d-121">如果 **為 False**，則路徑不能有陰影。</span><span class="sxs-lookup"><span data-stu-id="ec85d-121">If **False**, the path cannot have a shadow.</span></span> <span data-ttu-id="ec85d-122">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="ec85d-122">The default is **True**.</span></span> <span data-ttu-id="ec85d-123">這個屬性會覆寫父元素或 **陰影** 專案中的所有其他陰影屬性。</span><span class="sxs-lookup"><span data-stu-id="ec85d-123">This attribute overrides all other shadow attributes in the parent or **Shadow** element.</span></span>

<span data-ttu-id="ec85d-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="ec85d-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="ec85d-125">**範例**</span><span class="sxs-lookup"><span data-stu-id="ec85d-125">**Example**</span></span>

<span data-ttu-id="ec85d-126">圖形不會有陰影。</span><span class="sxs-lookup"><span data-stu-id="ec85d-126">The shape will not have a shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 