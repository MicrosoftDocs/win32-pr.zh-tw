---
title: VML 弧線元素
description: VML 弧線元素
ms.assetid: 46b5b78a-9a69-432b-9008-0ce7a658b9dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd35d59349e10f38495807ceb3f08dc254c117e2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316297"
---
# <a name="vml-arc-element"></a><span data-ttu-id="ba267-103">VML 弧線元素</span><span class="sxs-lookup"><span data-stu-id="ba267-103">VML Arc Element</span></span>

<span data-ttu-id="ba267-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="ba267-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ba267-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="ba267-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ba267-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="ba267-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ba267-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="ba267-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ba267-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="ba267-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ba267-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="ba267-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ba267-110">預先定義的弧線圖形。</span><span class="sxs-lookup"><span data-stu-id="ba267-110">Predefined arc shape.</span></span>

<span data-ttu-id="ba267-111">**Arc** 會使用 [>startangle](msdn-online-vml-startangle-attribute.md) 和 [endangle](msdn-online-vml-endangle-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="ba267-111">**Arc** uses the [startangle](msdn-online-vml-startangle-attribute.md) and [endangle](msdn-online-vml-endangle-attribute.md) attributes.</span></span>

<span data-ttu-id="ba267-112">以下是產生影像所需的最少程式碼。</span><span class="sxs-lookup"><span data-stu-id="ba267-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:arc
   style="top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```





 

 