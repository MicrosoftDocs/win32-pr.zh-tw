---
title: 'Offset 屬性 (扭曲)  (VML) '
description: 'Offset 屬性 (扭曲)  (VML) '
ms.assetid: 3d4b08c5-e29b-4ace-9c3e-75598068ff18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6dbabad6429ad82d4a5aa5cb9187fb1326d4900
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375437"
---
# <a name="offset-attribute-skewvml"></a><span data-ttu-id="229b9-103">Offset 屬性 (扭曲)  (VML) </span><span class="sxs-lookup"><span data-stu-id="229b9-103">Offset Attribute (Skew)(VML)</span></span>

<span data-ttu-id="229b9-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="229b9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="229b9-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="229b9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="229b9-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="229b9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="229b9-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="229b9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="229b9-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="229b9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="229b9-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="229b9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="229b9-110">定義扭曲的位移。</span><span class="sxs-lookup"><span data-stu-id="229b9-110">Defines the offset of the skew.</span></span> <span data-ttu-id="229b9-111">讀取/寫入 **VgVector2D**。</span><span class="sxs-lookup"><span data-stu-id="229b9-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="229b9-112">**適用於**</span><span class="sxs-lookup"><span data-stu-id="229b9-112">**Applies To**</span></span>

[<span data-ttu-id="229b9-113">斜</span><span class="sxs-lookup"><span data-stu-id="229b9-113">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="229b9-114">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="229b9-114">**Tag Syntax**</span></span>

<span data-ttu-id="229b9-115"><o： *element* offset = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="229b9-115"><o: *element* offset=" *expression* "></span></span>

<span data-ttu-id="229b9-116">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="229b9-116">**Script Syntax**</span></span>

<span data-ttu-id="229b9-117">*element* 。 offset = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="229b9-117">*element* .offset="*expression*"</span></span>

<span data-ttu-id="229b9-118">*運算式* =*element*。 offset</span><span class="sxs-lookup"><span data-stu-id="229b9-118">*expression*=*element*.offset</span></span>

<span data-ttu-id="229b9-119">**備註**</span><span class="sxs-lookup"><span data-stu-id="229b9-119">**Remarks**</span></span>

<span data-ttu-id="229b9-120">判斷圖形原始位置的 x 和 y 位移量。</span><span class="sxs-lookup"><span data-stu-id="229b9-120">Determines the amount of x and y offset from the shape's original location.</span></span> <span data-ttu-id="229b9-121">值的定義是以絕對測量或圖形的小數值來定義 (範圍從-0.5 到 + 0.5) 。</span><span class="sxs-lookup"><span data-stu-id="229b9-121">Values are defined in absolute measurement or fractional values of a shape (ranging from -0.5 to +0.5).</span></span> <span data-ttu-id="229b9-122">預設值為0，0。</span><span class="sxs-lookup"><span data-stu-id="229b9-122">Default is 0,0.</span></span>

<span data-ttu-id="229b9-123">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="229b9-123">*Microsoft Office Extensions Attribute*</span></span>

 

 