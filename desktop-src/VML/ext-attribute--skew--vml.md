---
title: 'Ext 屬性 (扭曲)  (VML) '
description: 'Ext 屬性 (扭曲)  (VML) '
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186026"
---
# <a name="ext-attribute-skewvml"></a><span data-ttu-id="9810a-103">Ext 屬性 (扭曲)  (VML) </span><span class="sxs-lookup"><span data-stu-id="9810a-103">Ext Attribute (Skew)(VML)</span></span>

<span data-ttu-id="9810a-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="9810a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9810a-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="9810a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9810a-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="9810a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9810a-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="9810a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9810a-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="9810a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9810a-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="9810a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9810a-110">定義扭曲的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="9810a-110">Defines the way a skew is displayed.</span></span> <span data-ttu-id="9810a-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9810a-111">Read/write.</span></span> <span data-ttu-id="9810a-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="9810a-112">**String**.</span></span>

<span data-ttu-id="9810a-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="9810a-113">**Applies To**</span></span>

[<span data-ttu-id="9810a-114">斜</span><span class="sxs-lookup"><span data-stu-id="9810a-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="9810a-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="9810a-115">**Tag Syntax**</span></span>

<span data-ttu-id="9810a-116"><o： *element* v:ext = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="9810a-116"><o: *element* v:ext=" *expression* "></span></span>

<span data-ttu-id="9810a-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="9810a-117">**Script Syntax**</span></span>

<span data-ttu-id="9810a-118">*元素* 。 ext = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="9810a-118">*element* .ext="*expression*"</span></span>

<span data-ttu-id="9810a-119">*運算式* =*元素* ext</span><span class="sxs-lookup"><span data-stu-id="9810a-119">*expression*=*element*.ext</span></span>

<span data-ttu-id="9810a-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="9810a-120">**Remarks**</span></span>

<span data-ttu-id="9810a-121">這個屬性是用來告訴圖形編輯器如何處理 **扭曲** 元素。</span><span class="sxs-lookup"><span data-stu-id="9810a-121">This attribute is used to tell graphical editors how to process the **Skew** element.</span></span> <span data-ttu-id="9810a-122">數值包括：</span><span class="sxs-lookup"><span data-stu-id="9810a-122">Values include:</span></span>

-   <span data-ttu-id="9810a-123">**edit**</span><span class="sxs-lookup"><span data-stu-id="9810a-123">**edit**</span></span>
-   <span data-ttu-id="9810a-124">**view** (預設) </span><span class="sxs-lookup"><span data-stu-id="9810a-124">**view** (default)</span></span>
-   <span data-ttu-id="9810a-125">**backwardCompatible**</span><span class="sxs-lookup"><span data-stu-id="9810a-125">**backwardCompatible**</span></span>

<span data-ttu-id="9810a-126">如果延伸模組設定為 [ **編輯**]，軟體檢視器可以忽略它。</span><span class="sxs-lookup"><span data-stu-id="9810a-126">If an extension is set to **edit**, it can be ignored by a software viewer.</span></span> <span data-ttu-id="9810a-127">如果設定為 **view**，則檢視器必須改為呈現點陣圖表示。</span><span class="sxs-lookup"><span data-stu-id="9810a-127">If set to **view**, the viewer must render the bitmap representation instead.</span></span>

<span data-ttu-id="9810a-128">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="9810a-128">*Microsoft Office Extensions Attribute*</span></span>

 

 