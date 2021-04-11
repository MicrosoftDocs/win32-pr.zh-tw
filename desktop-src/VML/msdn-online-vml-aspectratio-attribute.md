---
title: VML AspectRatio 屬性
description: VML AspectRatio 屬性
ms.assetid: bc209218-9259-454e-bad2-58f67e211709
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a505b01e12d723e4c8e1ff3da3e1663bda27a45f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682611"
---
# <a name="vml-aspectratio-attribute"></a><span data-ttu-id="26309-103">VML AspectRatio 屬性</span><span class="sxs-lookup"><span data-stu-id="26309-103">VML AspectRatio Attribute</span></span>

<span data-ttu-id="26309-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="26309-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="26309-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="26309-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="26309-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="26309-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="26309-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="26309-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="26309-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="26309-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="26309-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="26309-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="26309-110">決定是否可以透過編輯器來變更圖形的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="26309-110">Determines whether the aspect ratio of a shape can be changed by an editor.</span></span> <span data-ttu-id="26309-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="26309-111">Read/write.</span></span> <span data-ttu-id="26309-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="26309-112">**VgTriState**.</span></span>

<span data-ttu-id="26309-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="26309-113">**Applies To**</span></span>

[<span data-ttu-id="26309-114">鎖定</span><span class="sxs-lookup"><span data-stu-id="26309-114">Locks</span></span>](msdn-online-vml-locks-element.md)

<span data-ttu-id="26309-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="26309-115">**Tag Syntax**</span></span>

<span data-ttu-id="26309-116"><o： *element* aspectratio = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="26309-116"><o: *element* aspectratio=" *expression* "></span></span>

<span data-ttu-id="26309-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="26309-117">**Remarks**</span></span>

<span data-ttu-id="26309-118">若 **為 True**，則表示圖形的外觀比例無法由編輯器變更。</span><span class="sxs-lookup"><span data-stu-id="26309-118">If **True**, the aspect ratio of a shape cannot be changed by an editor.</span></span> <span data-ttu-id="26309-119">這有鎖定邊角調整大小控點的效果，因此只能調整圖形的大小 isotropically。</span><span class="sxs-lookup"><span data-stu-id="26309-119">This has the effect of locking the corner resize handles so that shapes can only be resized isotropically.</span></span> <span data-ttu-id="26309-120">預設值為 **False**。</span><span class="sxs-lookup"><span data-stu-id="26309-120">The default is **False**.</span></span>

<span data-ttu-id="26309-121">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="26309-121">*Microsoft Office Extensions Attribute*</span></span>

 

 