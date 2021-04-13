---
description: 基本轉譯引擎
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: 基本轉譯引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510216"
---
# <a name="basic-render-engine"></a><span data-ttu-id="13e84-103">基本轉譯引擎</span><span class="sxs-lookup"><span data-stu-id="13e84-103">Basic Render Engine</span></span>

> [!Note]  
> <span data-ttu-id="13e84-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="13e84-104">\[Deprecated.</span></span> <span data-ttu-id="13e84-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="13e84-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="13e84-106">基本轉譯引擎物件會從時間軸轉譯未壓縮的輸出。</span><span class="sxs-lookup"><span data-stu-id="13e84-106">The Basic Render Engine object renders uncompressed output from a timeline.</span></span> <span data-ttu-id="13e84-107">若要建立這個物件，請呼叫 **CoCreateInstance**。</span><span class="sxs-lookup"><span data-stu-id="13e84-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="13e84-108">針對壓縮的輸出，請使用智慧型轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="13e84-108">For compressed output, use the Smart Render Engine.</span></span> <span data-ttu-id="13e84-109">類別識別碼是 CLSID \_ RenderEngine。</span><span class="sxs-lookup"><span data-stu-id="13e84-109">The class identifier is CLSID\_RenderEngine.</span></span>

<span data-ttu-id="13e84-110">基本轉譯引擎會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="13e84-110">The Basic Render Engine exposes the following interfaces:</span></span>

-   [<span data-ttu-id="13e84-111">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="13e84-111">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   <span data-ttu-id="13e84-112">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="13e84-112">IObjectWithSite</span></span>
-   [<span data-ttu-id="13e84-113">**IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="13e84-113">**IRenderEngine**</span></span>](irenderengine.md)
-   [<span data-ttu-id="13e84-114">**IRenderEngine2**</span><span class="sxs-lookup"><span data-stu-id="13e84-114">**IRenderEngine2**</span></span>](irenderengine2.md)

## <a name="related-topics"></a><span data-ttu-id="13e84-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="13e84-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13e84-116">轉譯專案</span><span class="sxs-lookup"><span data-stu-id="13e84-116">Rendering a Project</span></span>](rendering-a-project.md)
</dt> <dt>

[<span data-ttu-id="13e84-117">智慧型轉譯引擎</span><span class="sxs-lookup"><span data-stu-id="13e84-117">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> </dl>

 

 



