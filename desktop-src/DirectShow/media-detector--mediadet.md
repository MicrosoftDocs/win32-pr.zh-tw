---
description: '媒體偵測器 (MediaDet) '
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: '媒體偵測器 (MediaDet) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116057"
---
# <a name="media-detector-mediadet"></a><span data-ttu-id="46d8e-103">媒體偵測器 (MediaDet) </span><span class="sxs-lookup"><span data-stu-id="46d8e-103">Media Detector (MediaDet)</span></span>

> [!Note]  
> <span data-ttu-id="46d8e-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="46d8e-104">\[Deprecated.</span></span> <span data-ttu-id="46d8e-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="46d8e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="46d8e-106">媒體偵測器 (MediaDet) 物件會從檔案來源抓取格式資訊和仍然是畫面格。</span><span class="sxs-lookup"><span data-stu-id="46d8e-106">The Media Detector (MediaDet) object retrieves format information and still frames from file sources.</span></span> <span data-ttu-id="46d8e-107">媒體偵測器不需要篩選圖形管理員就能運作。</span><span class="sxs-lookup"><span data-stu-id="46d8e-107">The Media Detector does not require the Filter Graph Manager to function.</span></span> <span data-ttu-id="46d8e-108">若要建立這個物件，請呼叫 **CoCreateInstance**。</span><span class="sxs-lookup"><span data-stu-id="46d8e-108">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="46d8e-109">類別識別碼是 CLSID \_ MediaDet。</span><span class="sxs-lookup"><span data-stu-id="46d8e-109">The class identifier is CLSID\_MediaDet.</span></span>

<span data-ttu-id="46d8e-110">若要讀取 Windows Media™檔案，應用程式必須提供軟體憑證，也稱為金鑰。</span><span class="sxs-lookup"><span data-stu-id="46d8e-110">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="46d8e-111">透過媒體偵測器的 **IObjectWithSite** 介面，將應用程式註冊為金鑰提供者。</span><span class="sxs-lookup"><span data-stu-id="46d8e-111">Register the application as a key provider through the Media Detector's **IObjectWithSite** interface.</span></span> <span data-ttu-id="46d8e-112">如需詳細資訊，請參閱 [解除鎖定 Windows Media FORMAT SDK](unlocking-the-windows-media-format-sdk.md)。</span><span class="sxs-lookup"><span data-stu-id="46d8e-112">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="46d8e-113">MediaDet 物件會公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="46d8e-113">The MediaDet object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="46d8e-114">**IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="46d8e-114">**IMediaDet**</span></span>](imediadet.md)
-   <span data-ttu-id="46d8e-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="46d8e-115">**IObjectWithSite**</span></span>

## <a name="related-topics"></a><span data-ttu-id="46d8e-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="46d8e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46d8e-117">使用來源</span><span class="sxs-lookup"><span data-stu-id="46d8e-117">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



