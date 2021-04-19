---
description: 時間表
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: 時間表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985502"
---
# <a name="timeline"></a><span data-ttu-id="435ba-103">時間表</span><span class="sxs-lookup"><span data-stu-id="435ba-103">Timeline</span></span>

> [!Note]  
> <span data-ttu-id="435ba-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="435ba-104">\[Deprecated.</span></span> <span data-ttu-id="435ba-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="435ba-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="435ba-106">時間軸物件會管理影片編輯專案中的所有物件。</span><span class="sxs-lookup"><span data-stu-id="435ba-106">The timeline object manages all of the objects in a video editing project.</span></span> <span data-ttu-id="435ba-107">若要建立這個物件，請呼叫 **CoCreateInstance**。</span><span class="sxs-lookup"><span data-stu-id="435ba-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="435ba-108">類別識別碼是 CLSID \_ AMTimeline。</span><span class="sxs-lookup"><span data-stu-id="435ba-108">The class identifier is CLSID\_AMTimeline.</span></span>

<span data-ttu-id="435ba-109">若要讀取 Windows Media™檔案，應用程式必須提供軟體憑證，也稱為金鑰。</span><span class="sxs-lookup"><span data-stu-id="435ba-109">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="435ba-110">透過時間軸的 **IObjectWithSite** 介面，將應用程式註冊為金鑰提供者。</span><span class="sxs-lookup"><span data-stu-id="435ba-110">Register the application as a key provider through the timeline's **IObjectWithSite** interface.</span></span> <span data-ttu-id="435ba-111">如需詳細資訊，請參閱 [解除鎖定 Windows Media FORMAT SDK](unlocking-the-windows-media-format-sdk.md)。</span><span class="sxs-lookup"><span data-stu-id="435ba-111">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="435ba-112">時間軸物件會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="435ba-112">The timeline object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="435ba-113">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="435ba-113">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   [<span data-ttu-id="435ba-114">**IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="435ba-114">**IAMTimeline**</span></span>](iamtimeline.md)
-   <span data-ttu-id="435ba-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="435ba-115">**IObjectWithSite**</span></span>
-   <span data-ttu-id="435ba-116">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="435ba-116">**IPersistStream**</span></span>

## <a name="related-topics"></a><span data-ttu-id="435ba-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="435ba-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="435ba-118">時間軸模型</span><span class="sxs-lookup"><span data-stu-id="435ba-118">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="435ba-119">建立時間軸</span><span class="sxs-lookup"><span data-stu-id="435ba-119">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



