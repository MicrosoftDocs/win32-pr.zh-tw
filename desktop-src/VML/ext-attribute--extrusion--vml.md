---
title: 'Ext 屬性 (延伸)  (VML) '
description: 'Ext 屬性 (延伸)  (VML) '
ms.assetid: 5c7b2137-ddb6-422c-a202-6de494dc993f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19721ebe03198485b7f43ff671cfd3c45b236c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375776"
---
# <a name="ext-attribute-extrusionvml"></a><span data-ttu-id="dd316-103">Ext 屬性 (延伸)  (VML) </span><span class="sxs-lookup"><span data-stu-id="dd316-103">Ext Attribute (Extrusion)(VML)</span></span>

<span data-ttu-id="dd316-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="dd316-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dd316-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="dd316-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dd316-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="dd316-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dd316-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="dd316-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dd316-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="dd316-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dd316-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="dd316-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dd316-110">定義圖形編輯器的預設延伸行為。</span><span class="sxs-lookup"><span data-stu-id="dd316-110">Defines the default extrusion behavior for graphical editors.</span></span> <span data-ttu-id="dd316-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="dd316-111">Read/write.</span></span> <span data-ttu-id="dd316-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="dd316-112">**String**.</span></span>

<span data-ttu-id="dd316-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="dd316-113">**Applies To**</span></span>

[<span data-ttu-id="dd316-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="dd316-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="dd316-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="dd316-115">**Tag Syntax**</span></span>

<span data-ttu-id="dd316-116"><o： *element* v:ext = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="dd316-116"><o: *element* v:ext=" *expression* "></span></span>

<span data-ttu-id="dd316-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="dd316-117">**Script Syntax**</span></span>

<span data-ttu-id="dd316-118">*元素* 。 ext = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="dd316-118">*element* .ext="*expression*"</span></span>

<span data-ttu-id="dd316-119">*運算式* =*元素* ext</span><span class="sxs-lookup"><span data-stu-id="dd316-119">*expression*=*element*.ext</span></span>

<span data-ttu-id="dd316-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="dd316-120">**Remarks**</span></span>

<span data-ttu-id="dd316-121">指示圖形化編輯器轉譯元素。</span><span class="sxs-lookup"><span data-stu-id="dd316-121">Instructs a graphical editor to render the element.</span></span> <span data-ttu-id="dd316-122">如果無法轉譯元素，則應該改用點陣圖表示。</span><span class="sxs-lookup"><span data-stu-id="dd316-122">If it can't render the element, the bitmap representation should be used instead.</span></span> <span data-ttu-id="dd316-123">預設值為 **view**。</span><span class="sxs-lookup"><span data-stu-id="dd316-123">The default value is **view**.</span></span>

<span data-ttu-id="dd316-124">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="dd316-124">*VML Standard Attribute*</span></span>

 

 