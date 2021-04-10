---
title: VML 曲線元素
description: VML 曲線元素
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b9e04086652bf9dde7d7e7f5ebdea0992f774c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186008"
---
# <a name="vml-curve-element"></a><span data-ttu-id="00673-103">VML 曲線元素</span><span class="sxs-lookup"><span data-stu-id="00673-103">VML Curve Element</span></span>

<span data-ttu-id="00673-104">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="00673-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="00673-105">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="00673-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="00673-106">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="00673-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="00673-107">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="00673-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="00673-108">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="00673-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="00673-109">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="00673-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="00673-110">預先定義的曲線圖形。</span><span class="sxs-lookup"><span data-stu-id="00673-110">Predefined curve shape.</span></span>

<span data-ttu-id="00673-111">**曲線** 使用 [to](to-attribute--curve--vml.md)、 [from](from-attribute--curve--vml.md)、 [control1](msdn-online-vml-control1-attribute.md)和 [control2](msdn-online-vml-control2-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="00673-111">**Curve** uses the [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [control1](msdn-online-vml-control1-attribute.md), and [control2](msdn-online-vml-control2-attribute.md) attributes.</span></span>

<span data-ttu-id="00673-112">以下是產生影像所需的最少程式碼。</span><span class="sxs-lookup"><span data-stu-id="00673-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 