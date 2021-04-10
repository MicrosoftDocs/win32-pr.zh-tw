---
title: 'ID 屬性 (VMLFrame)  (VML) '
description: 'ID 屬性 (VMLFrame)  (VML) '
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023690"
---
# <a name="id-attribute-vmlframevml"></a><span data-ttu-id="53d55-103">ID 屬性 (VMLFrame)  (VML) </span><span class="sxs-lookup"><span data-stu-id="53d55-103">ID Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="53d55-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="53d55-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="53d55-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="53d55-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="53d55-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="53d55-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="53d55-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="53d55-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="53d55-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="53d55-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="53d55-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="53d55-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="53d55-110">定義框架的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="53d55-110">Defines a unique identifier for the frame.</span></span> <span data-ttu-id="53d55-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="53d55-111">Read/write.</span></span> <span data-ttu-id="53d55-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="53d55-112">**String**.</span></span>

<span data-ttu-id="53d55-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="53d55-113">**Applies To**</span></span>

[<span data-ttu-id="53d55-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="53d55-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="53d55-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="53d55-115">**Tag Syntax**</span></span>

<span data-ttu-id="53d55-116"><v： *element* ID = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="53d55-116"><v: *element* ID=" *expression* "></span></span>

<span data-ttu-id="53d55-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="53d55-117">**Script Syntax**</span></span>

<span data-ttu-id="53d55-118">*元素* 。 ID = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="53d55-118">*element* .ID="*expression*"</span></span>

<span data-ttu-id="53d55-119">*運算式* =*元素*。識別碼</span><span class="sxs-lookup"><span data-stu-id="53d55-119">*expression*=*element*.ID</span></span>

<span data-ttu-id="53d55-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="53d55-120">**Remarks**</span></span>

<span data-ttu-id="53d55-121">使用 **ID** 參考框架。</span><span class="sxs-lookup"><span data-stu-id="53d55-121">Use **ID** to reference a frame.</span></span> <span data-ttu-id="53d55-122">例如，您可以藉由變更 **識別碼** 所參考的框架位置，在頁面上移動框架。</span><span class="sxs-lookup"><span data-stu-id="53d55-122">For example, you can move the frame around on the page by changing the frame position referenced by the **ID**.</span></span>

<span data-ttu-id="53d55-123">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="53d55-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="53d55-124">**範例**</span><span class="sxs-lookup"><span data-stu-id="53d55-124">**Example**</span></span>

<span data-ttu-id="53d55-125">框架的 **識別碼** 是 "frame01"。</span><span class="sxs-lookup"><span data-stu-id="53d55-125">The **ID** of the frame is "frame01".</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 