---
title: VML TableLimits 屬性
description: VML TableLimits 屬性
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682427"
---
# <a name="vml-tablelimits-attribute"></a><span data-ttu-id="fbf76-103">VML TableLimits 屬性</span><span class="sxs-lookup"><span data-stu-id="fbf76-103">VML TableLimits Attribute</span></span>

<span data-ttu-id="fbf76-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="fbf76-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fbf76-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="fbf76-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fbf76-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="fbf76-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fbf76-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="fbf76-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fbf76-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="fbf76-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fbf76-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="fbf76-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fbf76-110">資料表中每個資料列的最小高度值清單。</span><span class="sxs-lookup"><span data-stu-id="fbf76-110">List of minimum height values for each row in a table.</span></span> <span data-ttu-id="fbf76-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="fbf76-111">Read/write.</span></span> <span data-ttu-id="fbf76-112">**VgLengthArray**。</span><span class="sxs-lookup"><span data-stu-id="fbf76-112">**VgLengthArray**.</span></span>

<span data-ttu-id="fbf76-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="fbf76-113">**Applies To**</span></span>

[<span data-ttu-id="fbf76-114">形狀</span><span class="sxs-lookup"><span data-stu-id="fbf76-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="fbf76-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="fbf76-115">**Tag Syntax**</span></span>

<span data-ttu-id="fbf76-116"><v： *element* o:tablelimits = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="fbf76-116"><v: *element* o:tablelimits=" *expression* "></span></span>

<span data-ttu-id="fbf76-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="fbf76-117">**Remarks**</span></span>

<span data-ttu-id="fbf76-118">由 Microsoft PowerPoint 用於原生資料表。</span><span class="sxs-lookup"><span data-stu-id="fbf76-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="fbf76-119">預設值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fbf76-119">Default value is **Null**.</span></span>

<span data-ttu-id="fbf76-120">雖然此值是儲存在圖形中，但此屬性只有在資料表是由群組的圖形組成時才有用。</span><span class="sxs-lookup"><span data-stu-id="fbf76-120">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.</span></span> <span data-ttu-id="fbf76-121">將文字加入至資料表資料格時，資料列高度可能會增加。</span><span class="sxs-lookup"><span data-stu-id="fbf76-121">When text is added to table cells, the row height may increase.</span></span> <span data-ttu-id="fbf76-122">**TableLimits** 屬性會儲存原始資料列的高度，因此，如果刪除文字，資料列高度將不會低於原始值。</span><span class="sxs-lookup"><span data-stu-id="fbf76-122">The **TableLimits** attribute stores the original row height so that if text is deleted, the row height will not fall below the original value.</span></span>

<span data-ttu-id="fbf76-123">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="fbf76-123">*Microsoft Office Extensions Attribute*</span></span>

 

 