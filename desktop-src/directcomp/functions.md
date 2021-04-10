---
title: DirectComposition 函式
description: 本節說明 Microsoft DirectComposition \ 32 所提供的功能;Api。
ms.assetid: 750FDFD5-ADD5-43B3-A596-ECDB82C2EF73
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934e0b7e32f22faaefdf625e0af2a42a03e469d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092819"
---
# <a name="directcomposition-functions"></a><span data-ttu-id="4e2ae-103">DirectComposition 函式</span><span class="sxs-lookup"><span data-stu-id="4e2ae-103">DirectComposition functions</span></span>

<span data-ttu-id="4e2ae-104">本節說明 Microsoft DirectComposition API 所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="4e2ae-104">This section describes the functions provided by the Microsoft DirectComposition API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4e2ae-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="4e2ae-105">In this section</span></span>



| <span data-ttu-id="4e2ae-106">主題</span><span class="sxs-lookup"><span data-stu-id="4e2ae-106">Topic</span></span>                                                                                       | <span data-ttu-id="4e2ae-107">描述</span><span class="sxs-lookup"><span data-stu-id="4e2ae-107">Description</span></span>                                                                                                                                          |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e2ae-108">**DCompositionAttachMouseDragToHwnd**</span><span class="sxs-lookup"><span data-stu-id="4e2ae-108">**DCompositionAttachMouseDragToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousedragtohwnd)<br/>   | <span data-ttu-id="4e2ae-109">建立互動/InputSink，以將滑鼠按鍵向下移動，並將任何後續的 move 和 up 事件路由至指定的 HWND。</span><span class="sxs-lookup"><span data-stu-id="4e2ae-109">Creates an Interaction/InputSink to route mouse button down and any subsequent move and up events to the given HWND.</span></span><br/>                      |
| [<span data-ttu-id="4e2ae-110">**DCompositionAttachMouseWheelToHwnd**</span><span class="sxs-lookup"><span data-stu-id="4e2ae-110">**DCompositionAttachMouseWheelToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousewheeltohwnd)<br/> | <span data-ttu-id="4e2ae-111">建立互動/InputSink，以將滑鼠滾輪訊息路由至指定的 HWND。</span><span class="sxs-lookup"><span data-stu-id="4e2ae-111">Creates an Interaction/InputSink to route mouse wheel messages to the given HWND.</span></span> <br/>                                                        |
| [<span data-ttu-id="4e2ae-112">**DCompositionCreateDevice**</span><span class="sxs-lookup"><span data-stu-id="4e2ae-112">**DCompositionCreateDevice**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)<br/>                     | <span data-ttu-id="4e2ae-113">建立新的裝置物件，可用來建立其他 DirectComposition 物件。</span><span class="sxs-lookup"><span data-stu-id="4e2ae-113">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="4e2ae-114">**DCompositionCreateDevice2**</span><span class="sxs-lookup"><span data-stu-id="4e2ae-114">**DCompositionCreateDevice2**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice2)<br/>                   | <span data-ttu-id="4e2ae-115">建立新的裝置物件，可用來建立其他 DirectComposition 物件。</span><span class="sxs-lookup"><span data-stu-id="4e2ae-115">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="4e2ae-116">**DCompositionCreateDevice3**</span><span class="sxs-lookup"><span data-stu-id="4e2ae-116">**DCompositionCreateDevice3**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatedevice3)<br/>                   | <span data-ttu-id="4e2ae-117">建立新的 DirectComposition 裝置物件，可用於建立其他 DirectComposition 物件。</span><span class="sxs-lookup"><span data-stu-id="4e2ae-117">Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.</span></span><br/>                               |
| [<span data-ttu-id="4e2ae-118">**DCompositionCreateSurfaceHandle**</span><span class="sxs-lookup"><span data-stu-id="4e2ae-118">**DCompositionCreateSurfaceHandle**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatesurfacehandle)<br/>       | <span data-ttu-id="4e2ae-119">建立新的組合介面物件，該物件可以系結至 Microsoft DirectX 交換鏈或交換緩衝區，並與視覺效果建立關聯。</span><span class="sxs-lookup"><span data-stu-id="4e2ae-119">Creates a new composition surface object that can be bound to a Microsoft DirectX swap chain or swap buffer and associated with a visual.</span></span><br/> |
| <span data-ttu-id="4e2ae-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e2ae-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span></span><br/>         | <span data-ttu-id="4e2ae-121">抓取撰寫統計資訊。</span><span class="sxs-lookup"><span data-stu-id="4e2ae-121">Retrieves composition statistics information.</span></span><br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="4e2ae-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e2ae-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e2ae-123">DirectComposition 參考</span><span class="sxs-lookup"><span data-stu-id="4e2ae-123">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

