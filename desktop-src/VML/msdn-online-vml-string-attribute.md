---
title: VML 字串屬性
description: VML 字串屬性
ms.assetid: 99609814-29c9-4349-9509-8c91f2aaeff5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6c172b4ca1f5049a3e89528a2333378164f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375852"
---
# <a name="vml-string-attribute"></a><span data-ttu-id="29dd2-103">VML 字串屬性</span><span class="sxs-lookup"><span data-stu-id="29dd2-103">VML String Attribute</span></span>

<span data-ttu-id="29dd2-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="29dd2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="29dd2-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="29dd2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="29dd2-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="29dd2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="29dd2-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="29dd2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="29dd2-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="29dd2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="29dd2-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="29dd2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="29dd2-110">定義文字路徑的文字。</span><span class="sxs-lookup"><span data-stu-id="29dd2-110">Defines the text of the text path.</span></span> <span data-ttu-id="29dd2-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="29dd2-111">Read/write.</span></span> <span data-ttu-id="29dd2-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="29dd2-112">**String**.</span></span>

<span data-ttu-id="29dd2-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="29dd2-113">**Applies To**</span></span>

[<span data-ttu-id="29dd2-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="29dd2-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="29dd2-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="29dd2-115">**Tag Syntax**</span></span>

<span data-ttu-id="29dd2-116"><v： *element* string = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="29dd2-116"><v: *element* string=" *expression* "></span></span>

<span data-ttu-id="29dd2-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="29dd2-117">**Script Syntax**</span></span>

<span data-ttu-id="29dd2-118">*element* = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="29dd2-118">*element* .string="*expression*"</span></span>

<span data-ttu-id="29dd2-119">*運算式* =*元素*。字串</span><span class="sxs-lookup"><span data-stu-id="29dd2-119">*expression*=*element*.string</span></span>

<span data-ttu-id="29dd2-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="29dd2-120">**Remarks**</span></span>

<span data-ttu-id="29dd2-121">您必須指派文字字串來顯示文字路徑上的文字。</span><span class="sxs-lookup"><span data-stu-id="29dd2-121">You must assign a text string to display text on a text path.</span></span>

<span data-ttu-id="29dd2-122">VML 標準屬性</span><span class="sxs-lookup"><span data-stu-id="29dd2-122">VML Standard Attribute</span></span>

<span data-ttu-id="29dd2-123">**範例**</span><span class="sxs-lookup"><span data-stu-id="29dd2-123">**Example**</span></span>

<span data-ttu-id="29dd2-124">將顯示的字串為 "VML Text"。</span><span class="sxs-lookup"><span data-stu-id="29dd2-124">The string that will be displayed is "VML Text".</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 