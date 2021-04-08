---
title: 選擇正確的方法來 Windows Touch
description: 本節說明您可以使用 Windows Touch 不同的方法。
ms.assetid: 983023e4-355b-45ba-8572-d93c460d2ff8
keywords:
- Windows Touch，不同的方法
- Windows Touch，選擇方法
- Windows Touch，增強應用程式
- Windows Touch，縮放支援
- Windows Touch，舊版支援
- Windows Touch，RealTimeStylus 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cdd35b73989541fadd5449efbb3f95d76bfa5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023852"
---
# <a name="choosing-the-right-approach-to-windows-touch"></a><span data-ttu-id="90ede-109">選擇正確的方法來 Windows Touch</span><span class="sxs-lookup"><span data-stu-id="90ede-109">Choosing the Right Approach to Windows Touch</span></span>

<span data-ttu-id="90ede-110">本節說明您可以使用 Windows Touch 不同的方法。</span><span class="sxs-lookup"><span data-stu-id="90ede-110">This section explains the different approaches to Windows Touch that you can use.</span></span>

<span data-ttu-id="90ede-111">您可以透過許多方式使用 Windows Touch 功能來增強應用程式。</span><span class="sxs-lookup"><span data-stu-id="90ede-111">You can enhance applications using Windows Touch features in many ways.</span></span> <span data-ttu-id="90ede-112">在您採用方法之前，您應該考慮您想要如何處理您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="90ede-112">Before you adopt a method, you should consider what you want to do with your application.</span></span> <span data-ttu-id="90ede-113">以下是 Windows Touch 的一般案例：</span><span class="sxs-lookup"><span data-stu-id="90ede-113">The following scenarios are typical for Windows Touch:</span></span>

-   <span data-ttu-id="90ede-114">您希望應用程式的行為與舊版 Windows 中的行為相同，但希望 Windows Touch 訊息的行為一致。</span><span class="sxs-lookup"><span data-stu-id="90ede-114">You want your application to behave the same as in legacy versions of Windows but want Windows Touch messages to behave consistently.</span></span>
-   <span data-ttu-id="90ede-115">您想要在您的應用程式中進行自訂物件旋轉、轉譯、移動或縮放支援。</span><span class="sxs-lookup"><span data-stu-id="90ede-115">You want custom object rotation, translation, panning, or zoom support in your application.</span></span>
-   <span data-ttu-id="90ede-116">您希望您的應用程式能夠更精細地解讀 Windows Touch 手勢，或在特別針對 Windows Touch 輸入優化的應用程式上解讀多次觸控。</span><span class="sxs-lookup"><span data-stu-id="90ede-116">You want your application to have fine-grained interpretation of Windows Touch gestures or to interpret multiple touches on an application that is specifically optimized for Windows Touch input.</span></span>
-   <span data-ttu-id="90ede-117">您有一個使用 [**RealTimeStylus**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus) 物件的應用程式，而且想要使用 Windows Touch 功能來增強它。</span><span class="sxs-lookup"><span data-stu-id="90ede-117">You have an application that uses the [**RealTimeStylus**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus) object and want to enhance it with Windows Touch capabilities.</span></span>

## <a name="you-want-your-application-to-behave-as-it-did-in-legacy-versions-of-windows"></a><span data-ttu-id="90ede-118">您希望應用程式的行為與舊版 Windows 相同</span><span class="sxs-lookup"><span data-stu-id="90ede-118">You want your application to behave as it did in legacy versions of Windows</span></span>

<span data-ttu-id="90ede-119">在 Windows 7 中，應用程式預設會產生可啟用 Windows Touch 功能的訊息。</span><span class="sxs-lookup"><span data-stu-id="90ede-119">In Windows 7, applications by default generate messages that enable Windows Touch functionality.</span></span> <span data-ttu-id="90ede-120">例如，平移手勢會觸發 WM \_ \* 捲軸訊息。</span><span class="sxs-lookup"><span data-stu-id="90ede-120">For example, pan gestures trigger WM\_\*SCROLL messages.</span></span> <span data-ttu-id="90ede-121">除了 pan 支援之外，Windows 7 中的預設 WM 軌跡 \_ 處理常式還支援界限意見反應、縮放，以及按下和點擊。</span><span class="sxs-lookup"><span data-stu-id="90ede-121">In addition to pan support, the default WM\_GESTURE handler in Windows 7 supports boundary feedback, zoom, and press and tap.</span></span> <span data-ttu-id="90ede-122">您也可以透過舊版支援來啟用界限意見反應。</span><span class="sxs-lookup"><span data-stu-id="90ede-122">Boundary feedback is enabled through legacy support as well.</span></span> <span data-ttu-id="90ede-123">如需手勢如何對應至訊息的詳細資訊，請參閱 [Windows Touch 手勢總覽](windows-touch-gestures-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="90ede-123">See the [Windows Touch Gestures Overview](windows-touch-gestures-overview.md) for more information on how gestures map to messages.</span></span> <span data-ttu-id="90ede-124">只想要使用這種基本功能的開發人員不需要直接使用 Windows Touch API。</span><span class="sxs-lookup"><span data-stu-id="90ede-124">Developers who want only this basic functionality do not need to directly work with the Windows Touch API.</span></span>

> [!Note]  
> <span data-ttu-id="90ede-125">自訂捲軸處理常式必須支援適用于 **wm \_ VSCROLL** 訊息的 **SM \_ THUMBPOSITION** 要求，且必須支援 sb **\_ HSCROLL** 訊息的 **sb \_ LINELEFT** 要求和 **sb \_ LINERIGHT** 要求。</span><span class="sxs-lookup"><span data-stu-id="90ede-125">Custom scroll bar handlers must support the **SM\_THUMBPOSITION** request for **WM\_VSCROLL** messages and must support the **SB\_LINELEFT** request and **SB\_LINERIGHT** request for **WM\_HSCROLL** messages.</span></span>

 

-   <span data-ttu-id="90ede-126">[舊版對於移動捲軸的支援](legacy-support-for-panning-with-scrollbars.md)區段說明如何確保您的應用程式在 Windows 7 中的行為如同使用者預期。</span><span class="sxs-lookup"><span data-stu-id="90ede-126">The [Legacy Support for Panning with Scroll Bars](legacy-support-for-panning-with-scrollbars.md) section explains how to ensure that your application behaves as users expect in Windows 7.</span></span>

## <a name="you-want-custom-object-rotation-translation-panning-or-zoom-support"></a><span data-ttu-id="90ede-127">您想要自訂物件旋轉、轉譯、移動流覽或縮放支援</span><span class="sxs-lookup"><span data-stu-id="90ede-127">You want custom object rotation, translation, panning, or zoom support</span></span>

<span data-ttu-id="90ede-128">如果您想讓觸控的支援有限，但 Windows 7 提供的預設行為並不適用于您的應用程式，您可以使用筆勢來增強您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="90ede-128">If you want limited support for touch but the default behavior that Windows 7 offers is not adequate for your application, you can use gestures to enhance your application.</span></span> <span data-ttu-id="90ede-129">藉由使用筆勢，您可以藉由處理 [**WM \_ 手勢**](wm-gesture.md) 訊息來解讀手勢命令。</span><span class="sxs-lookup"><span data-stu-id="90ede-129">By using gestures, you can interpret the gesture commands by handling the [**WM\_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="90ede-130">如需筆勢的詳細資訊，請參閱 [Windows Touch 手勢](guide-multi-touch-gestures.md)一節。</span><span class="sxs-lookup"><span data-stu-id="90ede-130">More information on gestures can be found in the section [Windows Touch Gestures](guide-multi-touch-gestures.md).</span></span> <span data-ttu-id="90ede-131">如果您的應用程式只需要支援高度細微的旋轉、改善的縮放支援或單指移動，手勢就是進行 Windows Touch 開發的最佳方法。</span><span class="sxs-lookup"><span data-stu-id="90ede-131">If your application needs support only for high-granularity rotations, improved zooming support, or single-finger panning, gestures is the best approach to take for Windows Touch development.</span></span> <span data-ttu-id="90ede-132">除了解讀手勢訊息，您也可以選擇支援界限意見反應。</span><span class="sxs-lookup"><span data-stu-id="90ede-132">In addition to interpreting the gesture message, you can opt to have support for boundary feedback.</span></span> <span data-ttu-id="90ede-133">如需界限意見反應的詳細資訊，請參閱[Windows Touch 程式設計參考](windows-touch-programming-reference.md)的[界限意見](boundary-feedback.md)一節。</span><span class="sxs-lookup"><span data-stu-id="90ede-133">For more information on boundary feedback, see the [Boundary Feedback](boundary-feedback.md) section of the [Windows Touch Programming Reference](windows-touch-programming-reference.md).</span></span> <span data-ttu-id="90ede-134">在 Windows 7 中，命令提示字元和 Internet Explorer 會利用界限意見反應和手勢。</span><span class="sxs-lookup"><span data-stu-id="90ede-134">In Windows 7, the command prompt and Internet Explorer take advantage of boundary feedback and gestures.</span></span>

-   <span data-ttu-id="90ede-135">[改進單一手指移動體驗](improving-the-single-finger-panning-experience.md)一節說明如何藉由處理 [**WM \_ 手勢**](wm-gesture.md)訊息來自訂移動流覽體驗。</span><span class="sxs-lookup"><span data-stu-id="90ede-135">The [Improving the Single Finger Panning Experience](improving-the-single-finger-panning-experience.md) section explains how to customize the panning experience by handling the [**WM\_GESTURE**](wm-gesture.md) message.</span></span>

## <a name="you-want-fine-grained-gesture-interpretation-or-custom-handling-of-multiple-touch-points"></a><span data-ttu-id="90ede-136">您需要更細緻的手勢解讀或多個觸控點的自訂處理</span><span class="sxs-lookup"><span data-stu-id="90ede-136">You want fine-grained gesture interpretation or custom handling of multiple touch points</span></span>

<span data-ttu-id="90ede-137">如果您想要比 [**WM \_ 手勢**](wm-gesture.md) 訊息所提供的手勢更明確地控制手勢，或想要在多個物件上解讀多個手勢，則應該使用操作處理器。</span><span class="sxs-lookup"><span data-stu-id="90ede-137">If you want to have even more specific control of gestures than is offered by the [**WM\_GESTURE**](wm-gesture.md) message, or you want to interpret multiple gestures on multiple objects, you should use the manipulation processor.</span></span> <span data-ttu-id="90ede-138">操作處理器基本上是筆勢的超集合。</span><span class="sxs-lookup"><span data-stu-id="90ede-138">The manipulation processor essentially is a superset of gestures.</span></span> <span data-ttu-id="90ede-139">使用操作處理器需要您針對將原始觸控資料摘要至的操作，執行事件接收器。</span><span class="sxs-lookup"><span data-stu-id="90ede-139">Using the manipulation processor requires that you implement an event sink for manipulations that you feed raw touch data to.</span></span>

<span data-ttu-id="90ede-140">如果您想要在解讀手勢以外的情況下使用簡單的物件物理，您應該搭配操作處理器使用慣性處理器。</span><span class="sxs-lookup"><span data-stu-id="90ede-140">If you want simple object physics in addition to interpreting the gestures, you should use an inertia processor in conjunction with the manipulation processor.</span></span> <span data-ttu-id="90ede-141">慣性處理器適用于操作處理器，方法是在操作完成時從操作處理器取得速度值。</span><span class="sxs-lookup"><span data-stu-id="90ede-141">The inertia processor works with the manipulation processor by taking velocity values from the manipulation processor upon manipulation completion.</span></span>

<span data-ttu-id="90ede-142">如果您想要在您的應用程式中解讀多個觸控點，您應該建立一封 [**WM \_ 觸控**](wm-touchdown.md) 訊息的訊息處理常式。</span><span class="sxs-lookup"><span data-stu-id="90ede-142">If you want to interpret multiple touch points in your application, you should create a message handler for the [**WM\_TOUCH**](wm-touchdown.md) message.</span></span>

-   <span data-ttu-id="90ede-143">[Windows Touch 輸入](guide-multi-touch-input.md)區段會說明如何解讀 [**WM \_ 觸控**](wm-touchdown.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="90ede-143">The [Windows Touch Input](guide-multi-touch-input.md) section explains how you can interpret the [**WM\_TOUCH**](wm-touchdown.md) message.</span></span>
-   <span data-ttu-id="90ede-144">[偵測 [和追蹤多個觸控點](detecting-and-tracking-multiple-touch-points.md) ] 區段會示範如何建立可解讀多個輸入的簡單應用程式。</span><span class="sxs-lookup"><span data-stu-id="90ede-144">The [Detecting and Tracking Multiple Touch Points](detecting-and-tracking-multiple-touch-points.md) section demonstrates how to create a simple application that interprets multiple inputs.</span></span>
-   <span data-ttu-id="90ede-145">[操作和慣性](manipulation-and-inertia.md)區段說明如何啟用最具彈性的方法來 Windows Touch。</span><span class="sxs-lookup"><span data-stu-id="90ede-145">The [Manipulations and Inertia](manipulation-and-inertia.md) section explains how to enable the most flexible approach to Windows Touch.</span></span>

## <a name="you-want-to-enable-windows-touch-input-to-an-application-that-uses-the-realtimestylus"></a><span data-ttu-id="90ede-146">您想要對使用 RealTimeStylus 的應用程式啟用 Windows Touch 輸入</span><span class="sxs-lookup"><span data-stu-id="90ede-146">You want to enable Windows Touch input to an application that uses the RealTimeStylus</span></span>

<span data-ttu-id="90ede-147">如果您想要針對 Tablet PC 平臺上的多個連絡人啟用輸入，您必須執行可解讀 Windows Touch 資料的自訂 RealTimeStylus 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="90ede-147">If you want to enable input for multiple contacts on the Tablet PC platform, you must implement a custom RealTimeStylus plug-in that interprets the Windows Touch data.</span></span> <span data-ttu-id="90ede-148">Microsoft 引進了 [**ITablet3**](/windows/desktop/tablet/itablet3) 和 [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3) 介面，可讓您從多個連絡人外掛程式的連絡人輸入。</span><span class="sxs-lookup"><span data-stu-id="90ede-148">Microsoft introduced the [**ITablet3**](/windows/desktop/tablet/itablet3) and [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3) interfaces to enable input from multiple contacts in the RealTimeStylus plug-in.</span></span> <span data-ttu-id="90ede-149">這些介面可簡化擴充 RealTimeStylus 外掛程式，以支援多個接觸點。</span><span class="sxs-lookup"><span data-stu-id="90ede-149">These interfaces simplify extending RealTimeStylus plug-ins to support multiple contact points.</span></span>

<span data-ttu-id="90ede-150">若要檢查是否已啟用多個連絡人的支援，請呼叫 [**IsMultiTouch**](/windows/desktop/tablet/itablet3-ismultitouch)。</span><span class="sxs-lookup"><span data-stu-id="90ede-150">To check whether support for multiple contacts is enabled, call [**IsMultiTouch**](/windows/desktop/tablet/itablet3-ismultitouch).</span></span> <span data-ttu-id="90ede-151">若要檢查支援的連絡人數目，請呼叫 [**GetMaximumCursors**](/windows/desktop/tablet/itablet3-getmaximumcursors)。</span><span class="sxs-lookup"><span data-stu-id="90ede-151">To check the number of supported contacts, call [**GetMaximumCursors**](/windows/desktop/tablet/itablet3-getmaximumcursors).</span></span> <span data-ttu-id="90ede-152">若要啟用或停用多連絡人支援，請呼叫 [**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)。</span><span class="sxs-lookup"><span data-stu-id="90ede-152">To enable or disable multiple contact support, call [**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled).</span></span>

> [!Note]  
> <span data-ttu-id="90ede-153">如果您未在多個 RealTimeStylus 中啟用多個連絡人點，則會收到軌跡訊息，例如平移和縮放。</span><span class="sxs-lookup"><span data-stu-id="90ede-153">If you don't enable multiple contact points in the RealTimeStylus, you will receive gesture messages such as pan and zoom.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="90ede-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="90ede-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90ede-155">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="90ede-155">Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 