---
title: 'Title 屬性 (筆觸)  (VML) '
description: 'Title 屬性 (筆觸)  (VML) '
ms.assetid: 47cdec4a-9b35-47d7-a44d-e128c6c8a812
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52a5f121ff93d2fe43320dad6587dab45185713
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969118"
---
# <a name="title-attribute-strokevml"></a><span data-ttu-id="ff6a1-103">Title 屬性 (筆觸)  (VML) </span><span class="sxs-lookup"><span data-stu-id="ff6a1-103">Title Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="ff6a1-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ff6a1-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ff6a1-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ff6a1-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ff6a1-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ff6a1-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ff6a1-110">定義筆觸影像的標題。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-110">Defines the title of a stroke image.</span></span> <span data-ttu-id="ff6a1-111">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ff6a1-111">Read/write.</span></span> <span data-ttu-id="ff6a1-112">**字串**。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-112">**String**.</span></span>

<span data-ttu-id="ff6a1-113">**適用於**</span><span class="sxs-lookup"><span data-stu-id="ff6a1-113">**Applies To**</span></span>

[<span data-ttu-id="ff6a1-114">中風</span><span class="sxs-lookup"><span data-stu-id="ff6a1-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="ff6a1-115">**標記語法**</span><span class="sxs-lookup"><span data-stu-id="ff6a1-115">**Tag Syntax**</span></span>

<span data-ttu-id="ff6a1-116"><v： *element* title = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ff6a1-116"><v: *element* title=" *expression* "></span></span>

<span data-ttu-id="ff6a1-117">**指令碼語法**</span><span class="sxs-lookup"><span data-stu-id="ff6a1-117">**Script Syntax**</span></span>

<span data-ttu-id="ff6a1-118">*element* 。 title = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ff6a1-118">*element* .title="*expression*"</span></span>

<span data-ttu-id="ff6a1-119">*運算式* =*元素*。標題</span><span class="sxs-lookup"><span data-stu-id="ff6a1-119">*expression*=*element*.title</span></span>

<span data-ttu-id="ff6a1-120">**備註**</span><span class="sxs-lookup"><span data-stu-id="ff6a1-120">**Remarks**</span></span>

<span data-ttu-id="ff6a1-121">如果這個屬性具有值，則會 *內嵌* 筆觸影像。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-121">If this attribute has a value, then the stroke image is *embedded*.</span></span> <span data-ttu-id="ff6a1-122">屬性的實際值是當滑鼠指標移至影像上方時，要與圖片一起顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-122">The actual value of the attribute is the text to be displayed with the picture when the mouse pointer moves over the image.</span></span>

<span data-ttu-id="ff6a1-123">如果使用 **HRef** 標記，則會忽略 **Title** 。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-123">If the **HRef** tag is used, then **Title** is ignored.</span></span>

<span data-ttu-id="ff6a1-124">Microsoft Office 會使用這個屬性，但 Microsoft Internet Explorer 不會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="ff6a1-124">This attribute is used by Microsoft Office but is not used by Microsoft Internet Explorer.</span></span>

<span data-ttu-id="ff6a1-125">**Microsoft Office Extensions 屬性**</span><span class="sxs-lookup"><span data-stu-id="ff6a1-125">**Microsoft Office Extensions Attribute**</span></span>

 

 