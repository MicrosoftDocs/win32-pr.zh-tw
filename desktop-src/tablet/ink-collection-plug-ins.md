---
description: RealTimeStylus 物件原本就不會收集筆跡。 若要使用 RealTimeStylus 收集筆跡，請建立筆墨收集器外掛程式。
ms.assetid: 9a29525d-714a-431e-bb6f-4705d658537b
title: Ink-Collection 外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc060adf172938612e8f16f9a694e4ee3e1a7b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847781"
---
# <a name="ink-collection-plug-ins"></a><span data-ttu-id="64cde-104">Ink-Collection 外掛程式</span><span class="sxs-lookup"><span data-stu-id="64cde-104">Ink-Collection Plug-ins</span></span>

<span data-ttu-id="64cde-105">[**RealTimeStylus**](realtimestylus-class.md)物件原本就不會收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="64cde-105">The [**RealTimeStylus**](realtimestylus-class.md) object does not inherently collect ink.</span></span> <span data-ttu-id="64cde-106">若要使用 **RealTimeStylus** 收集筆跡，請建立筆墨收集器外掛程式。</span><span class="sxs-lookup"><span data-stu-id="64cde-106">To use the **RealTimeStylus** to collect ink, create an ink-collector plug-in.</span></span>

<span data-ttu-id="64cde-107">以下是在收集筆墨的表單上使用 [**RealTimeStylus**](realtimestylus-class.md) 物件的最基本案例。</span><span class="sxs-lookup"><span data-stu-id="64cde-107">The following is a minimal scenario for using the [**RealTimeStylus**](realtimestylus-class.md) object on a form that collects ink.</span></span>

1.  <span data-ttu-id="64cde-108">建立可執行 [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) 介面的表單。</span><span class="sxs-lookup"><span data-stu-id="64cde-108">Create a form that implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface.</span></span>
2.  <span data-ttu-id="64cde-109">建立 [**RealTimeStylus**](realtimestylus-class.md) 物件，並將它附加至表單上的控制項。</span><span class="sxs-lookup"><span data-stu-id="64cde-109">Create a [**RealTimeStylus**](realtimestylus-class.md) object, and attach it to a control on the form.</span></span>
3.  <span data-ttu-id="64cde-110">在表單的 [DataInterest](/previous-versions/ms574886(v=vs.100)) 屬性中，設定 StylusDown、封包和 StylusUp 通知的興趣。</span><span class="sxs-lookup"><span data-stu-id="64cde-110">Set interest in the StylusDown, Packets, and StylusUp notifications in the form's [DataInterest](/previous-versions/ms574886(v=vs.100)) property.</span></span>
4.  <span data-ttu-id="64cde-111">在表單的 [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown)、封 [**包**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets)和 [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) 方法中，新增程式碼以處理從表單之 [**RealTimeStylus**](realtimestylus-class.md) 物件傳送的手寫筆向下、封包和手寫筆的通知。</span><span class="sxs-lookup"><span data-stu-id="64cde-111">In the form's [**StylusDown**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusdown), [**Packets**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-packets), and [**StylusUp**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-stylusup) methods, add code to handle the stylus down, packets, and stylus up notifications that are sent from the form's [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="64cde-112">此程式碼應儲存畫筆資料，並建立和儲存筆劃。</span><span class="sxs-lookup"><span data-stu-id="64cde-112">This code should store the pen data, and create and store the strokes.</span></span>

<span data-ttu-id="64cde-113">如需這類應用程式的範例，請參閱 [ [RealTimeStylus 筆墨收集範例](realtimestylus-ink-collection-sample.md) ] 範例。</span><span class="sxs-lookup"><span data-stu-id="64cde-113">For a sample of such an application, see the [RealTimeStylus Ink Collection Sample](realtimestylus-ink-collection-sample.md) sample.</span></span>

> [!Note]  
> <span data-ttu-id="64cde-114">發生 [DisplaySettingsChanged](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) 事件時，請在 DisplaySettingsChanged 事件處理常式中呼叫所收集之筆劃的 [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) 方法，以重新計算 [寬度](/previous-versions/ms582112(v=vs.100)) 和 [高度](/previous-versions/ms582106(v=vs.100)) 屬性。</span><span class="sxs-lookup"><span data-stu-id="64cde-114">When a [DisplaySettingsChanged](/dotnet/api/microsoft.win32.systemevents.displaysettingschanged?view=dotnet-plat-ext-3.1) event occurs, call the [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) method of the collected strokes in a DisplaySettingsChanged event handler to recalculate the [Width](/previous-versions/ms582112(v=vs.100)) and [Height](/previous-versions/ms582106(v=vs.100)) properties.</span></span> <span data-ttu-id="64cde-115">這是考慮 DisplaySettingsChanged 事件所產生的每一英寸可能點 (DPI) 變更的必要專案。</span><span class="sxs-lookup"><span data-stu-id="64cde-115">This is necessary to account for possible dots per inch (dpi) changes that result from the DisplaySettingsChanged event.</span></span>

 

## <a name="ink-collection-and-recognizers"></a><span data-ttu-id="64cde-116">筆墨集合和辨識器</span><span class="sxs-lookup"><span data-stu-id="64cde-116">Ink Collection and Recognizers</span></span>

<span data-ttu-id="64cde-117">筆墨分析和手寫辨識都不是 [**RealTimeStylus**](realtimestylus-class.md) 物件的功能。</span><span class="sxs-lookup"><span data-stu-id="64cde-117">Neither ink analysis nor handwriting recognition is a function of the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="64cde-118">當筆墨收集器外掛程式收集筆墨或您想要辨識筆墨時，您可以將筆墨複製到 [RecognizerCoNtext](/previous-versions/ms552546(v=vs.100)) 或 [分隔](/previous-versions/ms583616(v=vs.100)) 物件。</span><span class="sxs-lookup"><span data-stu-id="64cde-118">As the ink-collector plug-in collects ink-or as you want to recognize the ink-you can copy the ink to a [RecognizerContext](/previous-versions/ms552546(v=vs.100)) or [Divider](/previous-versions/ms583616(v=vs.100)) object.</span></span> <span data-ttu-id="64cde-119">如需辨識和筆跡分析的詳細資訊，請參閱 [關於手寫辨識](about-handwriting-recognition.md) 或 [分隔物件](the-divider-object.md)。</span><span class="sxs-lookup"><span data-stu-id="64cde-119">For more information about recognition and ink analysis, see [About Handwriting Recognition](about-handwriting-recognition.md) or [The Divider Object](the-divider-object.md).</span></span>

## <a name="static-rendering"></a><span data-ttu-id="64cde-120">靜態呈現</span><span class="sxs-lookup"><span data-stu-id="64cde-120">Static Rendering</span></span>

<span data-ttu-id="64cde-121">若要在收集時轉譯筆墨，請將 [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) 物件附加至 [**RealTimeStylus**](realtimestylus-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="64cde-121">To render ink as it is being collected, attach a [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) object to the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="64cde-122">若要在收集筆墨之後轉譯筆墨，請使用轉譯 [器物件將](/previous-versions/ms552630(v=vs.100)) 筆劃繪製至適當的 [圖形](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) 物件。</span><span class="sxs-lookup"><span data-stu-id="64cde-122">To render ink after it has been collected, use a [Renderer](/previous-versions/ms552630(v=vs.100)) object to draw the strokes to the appropriate [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1) object.</span></span> <span data-ttu-id="64cde-123">如需 DynamicRenderer 物件的詳細資訊，請參閱動態轉譯器 [外掛程式](dynamic-renderer-plug-ins.md)。如需靜態和動態轉譯的範例，請參閱 [RealTimeStylus 筆墨收集範例](realtimestylus-ink-collection-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="64cde-123">For more information about the DynamicRenderer object, see [Dynamic-Renderer Plug-ins](dynamic-renderer-plug-ins.md). For a sample of both static and dynamic rendering, see [RealTimeStylus Ink Collection Sample](realtimestylus-ink-collection-sample.md).</span></span>

 

 
