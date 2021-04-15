---
title: 'On 屬性 (TextPath)  (VML) '
description: 'On 屬性 (TextPath)  (VML) '
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ae791b1144046a1c29e92d11663cd15d696bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508116"
---
# <a name="on-attribute-textpathvml"></a><span data-ttu-id="e3d4f-103">On 屬性 (TextPath)  (VML) </span><span class="sxs-lookup"><span data-stu-id="e3d4f-103">On Attribute (TextPath)(VML)</span></span>

<span data-ttu-id="e3d4f-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e3d4f-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e3d4f-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e3d4f-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e3d4f-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e3d4f-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e3d4f-110">定義是否顯示文字。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-110">Defines whether the text is displayed.</span></span> <span data-ttu-id="e3d4f-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e3d4f-111">Read/write.</span></span> <span data-ttu-id="e3d4f-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-112">**VgTriState**.</span></span>

<span data-ttu-id="e3d4f-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="e3d4f-113">**Applies To**</span></span>

[<span data-ttu-id="e3d4f-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="e3d4f-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="e3d4f-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="e3d4f-115">**Tag Syntax**</span></span>

<span data-ttu-id="e3d4f-116"><v： *element* on = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e3d4f-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="e3d4f-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="e3d4f-117">**Script Syntax**</span></span>

<span data-ttu-id="e3d4f-118">*element* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e3d4f-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="e3d4f-119">*運算式* =*元素*。開啟</span><span class="sxs-lookup"><span data-stu-id="e3d4f-119">*expression*=*element*.on</span></span>

<span data-ttu-id="e3d4f-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="e3d4f-120">**Remarks**</span></span>

<span data-ttu-id="e3d4f-121">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-121">Default is **False**.</span></span> <span data-ttu-id="e3d4f-122">此值必須設定為 **True** ，才能在文字路徑上顯示文字。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-122">This value must be set to **True** to display text on a text path.</span></span>

<span data-ttu-id="e3d4f-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="e3d4f-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="e3d4f-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="e3d4f-124">**Example**</span></span>

<span data-ttu-id="e3d4f-125">文字路徑上的文字將會顯示。</span><span class="sxs-lookup"><span data-stu-id="e3d4f-125">The text on the text path will be displayed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 