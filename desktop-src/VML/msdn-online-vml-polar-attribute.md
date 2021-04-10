---
title: VML 極座標屬性
description: VML 極座標屬性
ms.assetid: b7ea8764-057d-4c14-81ad-77ae82b1aa31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baea7a8c044436df7e6efbf178ddb0273d7fc59d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682474"
---
# <a name="vml-polar-attribute"></a><span data-ttu-id="35598-103">VML 極座標屬性</span><span class="sxs-lookup"><span data-stu-id="35598-103">VML Polar Attribute</span></span>

<span data-ttu-id="35598-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="35598-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="35598-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="35598-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="35598-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="35598-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="35598-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="35598-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="35598-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="35598-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="35598-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="35598-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="35598-110">指定極座標圖的中心位置。</span><span class="sxs-lookup"><span data-stu-id="35598-110">Specifies the center position for polar handles.</span></span> <span data-ttu-id="35598-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35598-111">Read/write.</span></span> <span data-ttu-id="35598-112">**VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="35598-112">**VgVector2D**.</span></span>

<span data-ttu-id="35598-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="35598-113">**Applies To**</span></span>

<span data-ttu-id="35598-114">[H](msdn-online-vml-h-element.md) ([控制碼](msdn-online-vml-handles-element.md) 的子項目) </span><span class="sxs-lookup"><span data-stu-id="35598-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="35598-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="35598-115">**Tag Syntax**</span></span>

<span data-ttu-id="35598-116"><v： *element* 極座標 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="35598-116"><v: *element* polar=" *expression* "></span></span>

<span data-ttu-id="35598-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="35598-117">**Remarks**</span></span>

<span data-ttu-id="35598-118">預設值為 null 字串。</span><span class="sxs-lookup"><span data-stu-id="35598-118">The default value is a null string.</span></span> <span data-ttu-id="35598-119">如果指定了值，這表示測量是極座標的，且 [Position](position-attribute--h--vml.md) 屬性會定義控制碼的半徑和角度值，而不是 x 和 y 值。</span><span class="sxs-lookup"><span data-stu-id="35598-119">If values are specified, this indicates that the measurement is polar and that the [Position](position-attribute--h--vml.md) attribute defines radius and angle values of the handle instead of x and y values.</span></span>

<span data-ttu-id="35598-120">*VML 標準屬性*</span><span class="sxs-lookup"><span data-stu-id="35598-120">*VML Standard Attribute*</span></span>

 

 