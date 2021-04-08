---
title: VML 方向屬性
description: VML 方向屬性
ms.assetid: bf6e0169-f0d4-4dfb-b59e-b5601049fd7a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a5bd45d4baaed100537207a02fc4308b964dfa2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682740"
---
# <a name="vml-direction-attribute"></a><span data-ttu-id="7fad7-103">VML 方向屬性</span><span class="sxs-lookup"><span data-stu-id="7fad7-103">VML Direction Attribute</span></span>

<span data-ttu-id="7fad7-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="7fad7-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7fad7-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="7fad7-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7fad7-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="7fad7-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7fad7-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="7fad7-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7fad7-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="7fad7-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7fad7-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="7fad7-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7fad7-110">定義文字方塊中文字的方向。</span><span class="sxs-lookup"><span data-stu-id="7fad7-110">Defines the direction of the text in the textbox.</span></span> <span data-ttu-id="7fad7-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="7fad7-111">Read/write.</span></span> <span data-ttu-id="7fad7-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="7fad7-112">**String**.</span></span>

<span data-ttu-id="7fad7-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="7fad7-113">**Applies To**</span></span>

[<span data-ttu-id="7fad7-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="7fad7-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="7fad7-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="7fad7-115">**Tag Syntax**</span></span>

<span data-ttu-id="7fad7-116"><v： *element* style = "direction： *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7fad7-116"><v: *element* style="direction: *expression* "></span></span>

<span data-ttu-id="7fad7-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="7fad7-117">**Remarks**</span></span>

<span data-ttu-id="7fad7-118">數值包括：</span><span class="sxs-lookup"><span data-stu-id="7fad7-118">Values include:</span></span>



| <span data-ttu-id="7fad7-119">值</span><span class="sxs-lookup"><span data-stu-id="7fad7-119">Value</span></span>   | <span data-ttu-id="7fad7-120">描述</span><span class="sxs-lookup"><span data-stu-id="7fad7-120">Description</span></span>                                                                                |
|---------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fad7-121">局部</span><span class="sxs-lookup"><span data-stu-id="7fad7-121">ltr</span></span>     | <span data-ttu-id="7fad7-122">文字會從左至右顯示。</span><span class="sxs-lookup"><span data-stu-id="7fad7-122">Text is displayed left-to-right.</span></span> <span data-ttu-id="7fad7-123">預設值。</span><span class="sxs-lookup"><span data-stu-id="7fad7-123">Default.</span></span>                                                  |
| <span data-ttu-id="7fad7-124">Rtl</span><span class="sxs-lookup"><span data-stu-id="7fad7-124">rtl</span></span>     | <span data-ttu-id="7fad7-125">文字由右至左顯示。</span><span class="sxs-lookup"><span data-stu-id="7fad7-125">Text is displayed right-to-left.</span></span>                                                           |
| <span data-ttu-id="7fad7-126">內容</span><span class="sxs-lookup"><span data-stu-id="7fad7-126">context</span></span> | <span data-ttu-id="7fad7-127">指出將以 "coNtext" 值寫出 **MSO 方向的 Alt** 標記。</span><span class="sxs-lookup"><span data-stu-id="7fad7-127">Indicates that the **MSO-Direction-Alt** tag will be written out with the value "context".</span></span> |



 

<span data-ttu-id="7fad7-128">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="7fad7-128">*Microsoft Office Extensions Attribute*</span></span>

 

 