---
title: VML 頂點屬性
description: VML 頂點屬性
ms.assetid: 3b887ecb-19e8-4ebf-9db6-bf3ed4f7d589
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a236be4b1496ceb938cc827692610a987cc2e9b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382669"
---
# <a name="vml-vertices-attribute"></a><span data-ttu-id="a203a-103">VML 頂點屬性</span><span class="sxs-lookup"><span data-stu-id="a203a-103">VML Vertices Attribute</span></span>

<span data-ttu-id="a203a-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="a203a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a203a-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="a203a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a203a-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="a203a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a203a-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="a203a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a203a-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="a203a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a203a-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="a203a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a203a-110">決定是否可以透過編輯器變更路徑的頂點。</span><span class="sxs-lookup"><span data-stu-id="a203a-110">Determines whether the vertices of a path can be changed by an editor.</span></span> <span data-ttu-id="a203a-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a203a-111">Read/write.</span></span> <span data-ttu-id="a203a-112">**VgTriState**。</span><span class="sxs-lookup"><span data-stu-id="a203a-112">**VgTriState**.</span></span>

<span data-ttu-id="a203a-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="a203a-113">**Applies To**</span></span>

[<span data-ttu-id="a203a-114">鎖定</span><span class="sxs-lookup"><span data-stu-id="a203a-114">Locks</span></span>](msdn-online-vml-locks-element.md)

<span data-ttu-id="a203a-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="a203a-115">**Tag Syntax**</span></span>

<span data-ttu-id="a203a-116"><o： *element* 頂點 = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a203a-116"><o: *element* vertices=" *expression* "></span></span>

<span data-ttu-id="a203a-117">**備註**</span><span class="sxs-lookup"><span data-stu-id="a203a-117">**Remarks**</span></span>

<span data-ttu-id="a203a-118">若 **為 True**，則會鎖定路徑頂點的編輯點。</span><span class="sxs-lookup"><span data-stu-id="a203a-118">If **True**, the edit points of the vertices of a path are locked.</span></span> <span data-ttu-id="a203a-119">Microsoft Office 的自選圖形預設值為 **True** ，否則為 **False**。</span><span class="sxs-lookup"><span data-stu-id="a203a-119">The default value is **True** for Microsoft Office AutoShapes, but otherwise is **False**.</span></span>

<span data-ttu-id="a203a-120">*Microsoft Office Extensions 屬性*</span><span class="sxs-lookup"><span data-stu-id="a203a-120">*Microsoft Office Extensions Attribute*</span></span>

 

 