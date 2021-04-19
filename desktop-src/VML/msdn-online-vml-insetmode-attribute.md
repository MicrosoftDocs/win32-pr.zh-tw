---
title: VML InsetMode 屬性
description: VML InsetMode 屬性
ms.assetid: 3cdce299-a490-43b9-93f5-09aca443e98b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f3ddee2a3c8060a9aa89dbd17bca329c1a105c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967488"
---
# <a name="vml-insetmode-attribute"></a><span data-ttu-id="ed598-103">VML InsetMode 屬性</span><span class="sxs-lookup"><span data-stu-id="ed598-103">VML InsetMode Attribute</span></span>

<span data-ttu-id="ed598-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ed598-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ed598-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ed598-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ed598-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ed598-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ed598-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ed598-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ed598-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ed598-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ed598-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ed598-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ed598-110">定義應用程式將如何允許自訂內凹值。</span><span class="sxs-lookup"><span data-stu-id="ed598-110">Defines how the application will allow custom inset values.</span></span> <span data-ttu-id="ed598-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ed598-111">Read/write.</span></span> <span data-ttu-id="ed598-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="ed598-112">**String**.</span></span>

<span data-ttu-id="ed598-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ed598-113">**Applies To**</span></span>

[<span data-ttu-id="ed598-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="ed598-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="ed598-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ed598-115">**Tag Syntax**</span></span>

<span data-ttu-id="ed598-116"><v： *element* o:insetmode = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ed598-116"><v: *element* o:insetmode=" *expression* "></span></span>

<span data-ttu-id="ed598-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="ed598-117">**Remarks**</span></span>

<span data-ttu-id="ed598-118">數值包括：</span><span class="sxs-lookup"><span data-stu-id="ed598-118">Values include:</span></span>

-   <span data-ttu-id="ed598-119">自動</span><span class="sxs-lookup"><span data-stu-id="ed598-119">auto</span></span>
-   <span data-ttu-id="ed598-120">自訂 (預設) </span><span class="sxs-lookup"><span data-stu-id="ed598-120">custom (default)</span></span>

<span data-ttu-id="ed598-121">如果值為 **auto**，則不允許自訂內凹值，而且應用程式會決定 textbox 的內部文字邊界。</span><span class="sxs-lookup"><span data-stu-id="ed598-121">If the value is **auto**, custom inset values are not allowed, and the application determines the inner text margin of a textbox.</span></span>

<span data-ttu-id="ed598-122">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="ed598-122">*Microsoft Office Extensions Attribute*</span></span>

 

 