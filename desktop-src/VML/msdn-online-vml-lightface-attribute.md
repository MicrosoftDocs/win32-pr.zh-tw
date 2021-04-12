---
title: VML LightFace 屬性
description: VML LightFace 屬性
ms.assetid: 552a4145-fb34-4a85-a32a-c9ef74f11f13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef71e5ea998233b16785e39dbe179490bc6cc32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375448"
---
# <a name="vml-lightface-attribute"></a><span data-ttu-id="eae59-103">VML LightFace 屬性</span><span class="sxs-lookup"><span data-stu-id="eae59-103">VML LightFace Attribute</span></span>

<span data-ttu-id="eae59-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="eae59-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="eae59-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="eae59-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="eae59-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="eae59-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="eae59-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="eae59-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="eae59-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="eae59-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="eae59-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="eae59-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="eae59-110">決定是否要對光源的正面臉部回應光線的變化。</span><span class="sxs-lookup"><span data-stu-id="eae59-110">Determines whether the front face of the extrusion will respond to changes in the lighting.</span></span> <span data-ttu-id="eae59-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="eae59-111">Read/write.</span></span> <span data-ttu-id="eae59-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="eae59-112">**VgTriState**.</span></span>

<span data-ttu-id="eae59-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="eae59-113">**Applies To**</span></span>

[<span data-ttu-id="eae59-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="eae59-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="eae59-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="eae59-115">**Tag Syntax**</span></span>

<span data-ttu-id="eae59-116"><o： *element* lightface = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="eae59-116"><o: *element* lightface=" *expression* "></span></span>

<span data-ttu-id="eae59-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="eae59-117">**Script Syntax**</span></span>

<span data-ttu-id="eae59-118"> lightface = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="eae59-118">*element* .lightface="*expression*"</span></span>

<span data-ttu-id="eae59-119">*運算式* =\*\* lightface</span><span class="sxs-lookup"><span data-stu-id="eae59-119">*expression*=*element*.lightface</span></span>

<span data-ttu-id="eae59-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="eae59-120">**Remarks**</span></span>

<span data-ttu-id="eae59-121">如果 **為 False**，當光源值變更時，front 臉部不會回應。</span><span class="sxs-lookup"><span data-stu-id="eae59-121">If **False**, the front face will not respond when a lighting value changes.</span></span> <span data-ttu-id="eae59-122">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="eae59-122">The default is **True**.</span></span>

<span data-ttu-id="eae59-123">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="eae59-123">*Microsoft Office Extensions Attribute*</span></span>

 

 