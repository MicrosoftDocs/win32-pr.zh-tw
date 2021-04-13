---
description: 本節包含有關 DXGI 所提供之函式的資訊。
ms.assetid: 209d2e65-b118-47a7-aece-fb140fdede3f
title: DXGI 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06cb98c47ec3e2cb841aa5c27017ee6bb614f9e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509880"
---
# <a name="dxgi-functions"></a><span data-ttu-id="e6b9f-103">DXGI 函數</span><span class="sxs-lookup"><span data-stu-id="e6b9f-103">DXGI Functions</span></span>

<span data-ttu-id="e6b9f-104">本節包含有關 DXGI 所提供之函式的資訊。</span><span class="sxs-lookup"><span data-stu-id="e6b9f-104">This section contains info about the functions provided by DXGI.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e6b9f-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="e6b9f-105">In this section</span></span>



| <span data-ttu-id="e6b9f-106">主題</span><span class="sxs-lookup"><span data-stu-id="e6b9f-106">Topic</span></span>                                                                                   | <span data-ttu-id="e6b9f-107">描述</span><span class="sxs-lookup"><span data-stu-id="e6b9f-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6b9f-108">**CreateDXGIFactory**</span><span class="sxs-lookup"><span data-stu-id="e6b9f-108">**CreateDXGIFactory**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)<br/>                               | <span data-ttu-id="e6b9f-109">建立可用來產生其他 DXGI 物件的 DXGI 1.0 factory。</span><span class="sxs-lookup"><span data-stu-id="e6b9f-109">Creates a DXGI 1.0 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="e6b9f-110">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="e6b9f-110">**CreateDXGIFactory1**</span></span>](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)<br/>                             | <span data-ttu-id="e6b9f-111">建立可用來產生其他 DXGI 物件的 DXGI 1.1 factory。</span><span class="sxs-lookup"><span data-stu-id="e6b9f-111">Creates a DXGI 1.1 factory that you can use to generate other DXGI objects.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="e6b9f-112">**CreateDXGIFactory2**</span><span class="sxs-lookup"><span data-stu-id="e6b9f-112">**CreateDXGIFactory2**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2)<br/>                             | <span data-ttu-id="e6b9f-113">建立可用來產生其他 DXGI 物件的 DXGI 1.3 factory。</span><span class="sxs-lookup"><span data-stu-id="e6b9f-113">Creates a DXGI 1.3 factory that you can use to generate other DXGI objects.</span></span><br/> <span data-ttu-id="e6b9f-114">在 Windows 8 中，系統上 DXGIDebug.dll 所建立的任何 DXGI factory 都會載入並使用它。</span><span class="sxs-lookup"><span data-stu-id="e6b9f-114">In Windows 8, any DXGI factory created while DXGIDebug.dll was present on the system would load and use it.</span></span> <span data-ttu-id="e6b9f-115">從 Windows 8.1 開始，應用程式會明確要求改為載入 DXGIDebug.dll。</span><span class="sxs-lookup"><span data-stu-id="e6b9f-115">Starting in Windows 8.1, apps explicitly request that DXGIDebug.dll be loaded instead.</span></span> <span data-ttu-id="e6b9f-116">使用 [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) 並指定 DXGI \_ 建立 \_ FACTORY 的 \_ 偵錯工具旗標來要求 DXGIDebug.dll; 如果系統上有 DLL，則會載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="e6b9f-116">Use [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) and specify the DXGI\_CREATE\_FACTORY\_DEBUG flag to request DXGIDebug.dll; the DLL will be loaded if it is present on the system.</span></span><br/> |
| [<span data-ttu-id="e6b9f-117">**DXGIDeclareAdapterRemovalSupport**</span><span class="sxs-lookup"><span data-stu-id="e6b9f-117">**DXGIDeclareAdapterRemovalSupport**</span></span>](/windows/desktop/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)<br/> | <span data-ttu-id="e6b9f-118">可讓進程指出它是否能夠復原任何正在移除的圖形裝置。</span><span class="sxs-lookup"><span data-stu-id="e6b9f-118">Allows a process to indicate that it's resilient to any of its graphics devices being removed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="e6b9f-119">**DXGIGetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="e6b9f-119">**DXGIGetDebugInterface**</span></span>](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)<br/>                       | <span data-ttu-id="e6b9f-120">抓取調試介面。</span><span class="sxs-lookup"><span data-stu-id="e6b9f-120">Retrieves a debugging interface.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="e6b9f-121">**DXGIGetDebugInterface1**</span><span class="sxs-lookup"><span data-stu-id="e6b9f-121">**DXGIGetDebugInterface1**</span></span>](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-dxgigetdebuginterface1)<br/>                     | <span data-ttu-id="e6b9f-122">抓取 Windows Store 應用程式用來對 Microsoft DirectX Graphic Infrastructure (DXGI) 進行偵錯工具的介面。</span><span class="sxs-lookup"><span data-stu-id="e6b9f-122">Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="e6b9f-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e6b9f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6b9f-124">DXGI 參考</span><span class="sxs-lookup"><span data-stu-id="e6b9f-124">DXGI Reference</span></span>](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

 




