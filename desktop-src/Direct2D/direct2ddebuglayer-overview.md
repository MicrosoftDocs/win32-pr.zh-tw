---
title: Direct2D Debug 圖層總覽
description: .
ms.assetid: 7c28e00b-ebb9-4b79-939c-64eade1351ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df560595ea0ae6c7a56c3fa568f2f94ae56652ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965563"
---
# <a name="direct2d-debug-layer-overview"></a><span data-ttu-id="0a7ab-103">Direct2D Debug 圖層總覽</span><span class="sxs-lookup"><span data-stu-id="0a7ab-103">Direct2D Debug Layer Overview</span></span>

<span data-ttu-id="0a7ab-104">Direct2D debug 層提供設計階段的偵錯工具訊息，可讓您將執行時間應用程式失敗降至最低。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-104">The Direct2D debug layer provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="0a7ab-105">本總覽描述 Direct2D debug 層的基本概念。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-105">This overview describes the basics of the Direct2D debug layer.</span></span> <span data-ttu-id="0a7ab-106">它會假設您已熟悉如何建立基本 Direct2D 應用程式。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-106">It assumes that you are familiar with creating basic Direct2D applications.</span></span>

<span data-ttu-id="0a7ab-107">本總覽包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-107">This overview contains the following sections.</span></span>

-   [<span data-ttu-id="0a7ab-108">什麼是 Direct2D Debug 層級</span><span class="sxs-lookup"><span data-stu-id="0a7ab-108">What Is the Direct2D Debug Layer</span></span>](#what-is-the-direct2d-debug-layer)
-   [<span data-ttu-id="0a7ab-109">安裝 Direct2D Debug Layer</span><span class="sxs-lookup"><span data-stu-id="0a7ab-109">Installing the Direct2D Debug Layer</span></span>](#installing-the-direct2d-debug-layer)
-   [<span data-ttu-id="0a7ab-110">啟用 Debug 圖層</span><span class="sxs-lookup"><span data-stu-id="0a7ab-110">Enabling the Debug Layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="0a7ab-111">Debug 層級</span><span class="sxs-lookup"><span data-stu-id="0a7ab-111">Debug Levels</span></span>](#debug-levels)
-   [<span data-ttu-id="0a7ab-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a7ab-112">Related topics</span></span>](#related-topics)

## <a name="what-is-the-direct2d-debug-layer"></a><span data-ttu-id="0a7ab-113">什麼是 Direct2D Debug 層級</span><span class="sxs-lookup"><span data-stu-id="0a7ab-113">What Is the Direct2D Debug Layer</span></span>

<span data-ttu-id="0a7ab-114">Direct2D debug 層會在其本身 DLL 中的 Direct2D （名為 d2d1debug.dll）分開執行，提供可讓您精確地使用 Direct2D 函式的調試訊息。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-114">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides debug messages to enable you to accurately use Direct2D functions.</span></span> <span data-ttu-id="0a7ab-115">調試訊息通常是因為 API 合約違規所造成，例如不正確參數 (可能是 Direct3D 相關的) 、不正確資源、執行緒違規和效能問題，例如在剪輯足夠的情況下使用圖層。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-115">The debug messages often result from API contract violations such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and performance issues such as using a layer when a clip would suffice.</span></span> <span data-ttu-id="0a7ab-116">若要指定 debug 層追蹤的資訊量，您可以指定下列三個調試層級的其中一個：資訊、警告和錯誤。和層級錯誤的訊息會觸發中斷點，以協助您進行調試。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-116">To specify how much information is traced by the debug layer, you can specify one of the three debug levels: information, warning, and error; and a message of level error triggers the breakpoint to help you debug.</span></span>

## <a name="installing-the-direct2d-debug-layer"></a><span data-ttu-id="0a7ab-117">安裝 Direct2D Debug Layer</span><span class="sxs-lookup"><span data-stu-id="0a7ab-117">Installing the Direct2D Debug Layer</span></span>

<span data-ttu-id="0a7ab-118">如需有關安裝調試層的指示，請參閱 [安裝 Direct2D 調試層](installing-the-direct2d-debug-layer.md)。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-118">For instructions on installing the debug layer, see [Installing the Direct2D Debug Layer](installing-the-direct2d-debug-layer.md).</span></span>

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="0a7ab-119">啟用 Debug 圖層</span><span class="sxs-lookup"><span data-stu-id="0a7ab-119">Enabling the Debug Layer</span></span>

<span data-ttu-id="0a7ab-120">若要在您的應用程式中啟用 debug 圖層，請在使用 [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)函式建立處理站時，指定 **D2D1 \_ debug \_ level \_ NONE** 以外的 [**D2D1 \_ 調試層 \_ 級**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level)值。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-120">To enable the debug layer in your application, specify a [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) value other than **D2D1\_DEBUG\_LEVEL\_NONE** when you create a factory with the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>

> [!Note]  
> <span data-ttu-id="0a7ab-121">如果已啟用 Direct2D debug 圖層，則在設定色彩內容時，Direct2D 色彩管理效果 (CLSID \_ D2D1ColorManagement) 可能會造成存取違規。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-121">If the Direct2D debug layer is enabled, the Direct2D color management effect (CLSID\_D2D1ColorManagement) may cause an access violation when setting a color context.</span></span> <span data-ttu-id="0a7ab-122">解決方法是在使用色彩管理效果時停用調試層</span><span class="sxs-lookup"><span data-stu-id="0a7ab-122">The workaround is to disable the debug layer when using the color management effect</span></span>

 

<span data-ttu-id="0a7ab-123">啟用 factory 的 debug 層也會啟用該處理站所建立之任何物件的偵錯工具資訊。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-123">Enabling the debug layer for a factory also enables debugging information for any object created by that factory.</span></span>

<span data-ttu-id="0a7ab-124">下列範例會在針對 DEBUG 組建設定編譯應用程式時，啟用 factory 的 debug 層。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-124">The following example enables the debug layer for a factory when the application is compiled for the DEBUG build configuration.</span></span>


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif
```



> [!Note]  
> <span data-ttu-id="0a7ab-125">如果未指定任何 factory 選項，或指定了「無」的 debug 層級，則不會叫用 debug 層。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-125">If no factory options are specified or a debug level of "none" is specified, the debug layer is not invoked.</span></span> <span data-ttu-id="0a7ab-126">在應用程式的發行版本中，不應使用 debug 層。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-126">The debug layer should never be active in the release version of an application.</span></span>

 

<span data-ttu-id="0a7ab-127">下一節將說明 [**D2D1 \_ debug \_ 層級**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) 列舉所定義的不同調試層級。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-127">The next section describes the different debug levels defined by the [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration.</span></span>

## <a name="debug-levels"></a><span data-ttu-id="0a7ab-128">Debug 層級</span><span class="sxs-lookup"><span data-stu-id="0a7ab-128">Debug Levels</span></span>

<span data-ttu-id="0a7ab-129">[**D2D1 \_ debug \_ level**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level)列舉會指定三個 DEBUG 層級： D2D1 \_ debug \_ LEVEL \_ error (error) 、D2D1 \_ debug \_ level \_ warning (warning) 和 D2D1 \_ DEBUG \_ level \_ information (資訊) 。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-129">The [**D2D1\_DEBUG\_LEVEL**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level) enumeration specifies three debug levels: D2D1\_DEBUG\_LEVEL\_ERROR (error), D2D1\_DEBUG\_LEVEL\_WARNING (warning), and D2D1\_DEBUG\_LEVEL\_INFORMATION (information).</span></span> <span data-ttu-id="0a7ab-130">這些層級的解讀方式如下：</span><span class="sxs-lookup"><span data-stu-id="0a7ab-130">These levels are interpreted as follows:</span></span>

-   <span data-ttu-id="0a7ab-131">**錯誤：** Direct2D 會將嚴重的錯誤訊息傳送至 debug 層。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-131">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="0a7ab-132">例如，中斷線程條件約束將會產生嚴重的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-132">For example, breaking a threading constraint will generate a severe error.</span></span>

-   <span data-ttu-id="0a7ab-133">**警告：** Direct2D 會將錯誤訊息和警告傳送至 debug 圖層，以便您可以處理這些訊息。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-133">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="0a7ab-134">**資訊：** Direct2D 會將錯誤訊息、警告和其他診斷資訊傳送至 debug 圖層。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-134">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="0a7ab-135">例如，效能改進訊息將會在這個 debug 層級傳送。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-135">For example, performance improvement messages will be sent at this debug level.</span></span>

<span data-ttu-id="0a7ab-136">值 D2D1 \_ DEBUG \_ LEVEL \_ none (None) 表示 Direct2D 不提供任何偵錯工具輸出。</span><span class="sxs-lookup"><span data-stu-id="0a7ab-136">The value D2D1\_DEBUG\_LEVEL\_NONE (none) indicates that Direct2D does not provide any debugging output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a7ab-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a7ab-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a7ab-138">Debug 訊息</span><span class="sxs-lookup"><span data-stu-id="0a7ab-138">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)
</dt> </dl>

 

 




