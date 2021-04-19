---
description: 智慧型轉譯引擎
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: 智慧型轉譯引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972933"
---
# <a name="smart-render-engine"></a><span data-ttu-id="1b80e-103">智慧型轉譯引擎</span><span class="sxs-lookup"><span data-stu-id="1b80e-103">Smart Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="1b80e-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="1b80e-104">\[Deprecated.</span></span> <span data-ttu-id="1b80e-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="1b80e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1b80e-106">智慧型轉譯引擎物件會從時間軸轉譯壓縮的輸出。</span><span class="sxs-lookup"><span data-stu-id="1b80e-106">The Smart Render Engine object renders compressed output from a timeline.</span></span> <span data-ttu-id="1b80e-107">若要建立這個物件，請呼叫 **CoCreateInstance**。</span><span class="sxs-lookup"><span data-stu-id="1b80e-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="1b80e-108">針對未壓縮的輸出，請使用基本轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="1b80e-108">For uncompressed output, use the Basic Render Engine.</span></span> <span data-ttu-id="1b80e-109">類別識別碼是 CLSID \_ SmartRenderEngine。</span><span class="sxs-lookup"><span data-stu-id="1b80e-109">The class identifier is CLSID\_SmartRenderEngine.</span></span>

<span data-ttu-id="1b80e-110">智慧型轉譯引擎會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="1b80e-110">The Smart Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="1b80e-111">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="1b80e-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="1b80e-112">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="1b80e-112">**IObjectWithSite**</span></span>
-   [<span data-ttu-id="1b80e-113">**IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="1b80e-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="1b80e-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="1b80e-114">**IRenderEngine2**</span></span>](irenderengine2.md)
-   [<span data-ttu-id="1b80e-115">**ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="1b80e-115">**ISmartRenderEngine**</span></span>](ismartrenderengine.md)

## <a name="related-topics"></a><span data-ttu-id="1b80e-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="1b80e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b80e-117">轉譯專案</span><span class="sxs-lookup"><span data-stu-id="1b80e-117">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="1b80e-118">基本轉譯引擎</span><span class="sxs-lookup"><span data-stu-id="1b80e-118">Basic Render Engine</span></span>](basic-render-engine.md)
</dt> </dl>

 

 



