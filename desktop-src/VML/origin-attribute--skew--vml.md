---
title: '原點屬性 (扭曲)  (VML) '
description: '原點屬性 (扭曲)  (VML) '
ms.assetid: 36f77073-7438-41b3-9107-95e27b01b776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf0c134ad8e7000e71a4237a6b5aac80e874c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382766"
---
# <a name="origin-attribute-skewvml"></a><span data-ttu-id="92a28-103">原點屬性 (扭曲)  (VML) </span><span class="sxs-lookup"><span data-stu-id="92a28-103">Origin Attribute (Skew)(VML)</span></span>

<span data-ttu-id="92a28-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="92a28-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="92a28-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="92a28-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="92a28-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="92a28-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="92a28-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="92a28-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="92a28-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="92a28-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="92a28-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="92a28-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="92a28-110">定義扭曲的原點。</span><span class="sxs-lookup"><span data-stu-id="92a28-110">Defines the origin of the skew.</span></span> <span data-ttu-id="92a28-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="92a28-111">Read/write.</span></span> <span data-ttu-id="92a28-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="92a28-112">**VgVector2D**.</span></span>

<span data-ttu-id="92a28-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="92a28-113">**Applies To**</span></span>

[<span data-ttu-id="92a28-114">斜</span><span class="sxs-lookup"><span data-stu-id="92a28-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="92a28-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="92a28-115">**Tag Syntax**</span></span>

<span data-ttu-id="92a28-116"><o： *element* 原點 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="92a28-116"><o: *element* origin=" *expression* "></span></span>

<span data-ttu-id="92a28-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="92a28-117">**Script Syntax**</span></span>

<span data-ttu-id="92a28-118">*element* 。源 = "*expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="92a28-118">*element* .origin="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="92a28-119">*運算式* =*元素*。來源</span><span class="sxs-lookup"><span data-stu-id="92a28-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="92a28-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="92a28-120">**Remarks**</span></span>

<span data-ttu-id="92a28-121">值通常是圖形大小的百分比，範圍從-0.5 到 + 0.5。</span><span class="sxs-lookup"><span data-stu-id="92a28-121">Values are typically a percentage of the shape's size and range from -0.5 to +0.5.</span></span> <span data-ttu-id="92a28-122">允許較大的值，將位移提供為圖形大小的倍數。</span><span class="sxs-lookup"><span data-stu-id="92a28-122">Larger values are allowed that give offsets as multiples of the shape's size.</span></span> <span data-ttu-id="92a28-123">預設值為0，0。</span><span class="sxs-lookup"><span data-stu-id="92a28-123">The default is 0,0.</span></span>

<span data-ttu-id="92a28-124">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="92a28-124">*Microsoft Office Extensions Attribute*</span></span>

 

 