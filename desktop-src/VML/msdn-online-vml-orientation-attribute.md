---
title: VML 方向屬性
description: VML 方向屬性
ms.assetid: 62298908-6e88-470d-bca2-0cfc1a38c2eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa19d8826638ef44ed99f9560e0db5dcb7ae455e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968929"
---
# <a name="vml-orientation-attribute"></a><span data-ttu-id="3c817-103">VML 方向屬性</span><span class="sxs-lookup"><span data-stu-id="3c817-103">VML Orientation Attribute</span></span>

<span data-ttu-id="3c817-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="3c817-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3c817-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="3c817-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3c817-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="3c817-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3c817-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="3c817-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3c817-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="3c817-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3c817-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="3c817-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3c817-110">指定圖形可以旋轉的向量。</span><span class="sxs-lookup"><span data-stu-id="3c817-110">Specifies the vector around which a shape can be rotated.</span></span> <span data-ttu-id="3c817-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3c817-111">Read/write.</span></span> <span data-ttu-id="3c817-112">**VgVector3D**。</span><span class="sxs-lookup"><span data-stu-id="3c817-112">**VgVector3D**.</span></span>

<span data-ttu-id="3c817-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="3c817-113">**Applies To**</span></span>

[<span data-ttu-id="3c817-114">擠壓</span><span class="sxs-lookup"><span data-stu-id="3c817-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="3c817-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="3c817-115">**Tag Syntax**</span></span>

<span data-ttu-id="3c817-116"><o： *element* 方位 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3c817-116"><o: *element* orientation=" *expression* "></span></span>

<span data-ttu-id="3c817-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="3c817-117">**Script Syntax**</span></span>

<span data-ttu-id="3c817-118">*element* 。方向 = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3c817-118">*element* .orientation="*expression*"</span></span>

<span data-ttu-id="3c817-119">*運算式* =*元素*。方向</span><span class="sxs-lookup"><span data-stu-id="3c817-119">*expression*=*element*.orientation</span></span>

<span data-ttu-id="3c817-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="3c817-120">**Remarks**</span></span>

<span data-ttu-id="3c817-121">您可以使用 [OrientationAngle](msdn-online-vml-orientationangle-attribute.md) 屬性來指定圍繞這個向量的旋轉量。</span><span class="sxs-lookup"><span data-stu-id="3c817-121">Use the [OrientationAngle](msdn-online-vml-orientationangle-attribute.md) attribute to specify the amount of rotation around this vector.</span></span> <span data-ttu-id="3c817-122">預設值為100、0、0。</span><span class="sxs-lookup"><span data-stu-id="3c817-122">Default value is 100,0,0.</span></span>

<span data-ttu-id="3c817-123">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="3c817-123">*Microsoft Office Extensions Attribute*</span></span>

 

 